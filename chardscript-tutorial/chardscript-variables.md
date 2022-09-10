# ChardScript Variables

## Variables

Variables are containers for storing data values.

## Creating Variables

To declaring a variable, you need use <mark style="color:red;">`call`</mark> to creating a new variable.

A variable is created the moment you first assign a value to it.

#### Example

{% code lineNumbers="true" %}
```renpy
call x = 5
call y = "Hello World!"
echo(x)
echo(y)
```
{% endcode %}

Variables do not need to be declared with any particular _type_, and can even change type after they have been set.

#### Example

{% code lineNumbers="true" %}
```renpy
call x = 5              # x is number
call x = "Hello World!" # x is string now
echo(x)
```
{% endcode %}

## Single or Double Quotes?

String variables can be declared using only double quotes:

#### Example

{% code lineNumbers="true" %}
```renpy
# Do
call x = "Hi World!"
# Don't
call x = 'Hi World!'
```
{% endcode %}

## Case-Sensitive

Variable names are case-sensitive.

#### Example

{% code lineNumbers="true" %}
```renpy
call x = 5
call X = "Hello World!"
# X will not overwrite x
```
{% endcode %}
