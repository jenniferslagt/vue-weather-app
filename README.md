# Weather app
![Schermafbeelding 2020-09-28 om 16 32 35](https://user-images.githubusercontent.com/45489420/94445855-3c231e00-01a8-11eb-80d7-f3a8c1eab1f1.png)

Check it <a href="https://jenniferslagt.github.io/vue-weather-app/"> here </a>

## Description
The weather app is a small app in which you have actually one main functionality: searching for a location and displaying the weather about that location. This app is made with the Vue.js framework and the Open Weather API. 

## Vue.js
Vue is a progressive framework for building user interfaces and based on Node.js. Vue.js features an incrementally adaptable architecture that focuses on declarative rendering and component composition. The core library is focused on the view layer only, so it's formally made for Front-Enders. Vue.js uses an HTML-based template syntax that allows binding the rendered DOM to the underlying Vue instance's data.  

## Open Weather API
The Open Weather API is one of the leading digital weather information providers. They offer a current, forecast and historical collection. I used the current collection. You can easily registrate and get a key to use the free data (check the source for more).

## Learning goals
The main goal on this small weather app is to learn Vue.js, this is what I've done: 
* I've learned what Vue.js is and how it works.
* I understand how data and methods work.
* You can bind data and make it dynamic.
* I know how events work. 
* I understand how events modifiers work and learnt about keyboard events.
* I understand how two-way data binding works between the parent (Vue.js) and its components.
* Props are used for data from the parent to the component(s).
* You can use $emit and $on to send data from the child and receive it on the child.
* I understand how to use conditional states. 
* You can toggle CSS classes based on the dynamic data. Fun fact: I changed the background based on the temperature with a simple class. When it's "warm" the background will be a desert, otherwise it will be a cold snowy background.

In short: this project was focused on working with components and dynamic data with Vue.js. I used the tutorial as a begin, then I splitted it up in more components and added some other features to make this work (check the sources for more info).


## Project setup
Please install Node.js and then Vue.js before you reuse this project.

```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).


## Sources
* [Build a Weather App in VueJS | VueJS Beginner Tutorial](https://www.youtube.com/watch?v=JLc-hWsPTUY)
* [Open Weather API](https://openweathermap.org/api)
* [Passing data between Vue components](https://dev-notes.eu/2018/05/passing-data-between-vue-components/#:~:text=Pass%20Data%20from%20Child%20to,the%20data%20value%20to%20pass.)
* [The Net Ninja: Vue JS 2 Tutorial](https://www.youtube.com/watch?v=5LYrN_cAJoA&list=PL4cUxeGkcC9gQcYgjhBoeQH7wiAyZNrYa)

