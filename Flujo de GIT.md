# Flujo de Git

## Objetivos

* Trazabilidad de cambios en el software
* Estandarización del proceso
* Revisión de código centrados en mejorar la calidad
* Apoyo a integración continua
* Evitar discrepancias entre entornos (producción y desarrollo)

Para cumplir estos **objetivos** necesitamos varias características:

* **Pull Request** para la trazabilidad y revisión del código
* Al menos **2 ramas eternas **para desarrollo/pre y producción (develop, master)
* Añadir **tags de versionado**

## Tags de Versionado

* En **Backend** los tags no deberían ser necesarios pero es posible que sean útiles si nos movemos a un sistema SaaS para tener control sobre qué versiones están desplegadas. Lo valoraremos más adelante.
* En el caso del **Desarrollo Mobile**, usaremos los tags para marcar las versiones con las que se generaron los diferentes apk/ipa. De este modo se podrá controlar exactamente que va en cada versión.

Para realizar el etiquetado se recomienda usar la estrategia de versionado semántico ([Semantic Versioning 2.0.0 | Semantic Versioning](https://semver.org/)). Se requiere empezar a etiquetar en el momento en el que proyecto se suba a producción.

![](https://lh3.googleusercontent.com/1xYYEHFlZD69R_K0J2PwWzxlorCSUb187YIw8fZLCeB404URQjy7MZyNpz0mVTyLw2pIV4hfzCaj04TPwV-KKwraB4Ot28Wh5eiNUeFvPELdHpYy2pzenXflFzemLsmsq-rXYmrOsZg)

## Consistencia en los Commits

El objetivo es que estandaricemos los mensajes de los commits y los PR.

Se propone un prefijo para los cambios en commits y pull requests

* ** \[FIX\] **Para arreglos o bugs detectados 
* ** \[ADD\]** Añadida nueva funcionalidad
* ** \[UPDATE\]** Actualización de una funcionalidad ya desarrollada
*  **\[REFACTOR\] ** Commit centrado en refactorizar cambios
*  **\[DELETE\]** Commit centrado en eliminar código ya no necesario

Ejemplos:

`$ git commit -m  "\[FIX\] Resolved issue with redis cache"`

`$ git commit -m  "\[ADD\] Add new user notification"`

## Estrategia de Ramas

Al final hemos optado por un modelo parecido a **gitflow** pero eliminando la rama de release que en nuestro caso añade demasiada complejidad sin mayor beneficio.  [Introducing GitFlow](https://datasift.github.io/gitflow/IntroducingGitFlow.html)\
\
Nos hubiese gustado un esquema con solo una rama eterna pero la necesidad de diferenciar en muchos proyectos DEV y PROD lo hace difícil. Más adelante lo valoraremos en función de la experiencia.\
\
Los merge se han de hacer mediante **pull request **(PR a partir de ahora). La necesidad de una validación por parte de otra persona dependerá del tipo de proyecto y número de personas implicadas.

## Ejemplo de flujo de una nueva funcionalidad.

```shell
git checkout develop <- Recordar crear la rama feature desde develop
git checkout -b feature/crud-automated-testing 
<Trabajamos en la rama haciendo commits>
git push 
<Hacer PR mediante el enlace> 
Resolver PR en bitbucket 
git checkout develop 
git pull
```

En el caso de que no se acepte por alguna razón el pull request siempre se puede volver a hacer commits y hacer otro PR más adelante.

## Ejemplo de flujo para un hotfix

Para un **hotfix** el proceso es el mismo, solo que se parte de master y se hace pull request a master y la rama nueva se ha de llama **hotfix/<descripción>**

Después de un **hotfix** se tendrá que hacer merge de la rama master contra la rama develop, para asegurar la consistencia entre las dos ramas.

## Despliegue

Llevar** cambios a producción** consiste en hacer PR de dev a master. Si se llega a implementar un sistema de despliegue continuo (CD) este paso se hará de manera automática.

![](https://lh4.googleusercontent.com/8wywM0NYa8DBbep161FCWM_u9utlL1De77UZAi6acFLXA-uILAiSP3te0oNRDAiF-MNoWLBeUuCm8TV38GVKjh-RGKOEPLkxLTdHdgqaJR2wFGJSSAz0UYW-cYLrFmcg0YwPihEsJLQ)

Para tener más claro el funcionamiento de los PR, la guía de de uso en **gitflow** ([Pull Requests and Gitflow](https://blog.axosoft.com/pull-requests-gitflow/))  es interesante aunque no sea exactamente el mismo esquema que usaremos.

## ¿Qué debemos de revisar antes de enviar un PR?

* No hay código muerto
* El código no tiene comentarios innecesarios
* Las variables están definidas dentro de su ámbito de acción más inmediato, y lo más cerca posible de donde se usan por 1ª vez
* Los nombres de las funciones se corresponden con lo que realmente hacen
* Los test prueban lo que realmente tienen que probar. 
* Se usa tipificación estricta siempre que sea posible

Revisar tus Pull Request antes que lo haga un compañero, ayudará a detectar problemas antes de que los detecte un tercero.

## ¿Qué es un Code Review?

**Code Review**, es el proceso mediante el cual los **distintos miembros de un equipo revisan en conjunto** la implementación realizada por otro miembro. Aportando **ideas sobre mejoras** en la implementación,** **posibles** refactorizaciones**, discusión de posibles **bugs**, **optimizaciones**, errores o **mejoras de arquitectura**, conveniencia o falta de cobertura de test, y todo tipo de discusiones sobre los cambios realizados para entregar una determinada funcionalidad.

Es importante que persigamos  los valores principales de **Extreme Programming**:

**Simplicidad**: KISS (Keep it Simple Stupid),  Evitar sobre ingeniería\
**Comunicación: **Código auto-documentado, Pair Programming,  Autoría Colectiva del Código\
**Feedback: **Ciclos Cortos de desarrollo, Ejecutar Pruebas Frecuentemente\
**Valentía: **Refactoring cuando es necesario,  Persistencia en los objetivos\
**Respeto: **> Autoestima > Productividad

## Recomendaciones para hacer un Code Review

* Como desarrollador, se **responsables** de crear código **funcional y mantenible.**
* Mantén una **mentalidad abierta** durante las revisiones de código. Realizar o acudir a revisiones de código con una actitud defensiva, es malo para todos
* Se **humilde**, aprende del resto, cada día te llevarás una lección, pregunta si es necesario
* Indica las mejoras de una forma **constructiva**. 
* Señala también lo bueno, no solo te quedes con los defectos

## ¿En que debemos de fijarnos en el proceso de Code Review?

* Propósito del cambio
* Legibilidad y estilo del código
* Diseño del código
* Mantenibilidad
* Seguridad
* Rendimiento

## Presentaciones destacadas:

**Slides Estrategia de GIT:**  [https://docs.google.com/presentation/d/1NtJ7_rA7q-mxDAbjUji4_SZ88S_jaedkPEXsXuvj7wE/edit](https://docs.google.com/presentation/d/1NtJ7_rA7q-mxDAbjUji4_SZ88S_jaedkPEXsXuvj7wE/edit)

**Slides Gitflow + Code Review: **[https://docs.google.com/presentation/d/1ClMSYVSTPvtLmTMspWmyZfEZX_jnXHpNzLP9c8JoUAQ/edit](https://docs.google.com/presentation/d/1ClMSYVSTPvtLmTMspWmyZfEZX_jnXHpNzLP9c8JoUAQ/edit)\
\

\

\
