# Interview : reverse-letters-in-words-of-sentence

Given a string, reverse the letters of the words in the sentence, but excluding the first letter of every word.

## 18-Apr-2024

```js
function reverseStr(str:string): string {
  let newStr = "";
  for (let i = str.length - 1; i >= 0; i--) {
    newStr += str[i];
  }
  return newStr;
}

function reverseLettersInWords(str: string) {
  const words = str.split(" ");
  const reverseWords = words.map(x => {
    return x.length > 1 ? x[0] + reverseStr(x.substring(1)) : x;
  });
  return reverseWords.join(" ");
}

```

Time: ****()

Memory: ****()
