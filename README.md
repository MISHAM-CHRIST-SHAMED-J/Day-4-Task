# Day-4-Task 
Compare two JSON have same property:

var obj1 = {
  name: 'person 1',
  age: 5
};
    
var obj2 = {
   age: 5,
   name: 'person 1'
};
    
let orderlist1=JSON.stringify(obj1);
let orderlist2=JSON.stringify(obj2);
if(orderlist1===orderlist2 && orderlist1.length===orderlist2.length)
{
console.log("True")
}
else
{
console.log("Flase")
}


Display country flag using rest API:

let url='https://restcountries.com/v2/all?fields=flag'
async function fetchText() {
    let response = await fetch(url);
              
   // console.log(response.status); // 200
   // console.log(response.statusText); // OK

    if (response.status === 200) {
        let data = await response.text();
        // handle data
        let dat=JSON.parse(data)
        for (i=1;i<=dat.length;i++)
       console.log(dat[i].flag)

    }
}

fetchText();



Display country Name,Region,Subregion,Population using rest API:

let url='https://restcountries.com/v2/all?fields=name,region,subregion,population'
async function fetchText() {
    let response = await fetch(url);
              
   // console.log(response.status); // 200
   // console.log(response.statusText); // OK

    if (response.status === 200) {
        let data = await response.text();
        // handle data
        let dat=JSON.parse(data)
        console.log(dat)

    }
}

fetchText();










