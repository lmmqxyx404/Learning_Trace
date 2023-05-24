# 注意，script标签引入资源的时候，顺序非常重要

# 数组原型的遍历方法的三大特征
1. 是否对原数组有影响
2. 中途能否中断
3. 是否有返回值组成新数组

# 当有不懂的DOM或者BOM API要查询时，首先考虑MDN
## 1. You can set the clipboard to read or write the content.
search the MDN

# BOM
## 1. listen to fresh or close the pge event.
```
window.addEventListener('beforeunload', ()=>{
    window.navigator.sendBeacon('http://localhost:8081',JSON.stringify({"data":'bye!'}))
})
```

# Object
## Object.defineProperty(obj, prop, descriptor)
Property descriptors present in objects come in two main flavors:
data descriptors and accessor descriptors

### descriptor
writable
configurable
enumerable
value

## about 

# GC (garbage collect)
There are two mainly ways.
## Reference-counting

## Mark-and-sweep algorithm