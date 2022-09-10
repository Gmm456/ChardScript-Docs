# ChardScript User Input

ChardScript allows for user input.

That means we are able to ask the user for input but with nothing question.

#### Example

```renpy
call username = ask()
echo("Hello " + username + "!")
```

{% hint style="info" %}
ChardScript stops executing when it comes to the <mark style="color:red;">`input()`</mark> function, and continues when the user has given some input.
{% endhint %}
