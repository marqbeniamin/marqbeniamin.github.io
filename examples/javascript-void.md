# What `javascript:void(0);` actually means?

![what is javascript void](https://images.unsplash.com/photo-1603468620905-8de7d86b781e?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2676&q=80)

As a frontend developer or even as a backend developer maybe you have found `javascript: void(0);` written as a value for a href attribute inside an anchor tag (`<a>`) and you wondered what that means.

Example:
```

<a href="javascript:void(0);" onclick="clickFunction()">
  Click
</a>

```

In this article, we will try to provide an explanation for the above syntax in order for you to know when and why it's used. To do that we will have to take it element by element.

## Javascript `void` keyword

As in other programming languages, `void` keyword from Javascript, is an operator that has the role to tell the program NOT to return the result of an expression and it returns `undefined` instead.

For example, the following expression will return the value of the mathematical operation:
```

let sum = 1 + 1;
console.log(sum); // 2

```
And the next expression will return `undefined`:
```

let sum = void(1 + 1);
console.log(sum); // undefined

```
Even though the variable `sum` is `undefined`, Javascript still executes the expression `(1 + 1)`:
```

let sum = void console.log(1 + 1); // 2
console.log(sum); // undefined

```
From the above, we can observe that the code that it is after the `void` operator will always be executed but the return of the expression will always be `undefined`. The role of `0` inside the void operator is simply just the one of a placeholder.

## Use `javascript:void(0);` as the value of href

The `javascript:` part is a possible value for the `href` attribute. This value tells your browser that the next text is a Javascript code and it should be treated accordingly. There are also other possible values for the `href` attribute like mailto:, file:, tel:, sms: etc.

## What is `javascript:void(0);`?

By using `javascript:void(0)`, the `<a>` tag will not send you to other web address. It will also not refresh the page as links usually do when you don't specify a value for the href attribute.

If you are wondering why we don't just remove the `href` attribute, the answer is that by removing the `href` attribute we will also remove the link appearance of the `<a>` element. That means that the cursor will not change when hovering the `<a>` tag. The cursor will act like it is on normal text.

In other words, by adding `javascript:void(0)` as the value of href attribute we will create a link that does nothing.

The example link from the beginning of this article will run the `clickFunction` function when the tag is clicked, but without refreshing the page or sending you to a different page.

## When to use `javascript:void(0);`?

Thankfully, with all the updates made in Javascript, you will never have to use it as there are better alternatives to it.

In order to prevent the default behavior of an `<a>` tag, it's generally recommended to use the `<button>` tag for buttons and the `<a>` tag for links. Also, if you need or want to change the cursor, it's recommended to use CSS instead of changing the tag to `<a>`.

In conclusion, we hope that now you have a better understanding of what `javascript:void(0);` is. Since it does nothing that you can't do with only HTML/CSS, the syntax presented at the beginning is not so common these days. Use this piece of information only to know what role it has when you see it somewhere, but keep your code clean and follow our advice on best practices.
