# The effect
it can use ajax to load the part of the wep page.
For example pull down the H5 page.

## The application scenario
1. pull down to update the page
2. enter the login form and judge the content
3. search engin provides us more intelligent tips

# The sample
## 1. create the object 
  ```
  let xhr = new XmlHttpRequest()
  ```
## 2. set the http methods and the destination
  ```
  xhr.open('get','http://www.example.com') // This is the get method.
  ```
## 3. send the request
   ``` 
   xhr.send()
   ```
## 4. get the response from the server and render the data
   ``` 
   xhr.onload=function(){
     console.log(xhr.responseText);
   }
   ```