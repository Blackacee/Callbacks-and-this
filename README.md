# Callbacks-and-this
 
Often when using a callback you want access to a specific context.
function SomeClass(msg, elem) {
 this.msg = msg;
 elem.addEventListener('click', function() {
 console.log(this.msg); // <= will fail because "this" is undefined
 });
}
var s = new SomeClass("hello", someElement);
