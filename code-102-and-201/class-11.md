# Assorted Topics

## Images

to align an image 
```css
img{
display: block;
margin: 0 auto;}
```

```css
section {
background-image: url("images/...");
background-repeat: no-repeat;
background-position: center center; OR background-position: 50% 50%;
}

/*You can also use a pair of pixels
or percentages. These represent
the distance from the top left
corner of the browser window
(or containing box).*/
```

`background 1 2 3 4 5` shorthand:
1: background-color
2: background-image
3: background-repeat
4: background-attachment
5: background-position


## Search engine optimization (SEO)

On-Page Techniques: text inside the webpage including Image Alt Text and Page Descriptions,The description also lives inside
the `<head>` element and is
specified using a `<meta>` tag.
It should be a sentence that
describes the content of the
page.

Off-Page Techniques: links to the page from other websites


Google analytics is a useful tool to get information about your website visitors .

In order to put your site on the web you will
need a domain name and web hosting.

when looking for a hostingservice check the:
- Disk space
- Bandwidth
- Backups
- Email accounts
- Server-side languages and databases

To transfer your code and images from your
computer to your hosting company, you use
something known as File Transfer Protocol.


## Video and Audio

The `<video>` and `<audio>` elements allow us to embed video and audio into web pages

```html
<video controls>
  <source src="" type="video/mp4">
  <p>a message if the video is not shown</p>
</video>

<audio controls src="">

</audio>
```

