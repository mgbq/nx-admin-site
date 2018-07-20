# 锁屏
### 1.    实现思路
- ( 1 ) 设置锁屏密码
- ( 2 ) 密码存localStorage (本项目已经封装h5的sessionStorage和localStorage)
- ( 3 ) vuex设置 `SET_LOCK  state.isLock = true` (为true是锁屏状态)
- ( 4 ) 在路由里面判断vuex的isLock(为true锁屏状态不能让用户后退url和自行修改url跳转页面否则可以)


#### （1）设置锁屏密码

```js
  handleSetLock() {
      this.$refs['form'].validate(valid => {
        if (valid) {
          this.$store.commit('SET_LOCK_PASSWD', this.form.passwd)
          this.handleLock()
        }
      })
    },
```

#### （ 2 )  密码存localStorage `setStore`是自己封装的方法
```js
  SET_LOCK_PASSWD: (state, lockPasswd) => {
      state.lockPasswd = lockPasswd
      setStore({
        name: 'lockPasswd',
        content: state.lockPasswd,
        type: 'session'
      })
    },
```

####  ( 3 )  vuex设置 `SET_LOCK  state.isLock = true` 同时存在store里面

```js
  SET_LOCK: (state, action) => {
      state.isLock = true
      setStore({
        name: 'isLock',
        content: state.isLock,
        type: 'session'
      })
    },
```

####  ( 4 )  在路由里面判断vuex里面的isLock

```js
 if (store.getters.isLock && to.path !== lockPage) {
      next({
        path: lockPage
      })
      NProgress.done()
```