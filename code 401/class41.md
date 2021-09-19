# React 4

## [Next.js - Dynamic Routes](https://nextjs.org/learn/basics/dynamic-routes)

#### Download Starter Code (Optional)

`npx create-next-app nextjs-blog --use-npm --example "https://github.com/vercel/next-learn/tree/master/basics/dynamic-routes-starter"`

#### You should also update the following files:

+ `public/images/profile.jpg` with your photo (Recommended: 400px width/height).
+ const name = `'[Your Name]'` in `components/layout.js` with your name.
+ `<p>[Your Self Introduction]</p>`in `pages/index.js` with your self introduction.

#### How to Statically Generate Pages with Dynamic Routes

We want each post to have the path `/posts/<id>`, where` <id>` is the name of the markdown file under the top-level posts directory.

Since we have `ssg-ssr.md` and `pre-rendering.md`, we’d like the paths to be `/posts/ssg-ssr `and `/posts/pre-rendering`.



#### First, we’ll create a page called `[id].js` under `pages/posts`. Pages that begin with [ and end with ] are dynamic routes in Next.js.

```
import Layout from '../../components/layout'

export default function Post() {
  return <Layout>...</Layout>
}
```

Now, here’s what’s new: We’ll export an async function called `getStaticPaths` from this page. 
In this function, we need to return a list of possible values for `id`.

```

Dynamic Routes
Page Path Depends on External Data
In the previous lesson, we covered the case where the page content depends on external data. We used getStaticProps to fetch required data to render the index page.

In this lesson, we’ll talk about the case where each page path depends on external data. Next.js allows you to statically generate pages with paths that depend on external data. This enables dynamic URLs in Next.js.

Page Path Depends on External Data
How to Statically Generate Pages with Dynamic Routes
In our case, we want to create dynamic routes for blog posts:

We want each post to have the path /posts/<id>, where <id> is the name of the markdown file under the top-level posts directory.
Since we have ssg-ssr.md and pre-rendering.md, we’d like the paths to be /posts/ssg-ssr and /posts/pre-rendering.
Overview of the Steps
We can do this by taking the following steps. You don’t have to make these changes yet — we’ll do it all on the next page.

First, we’ll create a page called [id].js under pages/posts. Pages that begin with [ and end with ] are dynamic routes in Next.js.

In pages/posts/[id].js, we’ll write code that will render a post page — just like other pages we’ve created.

import Layout from '../../components/layout'

export default function Post() {
  return <Layout>...</Layout>
}
Now, here’s what’s new: We’ll export an async function called getStaticPaths from this page. In this function, we need to return a list of possible values for id.

import Layout from '../../components/layout'

export default function Post() {
  return <Layout>...</Layout>
}

export async function getStaticPaths() {
  // Return a list of possible value for id
}

```


Finally, we need to implement `getStaticProps` again - this time, to fetch necessary data for the blog post with a given id. 

`getStaticProps `is given params, which contains id (because the file name is `[id].js`).

```
import Layout from '../../components/layout'

export default function Post() {
  return <Layout>...</Layout>
}

export async function getStaticPaths() {
  // Return a list of possible value for id
}

export async function getStaticProps({ params }) {
  // Fetch necessary data for the blog post using params.id
}
```
### Implement getStaticPaths

+ Create a file called `[id].js` inside the `pages/posts` directory.
+  Also, remove `first-post.js` inside the `pages/posts` directory — we’ll no longer use this.

+ paths contains the array of known paths returned by `getAllPostIds()`, which include the params defined by `pages/posts/[id].js`. 

### Render Markdown

To render markdown content, we’ll use the remark library. First, let’s install it:

`npm install remark@13 remark-html@13`

### Polishing the Post Page

Adding title to the `Post` Page

In `pages/posts/[id].js`, let’s add the title tag using the post data.

You'll need to add an import for `next/head` at the top of the file and add the title tag by updating the `Post` component

### Formatting the Date

To format the date, we’ll use the date-fns library. First, install it:

`npm install date-fns`

### Polishing the Index Page

Open `pages/index.js` and add the following imports at the top of the file for Link and Date:
```
import Link from 'next/link'
import Date from '../components/date'

```



## [Next.js - Deployment](https://nextjs.org/learn/basics/deploying-nextjs-app)

### Download Starter Code

`npx create-next-app nextjs-blog --use-npm --example "https://github.com/vercel/next-learn/tree/master/basics/basics-final"`


You should also update the following files:

+ `public/images/profile.jpg` with your photo (Recommended: 400px width/height).
+ `const name = '[Your Name]'` in `components/layout.js` with your name.
+ `<p>[Your Self Introduction]</p>` in `pages/index.js` with your self introduction.

### Push to GitHub

```
git remote add origin https://github.com/<username>/nextjs-blog.git
git push -u origin main
```
### Deploy to Vercel


The easiest way to deploy Next.js to production is to use the Vercel platform developed by the creators of Next.js.

Vercel is a serverless platform for static and hybrid applications built to integrate with your headless content, commerce, or database.

We make it easy for frontend teams to develop, preview, and ship delightful user experiences, where performance is the default. 

You can start using it for free — no credit card required.


+ Import your nextjs-blog repository
Once you’re signed up, import your nextjs-blog repository on Vercel. You can do so from here: https://vercel.com/import/git.

You’ll need to Install Vercel for GitHub. You can give it access to All Repositories.
Once you’ve installed Vercel, import `nextjs-blog`.
You can use default values for the following settings — no need to change anything. Vercel automatically detects that you have a `Next.js` app and chooses optimal build settings for you.

+ Project Name
+ Root Directory
+ Build Command
+ Output Directory
+ Development Command


#### Vercel has many more features, such as:

+ **Custom Domains**: Once deployed on Vercel, you can assign a custom domain to your Next.js app. Take a look at our documentation here.
Environment Variables: You can also set environment variables on Vercel. 

Take a look at our documentation here. 
You can then use those environment variables in your `Next.js` app.

+ **Automatic HTTPS**: HTTPS is enabled by default (including custom domains) and doesn't require extra configuration. We auto-renew SSL certificates.
