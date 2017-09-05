# es-config
es-fonfig for docave [npm es-config-docave](https://www.npmjs.com/package/eslint-config-docave)

之前打算使用Airbnb config 但是Airbnb 比较严格，结果就导致当项目的代码一build 的时候满屏都是错，
然后我的解决方式就是我观察这些报错，然后人工鉴定注掉释我感觉得不必要的部分
，因为当时觉得着些规范有些事我们应该学习的。

现在想使用新的解决方案：即只使用 eslint：recommended 加上开会商定后的规则。

## 安装
```bash
$ npm i eslint-config-docave
```

## 使用方法

### package.json
```json
{
  "name": "xxxxx",
  "version": "x.x.x",

  "eslintConfig": {
    "extends": "docave",
  }

}
```
### .eslintrc.js
```js
module.exports = {
  extends: 'docave',
};
```
### .eslintrc
```js
{
    "extends": "docave" 
}
```
### 检查的规则
eslint:recommended 加上下表所列规则
```js
 "rules": {
        "no-console": "off",
        "react/prefer-es6-class": "error",
        // Enforce stateless React Components to be written as a pure function 
        "react/prefer-stateless-function": "error",
        //扩展名: React模块使用 .jsx 扩展名.  - 文件名: 文件名使用帕斯卡命名. 如, ReservationCard.jsx.  - 引用命名: React模块名使用帕斯卡命名，实例使用骆驼式命名
        "react/jsx-pascal-case": "error",
        // 如果模块有多行的属性， 关闭标签时新建一行.
        "react/jsx-closing-bracket-location": "error",
        // 对于JSX属性值总是使用双引号("), 其他均使用单引号(')
        "jsx-quotes": "error",
        // 总是在自动关闭的标签前加一个空格，正常情况下也不需要换行 good <Foo />
        "no-multi-spaces": "error",
        // 不要在JSX {} 引用括号里两边加空格.
        "react/jsx-tag-spacing": "error",
        "react/jsx-curly-spacing": "error",
        // <img> 标签总是添加 alt 属性. 如果图片以presentation(感觉是以类似PPT方式显示?)方式显示，alt 可为空
        "jsx-a11y/alt-text": "error",
        //  不要在 alt 值里使用如 "image", "photo", or "picture"包括图片含义这样的词， 中文也一样.
        "jsx-a11y/img-redundant-alt": "error",
        // 使用有效正确的 aria role属性值 ARIA roles
        "jsx-a11y/aria-role": "error",
        // 不要在标签上使用 accessKey 属性. 
        "jsx-a11y/no-access-key": "error",
        // 总是在Refs里使用回调函数. 
        "react/no-string-refs": "error",
        // 将多行的JSX标签写在 ()里
        "react/jsx-wrap-multilines": "error",
        // 对于没有子元素的标签来说总是自己关闭标签.
        "react/self-closing-comp": "error",
        // 当在 render() 里使用事件处理方法时，提前在构造函数里把 this 绑定上去
        "react/jsx-no-bind": "error",
        // 在 render 方法中总是确保 return 返回值.
        "react/require-render-return": "error"
    }
```    
