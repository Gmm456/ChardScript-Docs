# ChardScript List

{% code lineNumbers="true" %}
```renpy
call myList = ["apple", "banana", "cherry"]
```
{% endcode %}

## List

Lists are used to store multiple items in a single variable.

Lists are created using square brackets:

#### Example

Create a List:

{% code lineNumbers="true" %}
```renpy
call thisList = ["apple", "banana", "cherry"]
echo(thisList)
```
{% endcode %}

## List Items

List items can add new item values, extend list to list and allow duplicate values.

List items are indexed, the first item has index <mark style="color:red;">`[0]`</mark>, the second item has index <mark style="color:red;">`[1]`</mark> etc.

## Append

To appends an element to the end of the list, use <mark style="color:red;">`append()`</mark> function:

#### Example

{% code lineNumbers="true" %}
```renpy
call theList = ["Hello World!"]
append(theList, "Hi World!")
echo(theList)
# Output: Hello World!, Hi World!
```
{% endcode %}

## Extend

To add the specified list elements (or any iterable) to the end of the current list, use <mark style="color:red;">`extend()`</mark> function:

#### Example

{% code lineNumbers="true" %}
```renpy
call list1 = ["apple", "banana"]
call list2 = ["cherry", "mango"]
extend(list2, list1)
echo(list2)
# Output: cherry, mango, apple, banana
```
{% endcode %}

## Allow Duplicates

Since lists are indexed, lists can have items with the same value:

#### Example

{% code lineNumbers="true" %}
```renpy
call thislist = ["apple", "banana", "apple", "banana"]
echo(thislist)
```
{% endcode %}

## List Length

To determine how many items a list has, use the <mark style="color:red;">`length()`</mark> function:

#### Example

{% code lineNumbers="true" %}
```renpy
call thislist = ["apple", "banana", "cherry"]
echo(length(thislist))
```
{% endcode %}

## List Items - Data Types

List items can be of any data type:

#### Example

String, int and boolean data types:

{% code lineNumbers="true" %}
```renpy
call list1 = ["apple", "banana", "cherry"]
call list2 = [1, 5, 7, 9, 3]
call list3 = [true, false, false]
```
{% endcode %}

A list can contain different data types:

#### Example

A list with strings, integers and boolean values:

{% code lineNumbers="true" %}
```renpy
call list1 = ["abc", 34, true, 40, "male"]
```
{% endcode %}

