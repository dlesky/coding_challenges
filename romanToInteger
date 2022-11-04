//converts roman numerals into numbers. leetcode challenge. 
//my very naive implementation below involved hardcoding the subtraction cases and uses splice to parse the array

let map =  {I:1, V:5, X:10, L:50, C:100, D:500, M:1000}

const romanToInt = function(s) {
    [parsedStr,intValue]=manageTuples(Array.from(s)); //process any tuples that involve subtraction and return a parsed string with associated value of the subtraction tuples 
    return final(parsedStr,intValue); //process remaining characters 
};

function final(str,count) {
  let finalCount = count;
  for (item of str) {finalCount += map[item]}
  return finalCount;
}

function manageTuples(arr) {
  let counter = 0;
  for (let i=0; i<arr.length; i++) {
    let tuple = arr.slice(i,i+2).join("")
    if(helper(tuple)) {
      arr.splice(i,2);
      i-=2;
      counter += helper(tuple);
    }
  }
  return [arr,counter]
}

function helper(deuce) {
  if (deuce==='IV') {return 4}
  else if (deuce==='IX') {return 9} 
  else if (deuce==='XL') {return 40}
  else if (deuce==='XC') {return 90}
  else if (deuce==='CD') {return 400}
  else if (deuce==='CM') {return 900}
  else {return null} 
}

//inspired by a solution from jeantimex:
const map = new Map([['I', 1], ['V', 5], ['X', 10], ['L', 50], ['C', 100], ['D', 500], ['M', 1000]]);

const romanToInt = s => {
  n = Array.from(s).map(x=>map.get(x)) //learned to use map.get() method
  let i = n.length - 1;
  let result = n[i];
  while (i > 0) {
    if (n[i-1] >= n[i]) {result+=n[i-1]} else {result-=n[i-1]}
    i--;
  }
  return result;
};














