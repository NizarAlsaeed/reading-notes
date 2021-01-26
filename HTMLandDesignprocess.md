## Web pages Design with HTML

### Design process

**step \# 1:** Identify the Target Audience

**step \# 2:** Why they visit your site (motivation, goals)

**step \# 3:** What information do they need to achieve thier goals

**step \# 4:** How often will they visit you site

**step \# 5:** Draw the site map

**step \# 6:** determine the Wireframe  for each page

**step \# 7:** Organize and prioritize content including visual hierarchy

**step \# 8:** Grouping content

**step \# 9:** Start with the Navigation


###  HTML5 Layout 
> Duckett: HTML & CSS, Chapter 17 

- It is a good practice to use html 5 tags instead of div elements only to help the bowser and the search engine to identifiy you website content.

#### List of main layout tags
- header `<header> </header>` for main page header and sections header
- footer `<footer> </footer>` for main page footer and sections footer
- navigation `<nav> </nav>`
- article `<article> </article>`
- side bar `<aside> </aside>`
- section `<section> </section>`
- heading group `<hgroup> </hgroup>` *uncommon*
- figures 

```html
<figure> 
<img/> 
<figcaption> </figcaption>
</figure>
```
- div `<div></div>` 


### Extra Markup
> Duckett: HTML & CSS, Chapter 8 

#### versions of HTML:
1. HTML 4
2. Translational XHTML
3. Strict XHTML
4. HTML 5  


#### comments
In HTML you can insert comments to the developer using `<-- comment!-->`

#### class and id
these are global attributes used with css mainly, classe and id are for the same purpose but the difference is that id must have a unique value for each element.

`class= "class value"`

`id = "id value"`

#### block elements and inline elements
block elements starts a new line and take up all the horizontal space on the line, but the inlne elements sit beside each other on the same line and take only the required horizontal space
#### iframes
you can include a live copy of other web page to be shown on your website directly using iframe tag with the src attribute:

```html
<iframe>
src="webpage link"
</iframe>
``` 

