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
 
