## Loops and operators in Javascript

### Comparison operators
- `==` is equal to
- `!=` is not equal to
- `===` strict equal to
- `!==` strict not equal to
- `>` Greater than `>=` Greater than or equal
- `<` Less than and `<=` Less than or equal


### Logical operators
- `&&` Logical And
- `||` Logical OR
- `!` Logical Not
> Logical Operators are evaluated *left* to *right*.
If the first condition can provide enough information to get the answer, then there is no need to evaluate the second condtion.

### Loops
Loops check a condition if it returns true, a code block will run untill it returns false.

#### for loop
```javascript
for (var i=0; i<number,i++){
    statements;
}
```
#### while loop
```javascript
while(i<number){
    statements;
    i++;
}
```