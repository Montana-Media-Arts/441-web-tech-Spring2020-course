---
title: Code on This Site
module: 2
jotted: true
---

# Code on This Site

<!--
<div class="embed-responsive embed-responsive-16by9"><iframe class="embed-responsive-item" src="https://www.youtube.com/embed/dK9cVaLtjaw" frameborder="0" allowfullscreen></iframe></div>
-->

Now that we have started looking at code, I want to mention a few specifics about how code will work and what it will look like on this site.

You have hopefully already noticed, during all of these first three weeks that there are specific code blocks. These should be displayed in your browser with a dark grey background and utilize a monospaced font. In theory this should _look like code_.

<div id="code-heading">Code Info</div>

```
Example Code Block

This is what code will look like in your browser on this site.
```

<br />


This code will also be highlighted so that the syntax of the code is more apparent.

## Specifying Language or File

When appropriate, there will be information about what the code is you are looking at in the upper-right hand corner. Typically, for this course, this will be one of;

- **HTML**
    - This is HTML code.
- **CSS**
   - This is Cascading Style Sheets
- **JS**
    - or JavaScript, which specifies the code you are looking at is general JavaScript.

# Code Results Output

Whenever possible and appropriate, I will also work to show you what the code output we are working on should look like. These sections will be surrounded with a big border.

<div class="displayed_code_example">
    <h1 style="">Code Results are Displayed in These Sections</h1>
</div>

# Playing with Code

Also, whenever possible, I will try to provide code output in a way that is editable, changeable, and playable, by you. There will static code blocks above the results sections, but there will also be a tab'd bar within the output section, that at a minimum will include;

- "Result"
- "HTML"
- "JavaScript"

If you see one of these sections, you can;

1. click on the other tabs,
2. change the code,
3. go back to "Results"
4. and see the changes live!

Try it below with the "Hello World!" example.

To do this;

- click the "JavaScript" tab,
- change the `"Hello World!"` bit in line 4,
    - perhaps add some more text, or change the tag types...?
- and go back to Results. You should now see your changes!


<div id="jotted-demo-1" class="jotted-theme-stacked"></div>

<script>
    new Jotted(document.querySelector("#jotted-demo-1"), {
    files: [
        {
            type: "js",
            hide: false,
            url:"https://raw.githubusercontent.com/Montana-Media-Arts/441-WebTech/master/lecture_code/02/02/script.js"
        },
        {
            type: "html",
            hide: false,
            url:"https://raw.githubusercontent.com/Montana-Media-Arts/441-WebTech/master/lecture_code/02/02/02_js_outside_html.html"

    }],
    showBlank: false,
    showResult: true,
    runScripts: false,
    plugins: [
        { name: 'ace', options: { "maxLines": 50 } },
        // { name: 'console', options: { autoClear: true } },
    ]
});
</script>


# Code Links

Below many code examples, there will also be a number of links. These are, and do the following;


- [**[ Code Download ]**](https://github.com/Montana-Media-Arts/441-WebTech/blob/master/lecture_code/02/02/02_js_outside_html.zip)
    - This will be a zip'd folder, containing all of the code for the example.
    - This is a way for you to easily download code examples, to play with on your own computers.
- [**[ View on GitHub ]**](https://github.com/Montana-Media-Arts/441-WebTech/tree/master/lecture_code/02/02)
    - This link will take you directly to the GitHub entry for this code, so that you can look at it there.
- [**[ Live Example ]**](https://montana-media-arts.github.io/441-WebTech/lecture_code/02/02/02_js_outside_html.html)
    - This will take you to a webpage that only has the code in question presented.

These links will occur underneath code examples when appropriate and available.