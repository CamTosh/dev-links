## js

### async
- history : blogs.msdn.com/b/eternalcoding/archive/2015/09/30/javascript-goes-to-asynchronous-city.aspx

### books
- js allonge : https://leanpub.com/javascriptallongesix/read#leanpub-auto-about-javascript-allong

### composition
- mpjme over inheritance vid : https://www.youtube.com/watch?v=wfMtDGfHWpA
- mpjme factory functions js : https://www.youtube.com/watch?v=ImwrezYhw4w&annotation_id=eab57fc0-790e-4e8e-89fd-5ab7fd16344e&src_vid=wfMtDGfHWpA&feature=cards

### libs
- eshint : www.smashingmagazine.com/2015/09/eslint-the-next-generation-javascript-linter/

### functional
- 10 things stop rewriting/lodash : http://colintoh.com/blog/lodash-10-javascript-utility-functions-stop-rewriting

### inheritance
- simple challenge to fans : https://medium.com/javascript-scene/a-simple-challenge-to-classical-inheritance-fans-e78c2cf5eead
- common misconceptions : https://medium.com/javascript-scene/common-misconceptions-about-inheritance-in-javascript-d5d9bab29b0a

### info
- creating an open source lib : https://egghead.io/series/how-to-write-an-open-source-javascript-library  
- js engines for idiots : developer.telerik.com/featured/a-guide-to-javascript-engines-for-idiots/           
- 10 interview questions : https://medium.com/javascript-scene/10-interview-questions-every-javascript-developer-should-know-6fa6bdf5ad95

### groups
- jskicks : https://javascriptkicks.com/

### promises
- promisees : http://bevacqua.github.io/promisees/                                                           
- awesome promises : https://github.com/wbinnssmith/awesome-promises                                         

### stamps
- spec : https://github.com/stampit-org/stamp-specification
- react-stamp : https://github.com/stampit-org/react-stamp
- stampit : https://github.com/stampit-org/stampit
- introducing post : https://medium.com/javascript-scene/introducing-the-stamp-specification-77f8911c2fee

### style guides
- khan : https://github.com/Khan/style-guides/blob/master/style/javascript.md#dont-use-underscore
- air bnb : https://github.com/airbnb/javascript

### versioning
- 2ality : http://www.2ality.com/2015/11/tc39-process.html

### native functions
#### strings

substring
```
var s = 'string'

s.substring(2)
-> 'ring'

s.substring(2,2)
-> 'ri'

( first arg is index but based of 1, not 0 )
( second arg is length - full length if omitted )
( https://developer.mozilla.org/en-US/docs/Web/XPath/Functions/substringa)
```

-> "
### regex

split string on first whitespace:
```
var str = "part1 part2"

str.match(/^(\S+)\s(.*)/).slice(1)

str.replace(/\s+/, '\x01').split('\x01')

[str.replace(/\s.*/, ''), str.replace(/\S+\s/, '')]

reverse = function (s) { return s.split('').reverse().join('') }
reverse(str).split(/\s(?=\S+$)/).reverse().map(reverse)

re = /^\S+\s|.*/g;
[].concat.call(re.exec(str), re.exec(str))

-> ["part1", "part 2"]

: http://stackoverflow.com/questions/10272773/split-string-on-the-first-white-space-occurence
```
