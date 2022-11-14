# lab8
Qno1 SOlution:
var addVal = function () {
  var counter = 0;
  return {
    add: function () {
      return (counter += 1);
    },
    reset: function () {
      return (counter = 0);
    },
  };
};

let count = addVal();
console.log('count', count);

console.log(count.add());
console.log(count.add());
console.log(count.reset());
console.log(count.add());

Qno 2 Solution:
Free variables are those variable which are not present in local variable and function
parameter
 Free variable of Qno1 is addValue and count,

Qno 3: Solution:
var make_adder = function (val) {
  var count = 0;
  return function () {
    return (count += val);
  };
};
var add5 = make_adder(5);
add5();
add5();
console.log(add5());

var add7 = make_adder(7);
add7();
add7();
console.log(add7());

Qno 4: Solution:
Using window['nameSpace'] = gVariable; => just a guess.

Qno 5: Solution:
class Employee{
Private name: string;
Private age: string;
Private salary: Number
public getName(): string{
return name;
}
Private getAge(): number {
return age;
}
Private getSalary(): number {
retrun salary;
}
Public setName():void {
this.name = name;
}
Public setAge() {
this.age = age;
}
Public method: setSalary(){
this.salary = salary;
}
Public increaseSalary(percentage) {
    this.salary = getSalary() + getSalary() * percentage;
}

// uses private getSalary()
Public method: incrementAge() {
this.age = getAge()+1;
}

Qno5: Soulution right way

 

 

const Employee = (function () {

  let name;

  let age;

  let salary;

  const getMethod = function () {

    return name;

  };

  const getAge = function () {

    return age;

  };

  const getSalary = function () {

    return salary;

  };

 

  const setName = function () {

    name = 'Kabita';

  };

 

  const setAge = function () {

    age = 23;

  };

 

  const setSalary = function () {

    salary = 3000;

    console.log('dd', salary);

  };

 

  const increaseSalary = function (percentage) {

    salary = getSalary() + (getSalary() * percentage) / 100;

    console.log(`Salary incerease to reach: ${salary}`);

  };

  const incrementAge = function () {

    age = getAge() + 1;

    console.log(`My age after increasing ${age}`);

  };

  const extension = function () {};

  return {

    setName,

    setAge,

    setSalary,

    increaseSalary,

    incrementAge,

    extension,

  };

})();

Qno 6: Solution:

Employee.extension = function () {

  let address;

  const setAddress = function (addr) {

    address = addr;

  };

  const getAddress = function () {

    return address;

  };

 

 

Extra: JSfiddle Solution:


var me = {
  first: 'Josh',
  last: 'Splinter',
  getFullName: function() {
    return this.first + ' ' + this.last;
  }
};

var you = {
  first: 'William',
  last: 'Smith'
};
const useCall = {
first: 'Nirajan',
last: 'Karki'
}
const useBind = {
first: 'Ttpl',
last: 'Stha'
}

console.log(me.getFullName.apply(you)); 
console.log(me.getFullName.call(useCall));
const getFull = me.getFullName.bind(useBind);
console.log(getFull());
