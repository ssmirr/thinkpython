# Strings

## 8.1 A string is a sequence

A string is a **sequence** of characters. You can access the characters one at a time with the
bracket operator:

```python | {type: 'terminal'}
fruit = 'banana'
letter = fruit[1]

```

The second statement selects character number 1 from `fruit` and assigns it to letter.

The expression in brackets is called an **index**. The index indicates which character in the sequence you want (hence the name).

But you might not get what you expect:

```python | {type: 'terminal'}
fruit = 'banana'
letter = fruit[0]
print letter

```

So `b` is the 0th letter ("zero-eth") of 'banana', `a` is the 1th letter ("one-eth"), and `n` is the 2th ("two-eth") letter.

You can use any expression, including variables and operators, as an index, but the value of the index has to be an integer. Otherwise you get:

```python | {type: 'terminal'}
fruit = 'banana'
letter = fruit[1.5]

```

> ✨ _This is an interactive document, so feel free to type your own statements above to run and explore the possibilities_ ☝

## 8.2 `len`

`len` is a built-in function that returns the number of characters in a string:

```python | {type: 'terminal'}
fruit = 'banana'
len(fruit)

```

To get the last letter of a string, you might be tempted to try something like this:

```python | {type: 'terminal'}
fruit = 'banana'
length = len(fruit)
last = fruit[length]

```

The reason for the `IndexError` is that there is no letter in `banana` with the index 6. Since we started counting at zero, the six letters are numbered 0 to 5. To get the last character, you have to subtract 1 from length:

```python | {type: 'terminal'}
fruit = 'banana'
length = len(fruit)
last = fruit[length-1]

```

Alternatively, you can use negative indices, which count backward from the end of the string. The expression `fruit[-1]` yields the last letter, `fruit[-2] yields the second to last, and so on. Try to get the 6th to last character using the REPL above and negative indices; what is this letter?

## 8.3 Traversal with `for` loop

A lot of computations involve processing a string one character at a time. Often they start at the beginning, select each character in turn, do something to it, and continue until the end. This pattern of processing is called a **traversal**. One way to write a traversal is with a `while` loop:

```python | {type: 'script'}
index = 0
while index < len(fruit):
    letter = fruit[index]
    print(letter)
    index = index + 1
```


```bash | {type: 'terminal'}
```

```bash | {type: 'terminal'}
```

```bash | {type: 'terminal'}
```