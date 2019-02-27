# 🔥React Bible🔥

Este documento tiene como objetivo describir el stack tecnológico que estamos usando en el departamento de Frontend.

Actualmente el núcleo principal del departamento  es la librería **React** para el renderizado, **React Router** para el enrutado, **Redux** para la lógica de negocio, **styled-components** para añadir los estilos y **Jest** para los tests unitarios. Como editor utilizamos **Visual Studio Code** configurado con **Prettier** y **ESLint**.

## Javascript

* [GitHub - ryanmcdermott/clean-code-javascript: Clean Code...](https://github.com/ryanmcdermott/clean-code-javascript)
* [GitHub - airbnb/javascript: JavaScript Style Guide](https://github.com/airbnb/javascript)

## React

* [React – A JavaScript library for building user interfaces](https://reactjs.org)
* [GitHub - enaqx/awesome-react: A collection of awesome...](https://github.com/enaqx/awesome-react)

## Boiler template

* [GitHub - facebook/create-react-app: Set up a modern web app...](https://github.com/facebookincubator/create-react-app)

## Herramientas

* [Visual Studio Code  → Visual Studio Code - Code Editing. Redefined](https://code.visualstudio.com/)
* [Prettier · Opinionated Code Formatter](https://prettier.io)
* [ESLint - Pluggable JavaScript linter](https://eslint.org)
* [react-devtools → react-devtools/packages/react-devtools at master ·...](https://github.com/facebook/react-devtools/tree/master/packages/react-devtools)

## Estructura de carpetas

Proyecto

```
  /
  ├── src/                                     
    ├── assets/      
    ├── components/ 
    ├── config/         
    ├── redux/       
    ├── services/   
```

Recursos

```
  /                  
  ├── src/                                   
    ├── assets/ 
      ├── colors/  
      ├── fonts/   
      ├── images/ 
      ├── i18n/   
```

Atomic design

```
  ├── src/                                                    
        ├── components/             
            ├── system/    
            ├── pages/       
            ├── organisms/          
            ├── molecules/          
            ├── atoms/   
```

Componente

```
<component>/
    ├── container.js  --> Redux Container Component (HOC)
    ├── index.js      --> External api
    ├── view.js       --> Presentational Component 
    ├── utils.js      --> Internal utils
    ├── styled.js     --> Styled components
    ├── readme.md     --> Style Guidist
    ├── test.js       --> Correct render test
```

Redux (re-ducs)

```
<duck>/
    ├── index.js        
    ├── actions.js      --> Simple actions with Flux Standard Action pattern
    ├── operations.js   --> Asyncs actions (thunks)
    ├── reducers.js     --> Reducer 
    ├── tests.js        --> Test
    ├── types.js        --> Simple actions types
    ├── utils.js        --> Other functions
```

## Redux

* [Redux · A Predictable State Container for JS Apps](https://redux.js.org/)
* [Redux 4 Ways – React Native Training – Medium](https://medium.com/react-native-training/redux-4-ways-95a130da0cdc)
* [5 Ways to Connect Redux Actions – Bene Studio](https://blog.benestudio.co/5-ways-to-connect-redux-actions-3f56af4009c8)
* awesome-redux → [GitHub - xgrommx/awesome-redux: Awesome list of Redux examples and middlewares](https://github.com/xgrommx/awesome-redux)
* re-ducs → [GitHub - alexnm/re-ducks: An attempt to extend the original...](https://github.com/alexnm/re-ducks)
* redux → [Redux · A Predictable State Container for JS Apps](https://redux.js.org)
* react-redux → [React Redux · Official React bindings for Redux](https://react-redux.js.org)
* redux-thunk → [GitHub - reduxjs/redux-thunk: Thunk middleware for Redux](https://github.com/reduxjs/redux-thunk)
* redux-logger → [GitHub - LogRocket/redux-logger: Logger for Redux](https://github.com/LogRocket/redux-logger)
* redux-persist → [GitHub - rt2zz/redux-persist: persist and rehydrate a redux store](https://github.com/rt2zz/redux-persist)

## Styled components

* styled-components → [styled-components](https://www.styled-components.com)

## Axios

* axios → [GitHub - axios/axios: Promise based HTTP client for the browser and node.js](https://github.com/axios/axios)
* axios-response-logger → [GitHub - srph/axios-response-logger: Axios interceptor which logs responses](https://github.com/srph/axios-response-logger)
* qs → [GitHub - ljharb/qs: A querystring parser with nesting support](https://github.com/ljharb/qs)

## i18n

* react-localization → [GitHub - stefalda/react-localization: Simple module to...](https://github.com/stefalda/react-localization)

## Test

* jest → [Jest · 🃏 Delightful JavaScript Testing](https://jestjs.io/)
* redux-mock-store → [GitHub - dmitry-zaets/redux-mock-store: A mock store for...](https://github.com/dmitry-zaets/redux-mock-store)

## Utilidades

* lodash → [Lodash](https://lodash.com)
* moment → [Moment.js | Home](https://momentjs.com)

## Guia de estilos

* react-styleguidist → [React Styleguidist: isolated React component development...](https://react-styleguidist.js.org)
* storybook → [https://storybook.js.org](https://storybook.js.org) 