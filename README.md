# custom-translate
custom-translate is a simple module for translating certain words or letters in a string with other words or letters you provide. Usage is simple:

#### wordTrans
```js
const translator = require('custom-translate');

const text = 'I have a cow that goes moo.';
const dictionary = {
	"cow": "cat",
	"moo": "meow"
};

translator.wordTrans(text, dictionary);
```
Output will be:
`I have a cat that goes meow.`

`wordTrans` automatically ignores casing, all instances of the word, regardless of case, will be replaced.

#### letterTrans
```js
const translator = require('custom-translate');

const text = 'I like cheese.';
const dictionary = {
	"c": "!",
	"i": "5"
};

translator.letterTrans(text, dictionary);
```

Output will be:
`S like !heese`

Unlike `wordTrans`, `letterTrans` does not ignore casing by default.

When using `letterTrans`, you can also optionally specify what to join the string back together with. This defaults to `''`.

```js
translator.letterTrans(text, dictionary, ' ');
```