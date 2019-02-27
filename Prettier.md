Prettier es un formateador de código. Es decir, modifica o arregla nuestro código según nuestra configuración para mantener todos los proyectos consistentes con las mismas reglas.

## Información oficial

* [Prettier · Opinionated Code Formatter](https://prettier.io/) 
* [GitHub - prettier/prettier: Prettier is an opinionated code formatter.](https://github.com/prettier/prettier)
* [GitHub - obartra/prettierrc: 🗄️ 💅 config file for prettier](https://github.com/obartra/prettierrc)

## Cómo integrar con Visual Studio Code

En el menú de **extensiones**:

* Buscar 'Prettier'
* Instalar y reiniciar

En el menú de **configuración**

* Buscar 'javascript' y habilitar la opción Javascript>Format>Enable (para que el editor aplique el formato de forma automática al guardar el fichero)
* Buscar 'prettier' y habilitar la opción Prettier>Require Config (para que sólo aplique el formato en proyectos con prettier habilitado)

## Fichero de configuración

Añadir en el directorio raíz el fichero .prettierrc

```json
{
    "printWidth": 160,
    "parser": "flow",
    "semi": false,
    "singleQuote": true,
    "bracketSpacing": true
 }
```

## Actualizar todos los ficheros js de un proyecto

`$ yarn global add prettier`

`$ prettier --config package.json --write 'src/\*\*/\*.js'`