# Kamby
Kamby Programming Language is a Lisp dialect with some conventions to create a lange more intuitive and compact.

## Lisp? But it doesn't look like
Internaly the implementation follows some basic concepts like S-expressions and car/cdr as any Lisp language.
Kamby has some conventions to make the syntax more friendly:
- Anything starting with a new line and finishing in end of line is considered an expression
- An item formed by 2 or less punctuation characters, will create an expression formed by (punct previous next). Ex.: 2 + 2 => (+ 2 2) ... something == anything => (== something anything)
- Blocks will be evaluated if is the first item of expression.

### Actions
- def key 'value' (Append 'key' in stack)
- key := 'value'  (Append 'key' in stack - syntax sugar for 'def')
- key = 'value'   (Edit last 'key' in stack)
- del key         (Remove last 'key' from stack)
- if (condition) { 'first' } (else_condition) { 'second' }
- while {condition} { 'Do this' }
- for {initialization} {condition} {increment} { 'Do this' }
- puts key 'or text'

### Operators
```
+ - * /
&& || == != >= <= > <
+= -=
```

## Known issues / TODO
- VM / Bytecode
- Change list items without keys (by index)
- Delete first item from object (using call context)

## License
MIT
