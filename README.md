# check-object-prop
提供模板，检查object的属性缺失或多余

```javascript
const checkObjectProp = function (template, obj) {
    Object.keys(template).forEach(key => {
        if (!obj.hasOwnProperty(key)) {
            console.warn('缺少字段', key, obj)
        }
    });

    Object.keys(obj).forEach(key => {
        if (!template.hasOwnProperty(key)) {
            console.warn('多余字段', key, obj)
        }
    })
}
```
