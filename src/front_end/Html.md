<!--
 * @Author: Lmmqxyx
 * @Date: 2022-02-10 13:47:27
 * @LastEditors: Please set LastEditors
 * @LastEditTime: 2022-05-17 16:00:34
 * @FilePath: \Learning_Note\Html.md
 * @Description: 
-->
# render the data
it is better to choose class selector when data needs to be rendered.
需要数据渲染的时候，注意选择标签尽量用类名去选择。
然后用展开运算符指定一个根元素

# use tags
html5 tags is in priority

# some attributue should be deprecated
The detail should be showed in MDN.
It is deprecated to use summary in table

# script tag
please remember the content of script is just JS.
it is not a JS function.

# attribute and property
The attribute belongs to HTML standard
The property belongs to Dom standard

## Once you get an element
Attribute is a child key of the property of an element.

## data flow
property can be modified once attribute is modified
attribute不会同步property上的值；
attribute和property之间的数据绑定是单向的，attribute->property；
更改property和attribute上的任意值，都会将更新反映到HTML页面中；
