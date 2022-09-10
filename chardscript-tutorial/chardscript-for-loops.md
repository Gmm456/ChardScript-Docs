# ChardScript For Loops

## ChardScript For Loops

A **for** loop is a repetition control structure that allows you to efficiently write a loop that needs to execute a specific number of times.

#### Example

The increment is 1:

{% code lineNumbers="true" %}
```renpy
for i=0 to 5 then
  echo(i)
end
```
{% endcode %}

## Custom increment For Loops

#### Example

The increment is 2.5:

{% code lineNumbers="true" %}
```renpy
for i=0 to 5 step 2.5 then
  echo(i)
end
```
{% endcode %}
