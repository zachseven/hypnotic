# hypnotIC

## *"I see what you meant."*

A programming language that doesn't scream at you. It understands.

---

## Philosophy

- No indentation requirements
- Phonetic shortcuts
- Forgiving syntax
- IC = "I see" = the language understands

---

## The Dictionary

| Normal | hypnotIC | Notes |
|--------|----------|-------|
| print | `*` | splat it out |
| input | `PV` | 5th grade humor |
| for | `4` | sounds like "for" |
| in | `n` | sounds like "in" |
| to | `2` | sounds like "to" |
| at | `@` | sounds like "at" |
| be | `b` | sounds like "be" |
| are | `r` | sounds like "are" |
| you | `u` | sounds like "you" |
| and | `&` | |
| or | `or` / `RHO` | normal / nerdy |
| not | `-` | negation |
| while | `wyl` | |
| if | `?` | questioning |
| else | `Ls` | sounds like "else" |
| elif | `file` | elif backwards - evil |
| function | `fun` | it should be |
| return | `re:` | like email reply |
| lambda | `\` | quick function |
| true | `t` | or `1` |
| false | `f` | or `0` |
| import | `->` | pull it in |
| comment | `fuck` | ignore this |
| array | `rayz` | sounds like "arrays" |
| null/none | `N^0` | nothing to the zero |
| break | `x` | cross it out |
| continue | `-->` | keep going |
| try | `hard` | try hard |
| catch | `C` | catch |
| self | `ego` | the object's ego |
| len/length | `"` | inches |
| == (equals) | `iz` | sounds like "is" |
| != (not equals) | `aint` | ain't |
| append | `up` | push up |
| pop | `!!!` | explosive |
| exponent | `^` | power |
| modulo | `mold` | remainder |
| dict | `{}` | keep it |
| end block | `IC` | "I see" |

---

## Syntax

### Variables
```
name = "Zach"
age = 25
active = t
nothing = N^0
```

### Print
```
* "Hello, world!"
* name
* 2 + 2
```

### Input
```
name = PV "What's ur name?"
age = PV "How old r u?"
```

### Comments
```
fuck this line is ignored
fuck so is this one
* "this runs"
```

### Conditionals
```
? age > 21
* "welcome"
file age > 18
* "almost"
Ls
* "nope"
IC
```

### Loops

**For loop:**
```
4 i n 10
* i
IC
```

**While loop:**
```
x = 10
wyl x > 0
* x
x = x - 1
IC
```

**Break and continue:**
```
4 i n 100
? i iz 5
x
IC
? i iz 3
-->
IC
* i
IC
```

### Functions
```
fun greet name
* "Hello, " + name
IC

greet "Zach"
```

**With return:**
```
fun add a b
re: a + b
IC

result = add 3 4
* result
```

**Lambda (quick function):**
```
double = \ x : x * 2
* double 5
fuck output: 10
```

### Arrays
```
nums = [1 2 3 4 5]

fuck loop through
4 n n nums
* n
IC

fuck length
* nums"
fuck output: 5

fuck append
nums up 6

fuck pop
last = nums!!!
```

### Dictionaries
```
user = {name: "Zach", age: 25, active: t}
* user.name
* user.age
```

### Classes
```
Dog
name = ""
age = 0

fun bark
* "woof!"
IC

fun introduce
* "I'm " + ego.name
IC
IC

mydog = Dog
mydog.name = "Rex"
mydog.age = 3
mydog.bark
mydog.introduce
```

**Inheritance:**
```
Animal
alive = t
IC

Dog < Animal
fun bark
* "woof"
IC
IC
```

### Error Handling
```
hard
x = 10 / 0
C
* "can't divide by zero"
IC
```

### Imports
```
-> math
-> myfile

* math.sqrt 16
```

### Operators

**Math:**
```
* 2 + 2      fuck 4
* 10 - 3     fuck 7
* 4 * 5      fuck 20
* 20 / 4     fuck 5
* 2 ^ 10     fuck 1024
* 10 mold 3  fuck 1
```

**Comparison:**
```
? a iz b      fuck a == b
? a aint b    fuck a != b
? a > b       fuck greater than
? a < b       fuck less than
? a >= b      fuck greater or equal
? a <= b      fuck less or equal
```

**Logical:**
```
? a & b       fuck a and b
? a or b      fuck a or b (also: RHO)
? -a          fuck not a
```

---

## Example Programs

### Hello World
```
* "Hello, world!"
```

### FizzBuzz
```
4 i n 100
? i mold 15 iz 0
* "FizzBuzz"
file i mold 3 iz 0
* "Fizz"
file i mold 5 iz 0
* "Buzz"
Ls
* i
IC
IC
```

### Fibonacci
```
fun fib n
? n <= 1
re: n
IC
re: fib(n-1) + fib(n-2)
IC

4 i n 10
* fib i
IC
```

### Guessing Game
```
-> random
secret = random.randint 1 100
guess = 0

* "Guess a number 1-100"

wyl guess aint secret
guess = PV "ur guess: "
guess = int guess

? guess < secret
* "2 low"
file guess > secret
* "2 high"
Ls
* "u got it!"
IC
IC
```

### Slot Machine
```
-> random

* "=== SLOT MACHINE ==="
* "Pull the lever..."

a = random.randint 1 6
b = random.randint 1 6
c = random.randint 1 6

* a + " | " + b + " | " + c

? a iz b & b iz c
* "JACKPOT! u win!"
file a iz b or b iz c or a iz c
* "2 match. small win."
Ls
* "u lose. life goes on."
IC
```

---

## Design Principles

1. **IC sees your intent** - The parser tries to understand what you meant
2. **No indentation fascism** - Use `IC` to close blocks
3. **Phonetic shortcuts** - Type how you think
4. **Forgiving** - Warnings, not errors when possible
5. **Fun** - Programming should be `fun`, not frustrating

---

## File Extension

`.ic`

---

## Taglines

- "hypnotIC - I see what you meant"
- "hypnotIC - code that understands you"
- "hypnotIC - stop fighting your compiler"
- "hypnotIC - I C what you did there"

---

*"Find what you love and let it kill you."*
— hypnotIC
