# React 4
For the case where each page path depends on external
data. Next.js allows you to statically generate pages with paths that depend on external data. This enables dynamic URLs in Next.js.

### Overview of the Steps
First, we’ll create a page called [id].js. Pages that begin with [ and end with ] are dynamic routes in Next.js.

Now, here’s what’s new: We’ll export an async function called getStaticPaths from this page. In this function
, we need to return a list of possible values for id.

Finally, we need to implement getStaticProps to fetch necessary data for the blog post with a 
given id. getStaticProps is given params, which contains id (because the file name is [id].js).

 The returned list is not just an array of strings — it must be an array of objects that look like the comment above.
 Each object must have the params key and contain an object 
 with the id key (because we’re using [id] in the file name). Otherwise, getStaticPaths will fail.
 
 ### Render Markdown
 To render markdown content, we’ll use the remark library.
 
 `npm install remark remark-html`
 
 ```javascript
import remark from 'remark'
import html from 'remark-html'

// Use remark to convert markdown into HTML string
  const processedContent = await remark()
    .use(html)
    .process(matterResult.content)
  const contentHtml = processedContent.toString()
```

## Deployment
### Deploy to Vercel
First, go to https://vercel.com/signup to create a Vercel account. Choose Continue with GitHub and go through the sign up process.

Choose your repo, when you deploy, your Next.js app will start building. It should finish in under a minute.

When it’s done, you’ll get deployment URLs. Click on one of the URLs and you should see the Next.js starter page live.




