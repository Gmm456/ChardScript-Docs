# ChardScript If...Else

## ChardScript Conditions and If statements

ChardScript supports the usual logical conditions from mathematics:

* Equals: <mark style="color:red;">`a == b`</mark>
* Not Equals: <mark style="color:red;">`a != b`</mark>
* Less than: <mark style="color:red;">`a < b`</mark>
* Less than or equal to: <mark style="color:red;">`a <= b`</mark>
* Greater than: <mark style="color:red;">`a > b`</mark>
* Greater than or equal to: <mark style="color:red;">`a >= b`</mark>

These conditions can be used in several ways, most commonly in "if statements" and loops.

An "if statement" is written by using the <mark style="color:red;">`if`</mark> keyword.

#### Example

If statement:

{% code lineNumbers="true" %}
```renpy
call a = 33
call b = 200
if b > a then
  echo("b is greater than a")
end
```
{% endcode %}

In this example we use two variables, <mark style="color:red;">`a`</mark> and <mark style="color:red;">`b`</mark>, which are used as part of the if statement to test whether <mark style="color:red;">`b`</mark> <mark style="color:red;"></mark><mark style="color:red;"></mark> is greater than <mark style="color:red;">`a`</mark>. As `a` is <mark style="color:red;">`33`</mark>, and b is <mark style="color:red;">`200`</mark>, we know that 200 is greater than 33, and so we print to screen that "b is greater than a".

## No end in If statement

We can not use end but also the code below the if statement will run under the if statement

#### Example

{% code lineNumbers="true" %}
```renpy
call a = 33
call b = 200
if b > a then
  echo("b is greater than a")
```
{% endcode %}

## Elseif

The <mark style="color:red;">`elseif`</mark> <mark style="color:red;"></mark><mark style="color:red;"></mark> keyword is a way of saying "if the previous conditions were not true, then try this condition".

#### Example

{% code lineNumbers="true" %}
```renpy
call a = 33
call b = 33
if b > a then
  echo("b is greater than a")
elseif a == b then
  echo("a and b are equal")
end
```
{% endcode %}

In this example <mark style="color:red;">`a`</mark> is equal to <mark style="color:red;">`b`</mark>, so the first condition is not true, but the <mark style="color:red;">`elseif`</mark> condition is true, so we print to screen that "a and b are equal".

## Else

The <mark style="color:red;">`else`</mark>keyword catches anything which isn't caught by the preceding conditions.

#### Example

{% code lineNumbers="true" %}
```renpy
call a = 200
call b = 33
if b > a then
  echo("b is greater than a")
elseif a == b then
  echo("a and b are equal")
else
  echo("a is greater than b")
end
```
{% endcode %}

In this example <mark style="color:red;">`a`</mark> is greater than <mark style="color:red;">`b`</mark>, so the first condition is not true, also the <mark style="color:red;">`elseif`</mark> condition is not true, so we go to the <mark style="color:red;">`else`</mark> condition and print to screen that "a is greater than b".

You can also have an <mark style="color:red;">`else`</mark> without the <mark style="color:red;">`elif`</mark>:

#### Example

{% code lineNumbers="true" %}
```renpy
call a = 200
call b = 33
if b > a then
  echo("b is greater than a")
else
  echo("b is not greater than a")
end
```
{% endcode %}

## Short Hand If

If you have only one statement to execute, you can put it on the same line as the if statement and can be without <mark style="color:red;">`end`</mark>.

#### Example

{% code lineNumbers="true" %}
```renpy
if a > b then echo("a is greater than b")
```
{% endcode %}

## Short Hand If ... Else

If you have only one statement to execute, one for if, and one for else, you can put it all on the same line:

#### Example

{% code lineNumbers="true" %}
```renpy
if a > b then echo("A") else echo("B")
```
{% endcode %}

{% hint style="info" %}
This technique is known as **Ternary Operators**, or **Conditional Expressions**.
{% endhint %}

## And

The <mark style="color:red;">`and`</mark> keyword is a logical operator, and is used to combine conditional statements:

#### Example

Test if <mark style="color:red;">`a`</mark> is greater than <mark style="color:red;">`b`</mark>, AND if <mark style="color:red;">`c`</mark> is greater than <mark style="color:red;">`a`</mark>:

{% code lineNumbers="true" %}
```renpy
call a = 200
call b = 33
call c = 500
if a > b and c > a then
  echo("Both conditions are True")
end
```
{% endcode %}

## Or

The <mark style="color:red;">`or`</mark> keyword is a logical operator, and is used to combine conditional statements:

#### Example

Test if <mark style="color:red;">`a`</mark> is greater than <mark style="color:red;">`b`</mark>, OR if <mark style="color:red;">`a`</mark> is greater than <mark style="color:red;">`c`</mark>:

{% code lineNumbers="true" %}
```renpy
call a = 200
call b = 33
call c = 500
if a > b or a > c then
  echo("At least one of the conditions is True")
end
```
{% endcode %}

## Nested If

You can have <mark style="color:red;">`if`</mark> statements inside <mark style="color:red;">`if`</mark> statements, this is called _nested_ <mark style="color:red;">`if`</mark> statements.

#### Example

{% code lineNumbers="true" %}
```renpy
call x = 41

if x > 10 then
  print("Above ten,")
  if x > 20 then
    print("and also above 20!")
  else
    print("but not above 20.")
  end
end
```
{% endcode %}
