# ToddLang Beta 1.0.2 Docs
Possibly the most shitty docs of all time.

## Variables
A variable is defined via `var`. Doing "a = 1" will not work, as it is missing the variable assignment keyword.   
Example: `var todd = "todd"`

## Booleans
Boolean statements, like true and false. True returns 1, false returns 0.   
Example: `var todd = false; var weiss = true;` 

## If Statements
If you have basic syntax knowledge this is going to be a breeze, basically just glorified lua. "if statement then do_something".   
Example: `if 1 == 1 then var todd = "todd"`   
Multi-line Example:
```
if 1 == 1 then
    var todd = "todd"
end
```

### Else and Elif
Called after and if statement, will function if requirements for the if statement aren't met. Elif is just if but will run if previous if statement's aren't ran.   
Example: `if 1 == 1 then var todd = true elif 2 == 2 then var todd = true else var todd = false`   
Multi-line Example:
```
if 1 == 1 then
    var todd = true
elif 2 == 2 then
    var todd = true
else
    var todd = false
end
```

### Not, and, or
They're all self-explanatory but I'll provide examples below.    
"Not" Example: `if not 1 == 2 then var todd = true`    
"And" Example: `if 1 == 1 and 2 == 2 then var todd = true`   
"Or" Example: `if 1 == 2 or 1 == 1 then var todd = true`   

## Functions
Use `public` to define a public function. Anything between the parenthesis are arguments to said function, and are only defined in the function after it's been called.

Single Line Example: `public add(x,y) -> var result = x + y; add(1,2)`
Multi Line Example:
```
public add(x,y)
    var result = x + y
end

add(1,2)
```

### Returning values with rustam
Great, you know functions now. But what about returning? To return, use `rustam` at the end of a function.   
Example: `public add(x,y) -> rustam x + y; three = add(1,2)`   
Multi Line Example:
```
public add(x,y)
    rustam x + y
end

three = add(1,2)
```

## Comments
Comments are a part of the code which contains a comment, or a note, which isn't executed and is there to be read. Comments in toddlang at the moment follow the Python comment syntax of #'s.   
Example:
```
# This code is for a subtract function!
public subtract(x,y)
    rustam x - y
end
```

## Loops

### For loops
its a fucking for loop i dont know what to tell you   
Example: `for i = 0 to 100 then var todd = i`   
Multi Line Example:
```
for i = 0 to 100 then # loops 100 times
    todd = i
end
```

#### Step
Basically every time a for loop iterates, its variable (usually `i`) goes up once. But! With step, you can change how much it increases.   
Example: `for i = 0 to 100 step 10 then var todd = i`   
Multi Line Example:
```
for i = 0 to 100 step 10 then # loops 10 times
    todd = i
end
```

### While Loops
Iterates while a statement is or isnt something.   
Example: `var todd = 0; while todd < 100 then var todd = todd + 1`   
Multi Line Example:
```
var todd = 0

while todd < 100 then
    var todd = todd + 1
end
```

## Continue and Break
`Continue` is pretty self explanatory, it continues.   
`Break` is too, it breaks a loop.   

"Break" Example: `while true then break; var todd = "wow loop broken"`   
"Continue" Example: `while true then continue`   
Multi Line  Example:
```
var todd = 0

while true then
    var todd = todd + 1
    if todd > 10000 then
        break
    else
        continue # super unnecessary but here for documentation purposes
    end
end
```

## Strings
strings are anything between quotes, like "this"!   

### string appending
use a + to append strings together.   
Example: `var todd = "Hello " + "World! "`

### string iteration
use a * to iterate a string   
Example: `var todd = "Hello World!" * 5`

## Lists
ok lists are literally just arrays lets get this part over quickly im tired of writing   
list example: `var list = ["foo","bar",69,420,true,false]`

### appending
appends item to list   
example: `append(list, "foobar")`

### popping
removes item from list. the number is the item's index. (pro tip, list indexes start at 0, so to remove the first item you'd do pop(list, 0).)   
example: `pop(list, 0)`

### extending
joins 2 lists together   
example: `extend(list, list2)`

### len
gets how many items are in the list 
example: `len(list)`

### inserting
inserts a item into a list at an index   
example: `insert(list, 0, "foobar")`

### indexing
fetch a item from a list via its index   
example: `index(list, 0)`

## types
types are stuff like strings, integers, booleans, etc.   

### strings
**str()** converts to a string   
example: `str(69)`   
**isstring()** checks if something is a string   
example: `isstring("hello world")`   

### numbers
isnumber() checks if something is a number (ints, floats, etc. works with all number types)   
example: `isnumber(3)`

### integers
int() converts to a integer   
example: `int("69")`

### floats
float() converts to a float   
example: `float("69.420")`

### booleans
literally just true and false we already went over this

### lists 
islist() checks if something is a list   
example: `islist([])`

### functions
isfunction() checks if something is a function   
example: `isfunction(toddsays)`

### bytes
bytes() converts to bytes   
COMING SOON

## Built In Functions
good job you made it to the less boring part!!!!   
   
### Toddsays
You know how some languages use `print()` as their stdout function? Well here at ToddLang we use `toddsays()`. Toddsays stdouts anything between the parenthesis, and returns 0.   
Example: `toddsays("Hello, world!")`   

### Toddreallysays
toddsays() but it returns the string stdout-ed   
Example: `toddreallysays("Hello, world!")`  

### Stdin
Really creative name, right? Captures stdin, or user input.   
Example: `toddsays("Whats your name?"); var name = stdin(); toddsays("Hello, " + name)`   
Multi Line Example:
```
toddsays("Whats your name?") 
var name = stdin()
toddsays("Hello, " + name)
```
### Intstdin
INSANELY creative name. stdin but converts to int. soon to be depracated due to int() probably.   
Example: `toddsays("Whats your age?"); var age = intstdin(); toddsays("2x your age is, " + str(age * 2))`   
Multi Line Example:
```
toddsays("Whats your age?")
var age = intstdin()
toddsays("2x your age is, " + str(age * 2))
```

### Clear
clears your shell   
example: `clear()`

### Istype
we went over the the istype functions (isnumber, isstring, etc) in the types catagory.   

### Shell
executes a command in shell and returns the stdout.   
example: `var message = shell("echo hello world")`

### Local Shell
executes a command in the the current shell window and returns null.   
example: `lcshell("color a")`


### runFile
executes a toddlang file. sunsetted by use() but not yet deprecated.      
example: `runFile("main.todd")`

### use
imports a library.   
example: `use("types.todd")`

## libraries
Libraries are basically *add-ons* to toddlang, adding custom functions into your namespace.   
Installed libraries are in `%localappdata%/toddlang/toddlang(current version)/libs`.   
You can also use toddlang files that are in the same directory as libraries.
