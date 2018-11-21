# React stuff 🔥

Regularly updated list with resources and links we found on the web, curated by the [Cloud District](http://clouddistrict.com) team.

---

## JavaScript

- [Clean code javascript](https://github.com/ryanmcdermott/clean-code-javascript)
- [Airbnb JavaScript Style Guide](https://github.com/airbnb/javascript)
- [Optimistic UI updates 📹](https://egghead.io/courses/optimistic-ui-updates-in-react?utm_source=drip&utm_medium=email&utm_content=react)
- [[Meetup] Javascript Kata: aplicando clean code y buenas prácticas en vivo](https://www.youtube.com/watch?v=C5IrXwu6nSQ&t=559s)

## React

- Boiler template

  - [Create React App](https://github.com/facebookincubator/create-react-app)

- Tips

  - [Official documentation](https://reactjs.org)
  - [Awesome React](https://github.com/enaqx/awesome-react)
  - [React v16.6](https://sergiodxa.com/essays/react-v-16-6)
  - [React v16.6.0: lazy, memo and contextType](https://reactjs.org/blog/2018/10/23/react-v-16-6.html)
  - [The Beginner's Guide to React📹](https://egghead.io/courses/the-beginner-s-guide-to-react)

## Tools

- [VS Code](https://code.visualstudio.com/)
- [Flow](https://flow.org/en/docs/install/)
- [Prettier](https://github.com/prettier/prettier)
- [React Devtools](https://github.com/facebook/react-devtools/tree/master/packages/react-devtools)
- [Debugging Tools](https://codeburst.io/react-native-debugging-tools-3a24e4e40e4)

## Libs

- Yarn --> [Yarn - Dependency management](https://yarnpkg.com/es-ES/)
- Router --> [react-router](https://github.com/ReactTraining/react-router)
- Redux --> [Redux](https://github.com/reactjs/redux/)
  | [Redux Thunk](https://github.com/gaearon/redux-thunk)
  | [Redux Persist](https://github.com/rt2zz/redux-persist)
  | [Redux Logger](https://github.com/LogRocket/redux-logger)
- Api --> [Axios](https://github.com/axios/axios)
  | [Querystring Parser](https://github.com/ljharb/qs)
- Objects/Arrays --> [Lodash](https://lodash.com/)
- Dates --> [Moment](https://momentjs.com/)
- Test --> [Jest](https://facebook.github.io/jest/)
- i18n --> [react-localization](https://github.com/stefalda/react-localization)

## Redux

- [Redux](https://redux.js.org/)
- [Getting started with Redux](https://egghead.io/courses/getting-started-with-redux)
- [Using Redux with React Native](https://medium.com/@pavsidhu/using-redux-with-react-native-9d07381507fe)
- [When do I know I'm ready for Redux](https://medium.com/dailyjs/when-do-i-know-im-ready-for-redux-f34da253c85f)
- [Redux 4 ways](https://medium.com/react-native-training/redux-4-ways-95a130da0cdc)
- [5 Ways to Connect Redux Actions](https://blog.benestudio.co/5-ways-to-connect-redux-actions-3f56af4009c8)
- [Quick Redux tips for connecting your React components](https://medium.com/dailyjs/quick-redux-tips-for-connecting-your-react-components-e08da72f5b3)
- [Awsome Redux Repo](https://github.com/xgrommx/awesome-redux)

## Flex

- [CSS-Tricks](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)

## Grid

- [CSS-Tricks](https://css-tricks.com/snippets/css/complete-guide-grid/)

## styled-components

- [styled components](https://www.styled-components.com)
- [Flexbox Froggy Game](https://flexboxfroggy.com/#es)
- [The magic behind 💅 styled-components](https://mxstbr.blog/2016/11/styled-components-magic-explained/)
- [Awesome 💅 Styled Components](https://github.com/styled-components/awesome-styled-components)
- Have the suffix 'Styled'
- They are inside styled.js

---

## Proyect Folder Structure

- [Better organize your React App](https://medium.com/@alexmngn/how-to-better-organize-your-react-applications-2fd3ea1920f1)
- [Organizing a React Native Project](https://medium.com/the-react-native-log/organizing-a-react-native-project-9514dfadaa0)

```
  /
  ├── public
        ├── index.html
  ├── index.js
  ├── src/
        ├── api/
        ├── assets/
            ├── css/
            ├── i18n/
            ├── images/
            ├── fonts/
        ├── config/
            ├── api.js
            ├── constants.js
            ├── paths.js
            ├── redux.js
            ├── styled.js
            ├── styles.js
        ├── redux/
        ├── stories/
        ├── components/
            ├── system/
            ├── pages/
            ├── organisms/
            ├── molecules/
            ├── atoms/
```

## Redux Duck Folder Structure

- [Reducks - duck folders](https://github.com/alexnm/re-ducks)
- One duck for each bussines concept
- Separated from the components for easy integration with React

```
duck/
├── index.js        --> Index
├── actions.js      --> Simple actions
├── operations.js   --> Asyncs actions (thuncs)
├── reducers.js     --> Reducer
├── selectors.js    --> State mappers (mapStateToProps)
├── tests.js        --> Test
├── types.js        --> Simple actions types
├── utils.js        --> Other functions
```

## Visual Components Folder Structure

- [Presentational and Container Components](https://medium.com/@dan_abramov/smart-and-dumb-components-7ca2f9a7c7d0)

```
component/
├── container.js  --> Redux Container Component
├── index.js      --> index/dinamic imports (react-loadable)
├── view.js       --> Presentational Component
├── utils.js      --> Internal utils
├── styles.css    --> old css clases
├── styled.js     --> Styled components
```

## Atomic design

- [atomic design](http://bradfrost.com/blog/post/atomic-web-design/)
- [¿Qué es el diseño atómico?](https://medium.com/pixel-perfect/qué-es-el-diseño-atómico-a5cbed06688e)

## Code Formatter

- [Prettier](https://github.com/prettier/prettier)

* Install prettier (VSCode extension)
* Menu>Preferences>config>User Config
* Add:

```
    "editor.formatOnSave": false,
    "[javascript]": {
        "editor.formatOnSave": true
    }
```

## Scripts

- Deploy:
  - `yarn install`
  - `yarn start`
  - http://localhost:3000/
- Test:
  - `yarn test`
  - `yarn test --coverage`
- Production:
  - Build --> `yarn build`
  - Analyze --> `yarn analyze`
