# ChardScript Comments

Comments can be used to explain ChardScript code, make the code more readable and prevent execution when testing code.

## Creating a Comment

Comments starts with a <mark style="color:red;">`#`</mark>, and ChardScript will ignore them:

#### Example

{% code lineNumbers="true" %}
```renpy
# This is a comment
echo("Hello World!")
```
{% endcode %}

Comments can be placed at the end of a line, and ChardScript will ignore the rest of the line:

#### Example

{% code lineNumbers="true" %}
```renpy
echo("Hello World!") # This is a comment
```
{% endcode %}

A comment does not have to be text that explains the code, it can also be used to prevent ChardScript from executing code:

#### Example

{% code lineNumbers="true" %}
```renpy
# echo("Hello World!")
echo("Comment will not work!")
```
{% endcode %}

## Multi Line Comments

ChardScript does not really have a syntax for multi line comments.

To add a multiline comment you could insert a <mark style="color:red;">`#`</mark> for each line:

#### Example

{% code lineNumbers="true" %}
```renpy
# This is a comment
# written in
# more than just one line
echo("Hello, World!")
```
{% endcode %}
