### 1.引入

```javascript
"usingComponents": {
    "rjx-uploader": "../../components/uploader/index"
}
```



### 2. 参数

| 字段      | 说明                                                         | 类型    | 是否必填 | 默认值  |
| --------- | ------------------------------------------------------------ | ------- | -------- | ------- |
| list      | 上传文件的数组                                               | Array   | 是       |         |
| type      | 默认上传类型                                                 | String  | 否       | 'image' |
| canSwitch | 是否可以切换上传类型                                         | Boolean | 否       | true    |
| must      | 是否显示必传的*号                                            | Boolean | 否       | true    |
| count     | 最多可以上传几张图片                                         | Number  | 否       | 1       |
| multiple  | 上传时是否可以多选                                           | Boolean | 否       | true    |
| refresh   | 在页面更新组件（一般用于文件的回显）<br />组件监听refresh的值，当refresh更新时组件会一起更新 | 自定义  | 否       | 自定义  |



### 3. 方法

| 名字     | 说明                                                         |
| -------- | ------------------------------------------------------------ |
| uploaded | 当任一个文件更新（新增/删除）时，触发该函数<br />与refresh对应，是组件更新页面 |



### 4. 使用示例

```javascript
data: {
    list: [
        {
          name: '营业执照',
          canSwitch: false
        },
        {
          name: '营业执照',
          type: 'file'
        }
    ]
},

licenseUpdated(e) {
    console.log(e)
    ...
}
```

```javascript
<rjx-uploader
    list='{{list}}'
    bind:uploaded='licenseUpdated'
/>
```



