# call-method
const apple={
brand:"apple",
model:"iphone14",
info :function(mon,year){
console.log(`${this.brand},${this model was released on ${mon}, ${year}`);
}
};

const samsung={
brand: "samsung",
brand:"j11",
}

const printInfo = apple.info;
printInfo.call(samsung,'feb',2023)
printInfo.call(apple,'sept',2043)

// it is same as call method only the only difference is apply doesnt receive list of arugments ,it will take arugment from an array 

// console.log(--apply--);
const arr1 = ['feb' ,2023]
const arr2 = ['sept' , 2043]
printInfo.apply(samsung,arr1);
printInfo.apply(apple,arr2);

just like call method bind also allows to set manllay set this keyword for any function call , here it doesnt call immediatelty  and returns a new keyword 

// console.log(--bind--);
const printAppleInfo= printInfo.bind(apple);
printAppleInfo('sept',2023)
printAppleInfo('oct',2034)
