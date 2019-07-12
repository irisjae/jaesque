# The Jayesque Style

### *this is javascript*

## Fantastical bits
- Put each statement on its own line(s)
- Don't add `;` at the end of your statements
- If your statement is impure; mark it with a `;` in the front!
    - _Why?_ Javascript expressions always play well with Automatic Semi-colon Insertion. It is the prefixes in statements which potentially cause problems (e.g. `hello () \n [] .forEach (...)` on the next line is confused with `hello () [] .forEach`, which gives errors like `Unexpected token ]`). So we can safely escape statements, and only statements! And the only statements that are not 'impure' are variable assignments, which also respect Automatic Semi-colon Insertion.
    - e.g. No `console .log (x)`. It's impure, so `;console .log (x)`
- If your function is impure; make it `{;}`!
    - e.g. No `x => console .log (x)`. It's impure, so `x => {;console .log (x)}`
- Don't use `this`, use `require ('thiss')`
- No function statements
- Make your functions generic. Use `x`, `y`, `z`, `t`, `u`, `v`, `w`, q`, `r`, s`, ... for the parameters (Unless they are really specific, obviously unreusable)
   - _What is this?_ basically the 'ABC' song triplets/quadruplets/quintuplets
- Add spaces between tokens
- Avoid suffixes smaller than the prefix. It is undiscoverable.
    - e.g. This is bad. The significant call operator `()` is undiscoverable! Is this a function or the value?

```
var result = (x => {
   ...
   var computation = step_1 + step_2
   return result
}) ()
```
- Mark your sentence with the one significant prefix (if its in a phrase), hide the rest on the previous line. Encourage the leading member to follow the `[` or `(`
    - e.g. (the prefix here is `o`)

```
var result = Oo (something,
  o (x => x .parent),
  o (R .reduce ((sum, x) => sum + x, 0)))
```
   or
```
var q = [ document .querySelector ('fire')
  , document .querySelector ('earth')
  , document .querySelector ('air')
  , document .querySelector ('water') ]
```
- Collapse the `)`s, `}`s, etc.

## Aesthetic bits
- Use tabs
- Use single quotes `''`
- Use snake_case (since hyphen-case does not work)
- Do add a space before `.`. The property is a word!
    - e.g. `document .body .style .backgroundImage = 'url(doge.png)'`
- Use arrow functions, and only arrow functions!
- Arrow functions with one parameter, take no brackets
- Curry!
- Use `var`, and `var` only
- Try to not mutate `var`s
- No class statements
- Write your unfinished code as `...`
