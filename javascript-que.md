# Map method
    - map() returns new array from existing array by applying function on each element of first/existing array.
# filter method
    - filter() returns those elements from array which fullfilled the criteria or condition.
# reduce method
    - reduce() reduces the array of values down to just a single value

    /*
Requirment 

Develop a function which calculate total salary of each employee and out as object which contain key as emp name and value as total salary 
*/


// Employee list
const emp = [{ name: 'a', sal: 200 }, { name: 'b', sal: 200 }, { name: 'a', sal: 500 }, { name: 'b', sal: 200 }, { name: 'c', sal: 300 }]


const result = emp.map((item)=>{
let obj = 
       
})

console.log(result)
/*
Output:
{
	a: 700,
  b: 400,
  c: 300
}



Explanation 
here emp with name a have 2 entries 
{ name: 'a', sal: 200 }
{ name: 'a', sal: 500 }

so a: 700

emp with name b have 2 entries
{ name: 'b', sal: 200 }
{ name: 'b', sal: 200 }

so b: 400

emp with name c have 1 entry
{ name: 'c', sal: 300 }

so c: 300
*/