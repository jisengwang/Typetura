# Typetura v4

Typetura is a CSS library that allows you to create dynamic responsive type systems with ease. v4 has numerous changes, including removal of all JavaScript, a new license (MIT), and a few changes to the API.

## What is Typetura?

Is it software? Is it a company? Yes.

Scott Kellum was working on ways to make variable fonts responsive to the viewport. Frustrated with the limitations of clamp(), he developed the technology and decided to quit his day job and start a company around the ideas that it enabled.

## Installation

Add [typetura.css](https://raw.githubusercontent.com/Typetura/Typetura/main/typetura.css) to your project. Copy and paste it into your CSS file or link to it in your HTML.

## Using Typetura

With Typetura you need to do three things: Identify the context, bind typetura’s styles, and create keyframes for your styles.

### Identifying the Context

By default, the context is the viewport. Similar to viewport units, Typetura looks at the width of the viewport to determine what styles to use. You can define your own context by using the utlity class `class="cq"` or by adding `container-type: inline-size;` to any element in your CSS. If you’re fimiliar with container queries, you’ve already got the hang of it.

```html
<div class="cq">
  <h1>Hello, world!</h1>
</div>
```

### Binding Typetura’s Styles

Typetura’s styles are bound to your elements by using the `tt` class.

```html
<div class="cq">
  <h1 class="tt">Hello, world!</h1>
</div>
```

### Creating Keyframes

Creating keyframes is where you’ll be spending most of your time. These are regular CSS keyframes that you might have used before, but they define how your styles change as the container gets bigger.

```html
<div class="cq">
  <h1 class="tt">Hello, world!</h1>
</div>
```

```css
h1 {
  animation-name: hello-world;
}
@keyframes hello-world {
  from {
    font-size: 1rem;
  }
  to {
    font-size: 4rem;
  }
}
```

### Advanced use of Typetura

Now that you’re up and running you may want to dive a little deeper in to what Typetura can do.

#### Identifying the Contexts

These are generic [container queries](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_containment/Container_queries) and can be defined using `container-type: inline-size;` in your CSS.

```css
.container {
  container-type: inline-size;
}
```



## Aknowledgements

Typetura is created and developed by [Scott Kellum](https://scottkellum.com) and Typetura LLC.

Special things to [Ana Monroe](https://anamonroe.com) for all the support and guidance, Gabrielle Kellner for helping communicate the vision, [Jane Ori](https://propjockey.io/) for cracking the `calc()` division problem, and [Roman Komarov](https://kizu.dev/) and [Miriam Suzanne](https://miriamsuzanne.com/) for their trailblazing on the bleeding edge of CSS.

## Patents

Use of this software does not grant licence to any patents held by Typetura LLC. For more information, please contact [Typetura LLC](https://typetura.com/ip) at [info@typetura.com](mailto:info@typetura.com). These patents describe the distribution of typographc systems at scale as well as how design software might be used to create and manage dynamic typographic systems. These patents protect our business usecases for this software and are not intended to restrict the use of the software itself on projects you own, operate, control, or are a part of.

As an example, if `fonts.bigcompany.com` is interested in distributing typographic systems with their fonts, they would need to license the patents. If `Big Design Software` decided to create an interface keyframing out text scaling in their app, they would need to license the patents. If `yourcompany.com` is using Typetura to manage their own typographic system, they would not need to license the patents.

## License (MIT)

Copyright © 2024 [Typetura LLC](https://typetura.com/)

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the “Software”), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

**The software is provided “as is”, without warranty of any kind, express or implied, including but not limited to the warranties of merchantability, fitness for a particular purpose and noninfringement. In no event shall the authors or copyright holders be liable for any claim, damages or other liability, whether in an action of contract, tort or otherwise, arising from, out of or in connection with the software or the use or other dealings in the software.**