# ESLint

ESLint es una herramienta de *linting* para Javascript. Un linter es un programa que se encarga de revisar el código e ir señalando errores y posibles bugs. 

El propósito de ESLint es encontrar errores de manera automática sin tener que ejecutar el código y poder corregirlos manualmente, o incluso de manera automática.

ESLint está basado en reglas que son 100% configurables y viene con un conjunto pre establecido que podemos usar como punto de inicio y más adelante poder activar o desactivar ciertas reglas a nuestra conveniencia.

## Documentación oficial

* [ESLint - Pluggable JavaScript linter](https://eslint.org)

## Extensión de VS Code

* [ESLint - Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)

## Instalar en cada proyecto

```shell
npm install --save-dev babel-eslint eslint eslint-plugin-react
```

## Fichero de configuración

Añadir el fichero .eslintrc en el directorio raíz

```json
{
    "parser": "babel-eslint",
    "env": {
        "browser": true,
      	"amd": true,
        "jest": true,
      	"es6": true
    },
    "plugins": [
        "react"
    ],
    "extends": [
        "eslint:recommended",
        "plugin:react/recommended"
    ],
    "rules": {
    	"no-console": "warn",
        "no-unused-vars": "warn"
    }
}
```

## Lecturas

* [Getting eslint right in React Native – The React Native Log – Medium](https://medium.com/the-react-native-log/getting-eslint-right-in-react-native-bd27524cc77b)
* [Cómo usar ESLint y Prettier para mejorar tu código JavaScript](https://platzi.com/tutoriales/1099-fundamentos-javascript-2017/2181-como-usar-eslint-y-prettier-para-mejorar-tu-codigo-javascript/)
* [GitHub - ryanmcdermott/clean-code-javascript: Clean Code...](https://github.com/ryanmcdermott/clean-code-javascript) 
* [GitHub - airbnb/javascript: JavaScript Style Guide](https://github.com/airbnb/javascript)