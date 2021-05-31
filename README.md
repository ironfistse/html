# HTML Notes

## Sources for learning
* https://ru.code-basics.com/languages/html/ (practical tasks)

---

## Basic markup of HTML page
```
<!DOCTYPE html>
<html lang="en-US">
<head>
    <meta charset="UTF-8">
    <title>Basic markup of HTML</title>
</head>
<body>
    <h1>Code Basics</h1>
    <p>Free programming place</p>
</body>
</html>
```
---

## HTML5 Tags

### \<header>
It has the same styles and properties like &lt;div> but it has a semantic meaning which is useful for robots. As a result they can analyze the meaning.
Usually it contains a logo, contact information, menu, etc.
```
<header>
  <!-- This will be the site header (top area). -->
</header>
```

---

### \<main>
It has the same styles and properties like &lt;div> but it has a semantic meaning.
The unique content of the site. This can be an article, a description of the service, data on the page, contacts, a service order form
```
<main>
  <!-- The unique content of the site -->
</main>
```

---

### \<footer>
It has the same styles and properties like &lt;div> but it has a semantic meaning.
Usually there is contact information, additional menu, legal information about the company.
```
<footer>
  <!-- Site footer (bottom area) -->
</footer>
```

---

### \<nav>
It is used to contain the main menu of the website. Sometimes a list of product categories is wrapped in a nav tag as well.
It has a semantic meaning for robots and different devices (screen readers, etc)
```
<nav>
    <ul>
        <li><a href="/">Главная</a></li>
        <li><a href="/about">О нас</a></li>
        <li><a href="/contacts">Контакты</a></li>
    </ul>
</nav>
```

---

### \<section   >
It allows you to mark content related to the main content meaning.
Inside is the content is directly related to the content of our page, but cannot exist without it.
Since &lt;section> is a piece of related content (article section, link form, etc.), there is often a heading inside (but it is not a requirement)
```
<section class="callback-form">
    <h2>Submit your application</h2>
    <form>
        <!-- Here is the service order form -->
    </form>
</section>
```

---
### \<article   >
It is intended to mark up a section that can be used on its own and is not structurally tied to a specific page.
For example, a block with exchange rates, weather, news or article previews.
Although these blocks may directly relate to the current page, they represent an independent unit that will not lose its meaning if you look at it separately from the context.
```
<section class="more">
    <h2>Read also</h2>
    <article class="article-block">
        <h3>Service 1</h3>
        <p>Description of new service</p>
        <a href="#">Link to the service</a>
    </article>

    <article class="article-block">
        <h3>Service 2</h3>
        <p>Description of new service</p>
        <a href="#">Link to the service</a>
    </article>
</section>
```
Due to the fact that &lt;article> can be used on its own, it must contain a heading inside it.

---

### \<audio>

This tag used to add audio on a page
```
<audio src="path to audio" controls></audio>
```
Different browsers support different audio formats. For this purpose you can use nested tag \<source>
```
<audio controls>
    <source src="https://example.com/audio.mp3">
    <source src="https://example.com/audio.ogg">
</audio>
```

### \<video>

This tag used to add video on a page
```
<video src="https://example.com/our-video.mp4" controls></video>
```
Different browsers support different video formats. For this purpose you can use nested tag \<source>
```
<video controls>
    <source src="https://example.com/our-video.mp4" type="video/mp4">
    <source src="https://example.com/our-video.webm" type="video/webm">
    <source src="https://example.com/our-video.ogg" type="video/ogg">
</video>
```
The presence of three formats of a file guarantees that your video will play on all devices. It is also required to have a type attribute that will tell the browser the video format. By this attribute the browser will decide which file to download.

The &lt;video> tag has several important attributes:
* controls - Adds controls for the video player.
* autoplay - Auto play after video download.
* width - The width of the video player.
* height - The height of the video player.

## Examples

### How to use label and input checkbox
Version #1 (relation by id)
```
<form>
    <input id="html" type="checkbox">
    <label for="html">I want to know HTML well</label>
</form>
```
Version #2 (relation through nesting)
```
<form>
    <label>
        <input type="checkbox">
        I want to know HTML well
    </label>
</form>
```

### How to use input checkbox
```
<form>
    <label>
        <input type="checkbox" name="languages" value="HTML">
        I want to learn HTML
    </label>
    <label>
        <input type="checkbox" name="languages" value="CSS">
        I want to learn CSS
    </label>
    <label>
        <input type="checkbox" name="languages" value="JS">
        I want to learn JS
    </label>
</form>
```
Attribute "name" is used to separate our checkboxes group among others and attribute "value" is used to find out which checkboxes were selected.

### How to use label and input radio
Version #1 (relation by id)
```
<form>
    <input id="radio_yes" type="radio" name="question">
    <label for="radio_yes">Yes</label>
    
    <input id="radio_no" type="radio" name="question">
    <label for="radio_no">No</label>
</form>
```
Version #2 (relation through nesting)
```
<form>
    <label>
        <input type="radio" name="question">
        Yes
    </label>
    <label>
        <input type="radio" name="question">
        No
    </label>
</form>
```

### How to use input radio
```
<form>
    <label>
        <input type="radio" name="question" value="yes">
        Yes
    </label>
    <label>
        <input type="radio" name="question" value="no">
        No
    </label>
</form>
```
Attribute "name" is used to make the browser understand the relationship between radios. Without "name" attribute it would be possible to choose all radios.
Attribute "value" is used to find out which particular radio was selected.
