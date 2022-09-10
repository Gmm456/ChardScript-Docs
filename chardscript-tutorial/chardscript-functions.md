# ChardScript Functions

A function is a block of code which only runs when it is called.

You can pass data, known as parameters, into a function.

A function can return data as a result.

## Creating a Function

In ChardScript a function is defined using the <mark style="color:red;">`group`</mark> keyword:

#### Example

{% code lineNumbers="true" %}
```renpy
group my_function()
  echo("Hello from a function")
end
```
{% endcode %}

## Short Hand Group

You can define a new function with only 1 line of code:

#### Example

{% code lineNumbers="true" %}
```renpy
group my_function() -> echo("Hello from a function")
```
{% endcode %}

## Calling a Function

To call a function, use the function name followed by parenthesis:

#### Example

{% code lineNumbers="true" %}
```renpy
group my_function()
  echo("Hello from a function")
end

my_function()
```
{% endcode %}

## Arguments

Information can be passed into functions as arguments.

Arguments are specified after the function name, inside the parentheses. You can add as many arguments as you want, just separate them with a comma.

The following example has a function with one argument (fname). When the function is called, we pass along a first name, which is used inside the function to print the full name:

#### Example

{% code lineNumbers="true" %}
```renpy
def my_function(fname):
  print("Hello " + fname)

my_function("Friend")
my_function("World")
my_function("Man")
```
{% endcode %}

## Parameters or Arguments?

The terms _parameter_ and _argument_ can be used for the same thing: information that are passed into a function.

{% hint style="info" %}
From a function's perspective:

A parameter is the variable listed inside the parentheses in the function definition.

An argument is the value that is sent to the function when it is called.
{% endhint %}

## Number of Arguments

By default, a function must be called with the correct number of arguments. Meaning that if your function expects 2 arguments, you have to call the function with 2 arguments, not more, and not less.

#### Example

This function expects 2 arguments, and gets 2 arguments:

{% code lineNumbers="true" %}
```renpy
group my_function(fname,lname)
  echo(fname + " " + lname)
end

my_function("Emil", "Refsnes")
```
{% endcode %}

If you try to call the function with 1 or 3 arguments, you will get an error:

#### Example

This function expects 2 arguments, but gets only 1:

{% code lineNumbers="true" %}
```renpy
group my_function(fname,lname)
  echo(fname + " " + lname)
end

my_function("Emil")
```
{% endcode %}

## Return Values

To let a function return a value, use the <mark style="color:red;">`give`</mark> statement:

#### Example

{% code lineNumbers="true" %}
```renpy
group my_function(x)
  give 5 * x
end

echo(my_function(3))
echo(my_function(5))
echo(my_function(9))
```
{% endcode %}

## Recursion

ChardScript also accepts function recursion, which means a defined function can call itself.

Recursion is a common mathematical and programming concept. It means that a function calls itself. This has the benefit of meaning that you can loop through data to reach a result.

The developer should be very careful with recursion as it can be quite easy to slip into writing a function which never terminates, or one that uses excess amounts of memory or processor power. However, when written correctly recursion can be a very efficient and mathematically-elegant approach to programming.

In this example, <mark style="color:red;">`tri_recursion()`</mark> is a function that we have defined to call itself ("recurse"). We use the <mark style="color:red;">`k`</mark> variable as the data, which decrements (<mark style="color:red;">`-1`</mark>) every time we recurse. The recursion ends when the condition is not greater than 0 (i.e. when it is 0).

To a new developer it can take some time to work out how exactly this works, best way to find out is by testing and modifying it.

#### Example

{% code lineNumbers="true" %}
```renpy
group tri_recursion(k)
  if k > 0 then
    call result = k + tri_recursion(k - 1)
    echo(result)
  else
    call result = 0
  end
  give result
end

echo("Recursion Example Results")
tri_recursion(6)
```
{% endcode %}
