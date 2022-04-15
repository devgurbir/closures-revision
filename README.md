# closures-revision

#### What are IIFE?

An IIFE (Immediately Invoked Function Expression) is a JavaScript function that runs as soon as it is defined. It is a design pattern which is also known as a Self-Executing Anonymous Function. 

Two common usecases of IIFEs are to avoid polluting the global namespace and in the module design pattern.

#### What is currying?

Currying is transforming functions that can be called as f(1, 2, 3) to f(1)(2)(3)

#### Write a program to throttle using closures

```
function throttler( callback, duration ){
  let flag = false;
  
  return function(){
      if(!flag){
        callback.apply(null, args)
        flag = true;
        setTimeout(() => { flag = false}, duration )
      }
   }
  
}
```


#### Explain some areas where you have seen currying being implemented in React / other libraries?

I have seen currying mostly used to implement functions where one parameter is fixed by passing it into the function used to create the function with the fixed parameter.
