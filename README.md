# NuxtCheatSheet

## TODO:
- [ ] Should I add an API testing page in the vue?



#### Start Nuxt App

```
npx create-nuxt-app <project-name>
```


#### import font awesome if needed
```
      {
        rel: "stylesheet",
        href: "https://use.fontawesome.com/releases/v5.0.13/css/all.css"
      }
```
[[Vuetify-FontAwesome]](https://vuetifyjs.com/en/customization/icons#install-font-awesome-5-icons)


#### Adding Proxy if needed
[[Nuxt Proxy]](https://zh.nuxtjs.org/faq/http-proxy/)


Proxy setting
```
  proxy: {
    "/api": {
      target: "http://localhost:8080",
      pathRewrite: {
        "^/api": "/"
      }
    }
  },

```


#### Adding Cookies if needed
[[Nuxt Cookies]](https://www.npmjs.com/package/cookie-universal-nuxt)

##### Get
```javascript
user = this.$cookies.get("user");
```

##### Set

```javascript
this.$cookies.set("user", user);
```



#### Adding Infinite Scroll if needed

[[vue-infinite-scroll in Nuxt]](https://blog.csdn.net/qq_39711712/article/details/88529678)
[[GitHub]](https://github.com/ElemeFE/vue-infinite-scroll)
[[in Vuejs]](https://www.jianshu.com/p/c4abab8c1ba6)
 
Add a Plugin "vue-infinite-scroll.js"
 ```javascript
import Vue from 'vue';
import infiniteScroll from 'vue-infinite-scroll';

export default () => {
  Vue.use(infiniteScroll)
}
 ```
 In nuxt.config.js
 
 ```javascript
  plugins: [{
    src: '~plugins/vue-infinite-scroll',
    ssr: false
  }],
 ```
 
 
 #### Install marked if using markdown
 
 [[Marked]](https://github.com/markedjs/marked)
 
 ```
 npm install --save marked
 ```
 
 
 #### Adding Util functions 
 
 ```javascript
 
import moment from "moment";
import marked from "marked";

const formateTime = time => {
  return moment(time).format("Do MMMM YYYY hh:mm a");
};

const sortByCreatedAt = (a, b) => {
  if (a.createdAt > b.createdAt) {
    return -1;
  } else if (a.createdAt < b.createdAt) {
    return 1;
  } else {
    return 0;
  }
};

const sortByCreatedAtReverse = (a, b) => {
  if (a.createdAt > b.createdAt) {
    return 1;
  } else if (a.createdAt < b.createdAt) {
    return -1;
  } else {
    return 0;
  }
};

const tidyUpText = text => {
  return text
    .trim()
    .toLowerCase()
    .replace(/ /g, "-");
};

const compiledMarkdown = md => marked(md, { breaks: true });

export default {
  formateTime,
  sortByCreatedAt,
  tidyUpText,
  compiledMarkdown,
  sortByCreatedAtReverse
};

 ```
 
