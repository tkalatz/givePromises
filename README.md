# givePromises
Javascript Asynchronous Programming and Promises, Never give promises ;)
Javascript promises can blow your mind... but can make things better - as promises always

```javascript
const givePromise = (gift) => {
  return new Promise( (r,f) => {
   r(gift);
   console.log("Promise Given for a new Gift!");
  })
}

const doYouRemember = (thought,seconds) => {
  return new Promise( (r,f) => {
  console.log(thought+" trying to remember...");
  setTimeout( function() {
    r("Promises are usually forgotten!"); 
	console.log(seconds+" seconds is too much thinking, for what you have promised and you cannot rethink.");
  }, seconds*1000) 
  })
} 

givePromise("A gift").then( gift => {
  return gift+" was ";
 })
 .then ( (result) => {
  return result+"promised but ";
 })
 .then( (thought) => doYouRemember(thought,3) )
 .then( result => {
	 console.log(result);
});
```
