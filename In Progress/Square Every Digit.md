function squareDigits(num){
  let string = num.toString().split('');
  string = string.map(x => {
    let y = x*x;
    return y.toString();
  });
  string = string.join('');
  num = Number.parseInt(string, 10);
  return num;
}

Welcome. In this kata, you are asked to square every digit of a number and concatenate them.

For example, if we run 9119 through the function, 811181 will come out, because 92 is 81 and 12 is 1.

Note: The function accepts an integer and returns an integer

Note from me: make sure to explain my steps using differently named vars;

function squareDigits(num){
  return Number(num.toString().split('').map(x => (x*x).toString()).join(''));
}

Cite documentation because that makes this easy