# React stuff 🔥

Regularly updated list with resources and links we found on the web, curated by the [Cloud District](http://clouddistrict.com) team.

---
## React

* Boiler template
  * [Create React App](https://github.com/facebookincubator/create-react-app)

* Inspiration for everything
  * [Official documentation](https://reactjs.org)
  * [Awesome React](https://github.com/enaqx/awesome-react)

* Courses / Tutorials / Books
  * [The Beginner's Guide to React📹](https://egghead.io/courses/the-beginner-s-guide-to-react) 
  * [Getting started with Redux](https://egghead.io/courses/getting-started-with-redux)

* Tools
  * [VS Code](https://code.visualstudio.com/)
  * [Flow](https://flow.org/en/docs/install/)
  * [Prettier](https://github.com/prettier/prettier)
  * [React Devtools](https://github.com/facebook/react-devtools/tree/master/packages/react-devtools)
  * [Debugging Tools](https://codeburst.io/react-native-debugging-tools-3a24e4e40e4)

* Libs
  * Yarn                  --> [Yarn - Dependency management](https://yarnpkg.com/es-ES/)
  * Router                --> [react-router](https://github.com/ReactTraining/react-router)
  * Redux                 --> [Redux](https://github.com/reactjs/redux/)
                              | [Redux Thunk](https://github.com/gaearon/redux-thunk)
                              | [Redux Persist](https://github.com/rt2zz/redux-persist)
  * Api                   --> [Axios](https://github.com/axios/axios)
                              | [Querystring Parser](https://github.com/ljharb/qs)
  * Objects/Arrays        --> [Lodash](https://lodash.com/)
  * Dates                 --> [Moment](https://momentjs.com/)
  * Test                  --> [Jest](https://facebook.github.io/jest/)
  * Dinamic imports rutes --> [react-loadable](https://github.com/jamiebuilds/react-loadable)
  * styled-components     --> [styled-components](https://github.com/styled-components/styled-components)
  * Storybook             --> [Storybook](https://github.com/storybooks/storybook)
  * Async Components Load --> [react-loadable](https://github.com/jamiebuilds/react-loadable)
  * i18n                  --> [react-localization](https://github.com/stefalda/react-localization)

* UI Components
  * [react-dropzone](https://github.com/react-dropzone/react-dropzone)
  * [react-placeholder](https://github.com/buildo/react-placeholder)
  * [react-spinkit](https://github.com/KyleAMathews/react-spinkit)
  * [react-slick](https://github.com/akiran/react-slick)
  * [reapop](https://github.com/LouisBarranqueiro/reapop)
  * [react-stepzilla](https://github.com/newbreedofgeek/react-stepzilla)

* UIKits
  * [Material-ui](https://material-ui.com)
  * [React-Bootstrap](https://react-bootstrap.github.io)

* Redux tips
  * [Redux](https://redux.js.org/)
  * [Using Redux with React Native](https://medium.com/@pavsidhu/using-redux-with-react-native-9d07381507fe) 
  * [When do I know I'm ready for Redux](https://medium.com/dailyjs/when-do-i-know-im-ready-for-redux-f34da253c85f)
  * [Redux 4 ways](https://medium.com/react-native-training/redux-4-ways-95a130da0cdc)
  * [5 Ways to Connect Redux Actions](https://blog.benestudio.co/5-ways-to-connect-redux-actions-3f56af4009c8)
  * [Quick Redux tips for connecting your React components](https://medium.com/dailyjs/quick-redux-tips-for-connecting-your-react-components-e08da72f5b3)
  * [Awsome Redux Repo](https://github.com/xgrommx/awesome-redux)

* Flex
  * [CSS-Tricks](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)

* Grird
  * [CSS-Tricks](https://css-tricks.com/snippets/css/complete-guide-grid/)

* styled-components Tips
  * [Flexbox Froggy Game](https://flexboxfroggy.com/#es)
  * [The magic behind 💅 styled-components](https://mxstbr.blog/2016/11/styled-components-magic-explained/)
  * [Awesome 💅 Styled Components](https://github.com/styled-components/awesome-styled-components)
  * Have the suffix 'Styled'
  * They are inside styled.js

* Other Articles and examples
  * [Optimistic UI updates 📹](https://egghead.io/courses/optimistic-ui-updates-in-react?utm_source=drip&utm_medium=email&utm_content=react)
  * [[Meetup] Javascript Kata: aplicando clean code y buenas prácticas en vivo](https://www.youtube.com/watch?v=C5IrXwu6nSQ&t=559s)


---

## Proyect Folder Structure

* [Better organize your React App](https://medium.com/@alexmngn/how-to-better-organize-your-react-applications-2fd3ea1920f1)
* [Organizing a React Native Project](https://medium.com/the-react-native-log/organizing-a-react-native-project-9514dfadaa0)

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

* [Reducks - duck folders](https://github.com/alexnm/re-ducks)
*  One duck for each bussines concept
*  Separated from the components for easy integration with React Native
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

* [Presentational and Container Components](https://medium.com/@dan_abramov/smart-and-dumb-components-7ca2f9a7c7d0)

```
component/
├── container.js  --> Redux Container Component
├── index.js      --> index/dinamic imports (react-loadable)
├── view.js       --> Presentational Component 
├── utils.js      --> Internal utils
├── styles.css    --> old css clases 
├── styled.js     --> Styled components
```

    
## Atomic design inspiration

* [atomic design](http://bradfrost.com/blog/post/atomic-web-design/)
* [¿Qué es el diseño atómico?](https://medium.com/pixel-perfect/qué-es-el-diseño-atómico-a5cbed06688e)


## Code Formatter

* [Prettier](https://github.com/prettier/prettier)

- Install prettier (VSCode extension)
- Menu>Preferences>config>User Config
- Add:
```
    "editor.formatOnSave": false,
    "[javascript]": {
        "editor.formatOnSave": true
    }
```

## Storybooks

* [Storybook](https://storybook.js.org/)
* ```npm i -g @storybook/cli```
* ```yarn run storybook```
* http://localhost:9009/

```
├── stories/ 
    ├── atoms
    ├── molecules 
    ├── organism 
```

## Scripts
* Deploy: 
    * ```yarn install```  
    * ```yarn start```
    * http://localhost:3000/
* Test: 
    * ```yarn test```
    * ```yarn test --coverage```
* Storybook: 
    * ```yarn run storybook```
    * http://localhost:9009/
* Production:
    * Build --> ```yarn build``` 
    * Analyze --> ```yarn analyze```