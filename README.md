# Flower-project

## Git problem

- git 出现"Updates were rejected because the tip of your current branch is behind"的问题

1. 主要是因为远程仓库与本地仓库冲突的问题
2. 使用 git pull 将仓库一致后再 push

- 当 push 时出现"could not read from remote respository.please make sure you have the correct access rights and the respository exists"错误时

1. 主要是没有设置密钥
2. 在.git 文件处 Git bash here 输入命令"ssh-keygen -t rsa -C "2017118621@qq.com",一路 enter 再输入"cat ~/.ssh/id_rsa.pub"得到密钥再从 github 上 new ssh。

- 当 push 时出现 Everything up-to-date 但远程仓库并未修改的解决策略

1. 新建一个分支 new
2. 在这个分支上 new 添加修改后的文件 git add ,git commit -m
3. 切换到 master 分支，合并分支 git merge new
4. 删除 new 分支

## VUE problem

- el，template，render 属性优先性

1. 在进行 DOM 树的渲染时，render 渲染函数的优先级最高，template 次之且需编译成渲染函数，而挂载点 el 属性对应的元素若存在，则在前两者均不存在时，其 outerHTML 才会用于编译与渲染。
2. data 对象里即是 el 属性获取挂载元素的 outerHTML
   方式渲染

```
el: '.vapp-1',
  data: {
    info: '这是通过el属性获取挂载元素outerHTML方式渲染。'
  }
```

3. template 方式渲染,将 template 模板编译生成渲染函数，然后再渲染 DOM 树

```
template: '<div>这是template属性模板渲染</div>'
```

4. render 方式渲染,不需要编译.Vue 构造函数将直接使用渲染函数渲染 DOM 树

```
render (h) {
    return h('div', this.hello)
  }
```

- vue 插槽

1. 插槽可以是任意内容，子组件挖个坑，父组件往里面放东西。
2. 作用: 使组件标签内的内容起作用

```
Vue.component('child-component',{
        template:`
            <div>
            Hello,World!
            <slot></slot>
            </div>
        `
})
<child-component>你好</child-component>
```

3. 具名插槽与默认插槽

```
<div id="app">
    <child-component>
        <template slot="girl">
            漂亮、美丽、购物、逛街
        </template>
        <template slot="boy">
            帅气、才实
        </template>
        <div>
            我是一类人，
            我是默认的插槽
        </div>
    </child-component>
</div>
```

4. 作用域插槽
5. element carousel 插件的图片描述需要用 url 否则显示不出图片
