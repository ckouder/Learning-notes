# 10 tips for beginner to design webpages

### 1. Ensure the objective of the website before making

It's kind of tricky because this rule can be used in nearly everywhere. For a person who want to learn to make a website, will often get into the traps of CSS: they want to use different kinds of special effects in their website and ignore whether they fit the final objective or not.

Often, this action will lead to a bad end: the magnificent effects they persuade will become a distraction while reading. Therefore, first we have to ensure the objective of the website.

### 2. Prototype website for different devices first

For different devices, the webpage will look different in may ways. This is because web developers and designers have made some magic to deal with these conditions: prototyping.

There's many professional prototyping tools on website, [sketch](/www.sketchapp.com) and [adobe XD](http://www.adobe.com/products/experience-design.html?promoid=PYPVQ3HN&mv=other) are definitely good helpers, some pencil-paper-based quick sketches are also fine. I recommend to have the later option because the first one will take you long time to learn. As a beginner, prototyping can help you understand elements arrangement in a much clear and direct way. This will help reduce time cost later on debugging.

\[pictures\]

### 3.Use framework in projects

Frameworks are useful "wheels" which can largely improve your working efficiency. Someone may thinks that producing an individual framework during work can be pleasant. But remember, never reproduce the wheels, that's useless especially when you are making a website, unless you have to. Without proper framework, your development will become less efficient and will meet thousands of unexpected problems which really frustrated you.

In contrast, after you finish current projects, studying the framework, or reproducing the framework become useful. It can help you better understanding how the framework and website work.

recommend: [bootstrap 4](https://v4-alpha.getbootstrap.com/)

### 4.Carefully name DOM elements

Tell a joke, in old China, poor people always give name casually to their children such as "Ergou Wang"\(which first name has the meaning of two dogs\). They believe that this can brings good luck into family. However, good luck never fall this way when you are developing. It only causes brain chaos when you searching for this element.

The DOM elements are often connected to CSS. A careful class name can reduce time cost in understanding and searching for proper elements. In the table below, I will show some examples of good names and bad names.

| Sections of documents | Parts of section | GOOD class name | BAD class name |
| :--- | :--- | :--- | :--- |
| navigation bar | icon | nav-icon | iconA |
|  | search input | nav-search-input | search |
|  | search submit button | nav-search-submit | submit |
| content | articles | content-article | articleName |
|  | image in articles | content-image | imageofdogs |

As you can see, some bad names are really short and don't represent any positional characteristics, some even use content to name it\(do you change the class name when content inside changes?\). A good name should avoid these problems above. I recommend you to learn [BEM](https://en.bem.info/methodology/). \(although its class names are long sometimes.

### 5.Learn CSS pre-processors and Emmet

Once you get familiar with HTML and CSS, it's a good choice for you to learn some other things such as LESS, SCSS\(both for CSS pre-processing\) and Emmet\(type html in an intelligent way\). These tools will make you work in a much simpler way. Sometimes you may find out that it's difficult for you to understand the abstract concepts such as @mixin, it means that you have to spend more time on doing more projects in an original way.

Once you found out that how complex to do with original codes, you will automatically recognize the advantages of studying these pre-processing languages.

They are born to deal with such conditions.

### 6.Add comments

According to some recent researches, no matter how your are familiar with your personal codes, you will have less impressions after 6 weeks. This means you will forget the logic inside your code after 6 weeks. Therefore adding comments are **really really important **for both yourself and others.

A good comments can implement a module, a special functionality or a variable in a few words others can be misleading. To study how to write a good comment, I recommend that you can write comments in this way:

Result - \(Parts\) - Functions - Modules

for a retro-snake game, a function used to check whether the snake collides something while moving snake forward, you can have:

```js
// returns a bool value to check whether the snake collides food during snake's movement.
function collideCheck(snakePos, FoodPos) {
    // collide: return true if the snake collides FoodPos when the snake is moving
    var collide = false;
    ...
}
```

### 7.Abstract common styles from CSS into variables and classes

Have you ever met such condition? You want to refresh a color into another color in CSS but the color is everywhere inside this file. So you keep searching and searching to the end of the document. That's idotic, complex and time-consuming! The best way to deal with this condition is to abstract those styles into CSS variables or classes, use them directly in HTML file. For example:

```html
...
<div class="content">
    ...
    <ul class="content-article-list">
      ...
      ...
    </ul>
</div>
<footer> ... </footer>
```

```css
/*Fundamental CSS*/
/*---------------*/
li {
    background-color: #333;
    color: #e61b43;
}

.content > .content-article-list {
    padding: 15px 0 15px 0;
    background-color: #333;
    color: #e61b43;
}

footer {
    background-color: #333;
    color: #e61b43;
}
```

can be changed into:

```html
...
<div class="content bg-black-text-red">
    ...
    <ul class="content-article-list bg-black-text-red">
        ...
        ...
    </ul>
</div>
<footer> ... </footer>
```

```css
.bg-black-text-red {
    background-color: #333;
    color: #c61b43;
}

.content-article-list {
    padding: 15px 0 15px 0;
}
```

much more clear, right ?

### 8.Tidy up documents into one fixed style

> "Part of being a good steward to a successful project is realizing that writing code for yourself is a Bad Idea™. If thousands of people are using your code, then **write your code for maximum clarity**" - Idan Gazit

While coding, some habits are important for both yourself and others and tidy up the document is one of the most important one. For a instance, some coders like to have 4 space as a tab while others prefer 8 spaces or 2 spaces. It's important to follow a fixed rule in any document. 8 spaces are OK so never change to 4 space in a single document. That will cause chaos in others' mind.

You can find detailed CSS coding standard [here.](https://make.wordpress.org/core/handbook/best-practices/coding-standards/css/)

### 9.Do cross-browser tests

Well, many websites are seemed to be fixed in style in different browsers but actually they are not. Different companies have different methods to resolve HTML file, box model and JavaScript file and make it work properly. However, some CSS attributes are quite different in different browsers. Some of them needed to act prefix while others may never work. It's **really important** to test your website in different browsers. 

However, if you are using a framework in your website, you may pass the browser test easily because all the published framework are being test in different browsers.

### 10.READ-SEARCH-ASK

This is a good habit. When you're debugging, read your code until you can not find any problem, then search the internet. "Ask" will be the last option because it's time-consuming and has the risk to be wrong.

Here's a list of helpful websites:

* [Mozilla Developer Network](https://developer.mozilla.org/en-US/)
* [W3C Wiki](https://www.w3.org/wiki/Main_Page)
* [Bootstrap 4 Documentation](https://v4-alpha.getbootstrap.com/getting-started/introduction/)
* [CSS-tricks](https://css-tricks.com/)
* [Runoob\(Chinese\)](https://runoob.com/)
* [Github](/github.com)

Here you can find some helpful lessons:

* [freeCodeCamp](/freecodecamp.com)

Here you can ask questions:

* [Quora](/quora.com)
* [StackOverFlow](/stackoverflow.com)
* [freeCodeCamp - Forum ](https://forum.freecodecamp.com/)



