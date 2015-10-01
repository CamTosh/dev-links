[back](README.md)

## js 

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
