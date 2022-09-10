# ChardScript While Loops

## ChardScript Loops

ChardScript has two primitive loop commands:

* <mark style="color:red;">`while`</mark> loops
* <mark style="color:red;">`for`</mark> loops

## The while Loop

With the <mark style="color:red;">`while`</mark> loop we can execute a set of statements as long as a condition is true.

#### Example

Print i as long as i is less than 6:

{% code lineNumbers="true" %}
```renpy
call i = 1
while i < 6 then
  echo(i)
  call i = i + 1
end
```
{% endcode %}

{% hint style="info" %}
**Note:** remember to increment i, or else the loop will continue forever.
{% endhint %}

## The stop Statement

With the <mark style="color:red;">`stop`</mark> statement we can stop the loop even if the while condition is true:

#### Example

Exit the loop when i is 3:

{% code lineNumbers="true" %}
```renpy
call i = 1
while i < 6 then
  echo(i)
  if i == 3 then
    stop
  end
  call i = i + 1
end
```
{% endcode %}

## The continue Statement

With the <mark style="color:red;">`continue`</mark> statement we can stop the current iteration, and continue with the next:

#### Example

Continue to the next iteration if i is 3:

{% code lineNumbers="true" %}
```renpy
call i = 0
while i < 6 then
  call i = i + 1
  if i == 3 then
    continue
  end
  echo(i)
end
```
{% endcode %}

