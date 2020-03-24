<p align="center"><img src="/images/c4c-x-omafra-banner.png" alt="Code for Canada Logo" style="display: block; margin: 0 auto;"></p>

---

Link to blog: https://code-for-canada.github.io/omafra-updates/

# Add a Post

## Quick Start

### Step 1) Create the file

Navigate to the [_posts folder](https://github.com/code-for-canada/omafra-updates/tree/master/_posts) and click the `Create new file` button ![Create new file button example](/images/create-file-ex.png)

Make sure to name the post in the format `<YYYY-MM-DD-Post-Title>.md` e.g. `2020-03-02-First-Month.md`

### Step 2) Add post data

At the top of the file add your post data in the format:

```
---
layout: post
title: <Your Post Title>
author: <Your Full Name>
banner: <Image File Name>
---
```
e.g.
```
---
layout: post
title: First Month at OMAFRA
author: Seyi Tayor
banner: sprint-0-banner.png
---
```

Don't worry  This won't appear in the post, it's only used for the blog to pull some information about the post to be displayed.

### Step 3) Add your content

Make sure to write your content in markdown format, I've included a link to a quick markdown guide below.

https://guides.github.com/features/mastering-markdown/

If you're editing your file on github.com you can click `Preview Changes` to view your post formatted in Markdown

(I'll talk about adding images to your post below, it's a little fussy)

### Step 4) Publish your post

When your done editing on GitHub just scroll down to the bottom of the page and click `Commit Changes`

It should look something like this:

![Commit Changes screenshot](/images/commit-ex.png)

### Step 5) Check out your work!

Now you can go to the blog and check out your post!

The post will be availabe at `https://code-for-canada.github.io/omafra-updates/<your-post-title>`

It may take a few minutes for your post to appear but don't worry, if you followed the instructions above it should be up shortly!

## Add Images to Your Post

What's an article without pictures? I mean, I guess it's still an article but you should add some pictures anyway!

Here's how:

### Step 1) Upload your image to github

> If you're using an image hosted on another site you can skip straight to step 2

Navigate to the [images folder](/images) and click `Upload files` right next to the `Create new file` button we saw before. Select your photo to upload and blah blah blah, you know how to upload files to stuff.

> Note: Images will display at their actual size (up to a maximum width the same as the post body), make sure to edit the files so they're the size you want

### Step 2) Add your image to a post

We're gonna use markdown notation here to add our image so it'll look a little funny

The markdown notation for images is `![<alt text that describes your image>](<https://your-image-url-here>)`

To include an external image just copy and paste the full URL

To include an image hosted in our `images` folder (like we added in Step 1) use the path `/omafra-updates/images/<your-file-name>`

For example, to include the Code for Canada logo saved in `/images` add `![Code for Canada logo](/omafra-updates/images/cfc-web-logo.png)`

You should see:
![Code for Canada logo](/images/cfc-web-logo.png)

> Note: These images won't work when you preview the post in the github editor, this is because of the way our blog is compiled when we publish.
> In order to preview your post with images change the path to `/images/<your-file-name>`, removing the `/omafra-updates` prefix, just make sure to add it back before publishing

## Banner Images

I've added some special styling rules for banner images at the top of a post. If you want to include a banner image with your post make sure to include a banner item in your post data at the top of your file like the example below

```
---
layout: post
title: First Month at OMAFRA
author: Seyi Tayor
banner: sprint-0-banner.png
---
```
For now banners must be hosted in the `images` folder and cannot be external photos

Make sure to only include the file name in the post data, don't include `/omafra-updates/images/` like you would for a normal image

## Adding a Table of Contents

You can add an auto-generated Table of Contents to your posts with just a couple lines in your markdown file.

```
1. Contents
{:toc}
```

Add these two lines anywhere you want the ToC to appear (my preferance is right after the intro paragraph) and when the page is rendered your ToC will be auto-magically populated with all of the headers in your post.

![A screenshot of the auto-generated table of contents](/images/toc-screenshot.png)

Make sure you write informative headers!

<br />

# Jekyll Now

> Note: I've included the generic Jekyll Now README below

### Code for Canada team blog quick start
(this assumes previous knowledge of github and access to the Code for Canada github org)

1. Clone [Jekyll Now](https://github.com/barryclark/jekyll-now)
2. Create your blog's repository in the Code for Canada github org
3. Push your Jekyll Now clone to your new repo
4. **In your repo settings under Github Pages change source from gh-pages to master** (or don't, I'm not a cop)
5. In `_config.yml` set `baseurl` (line 50) to your project name with a `/` in front (ex. this repo's `baseurl` is set to `/omafra-updates`)
6. Follow instructions in Jekyll Now generic README below starting from step 2

<details><summary>Open the Jekyll Now generic README</summary>
  
# Jekyll Now

**Jekyll** is a static site generator that's perfect for GitHub hosted blogs ([Jekyll Repository](https://github.com/jekyll/jekyll))

**Jekyll Now** makes it easier to create your Jekyll blog, by eliminating a lot of the up front setup.

- You don't need to touch the command line
- You don't need to install/configure ruby, rvm/rbenv, ruby gems :relaxed:
- You don't need to install runtime dependencies like markdown processors, Pygments, etc
- If you're on Windows, this will make setting up Jekyll a lot easier
- It's easy to try out, you can just delete your forked repository if you don't like it

In a few minutes you'll be set up with a minimal, responsive blog like the one below giving you more time to spend on writing epic blog posts!

![Jekyll Now Theme Screenshot](/images/jekyll-now-theme-screenshot.jpg "Jekyll Now Theme Screenshot")

## Quick Start

### Step 1) Fork Jekyll Now to your User Repository

Fork this repo, then rename the repository to yourgithubusername.github.io.

Your Jekyll blog will often be viewable immediately at <https://yourgithubusername.github.io> (if it's not, you can often force it to build by completing step 2)

![Step 1](/images/step1.gif "Step 1")

### Step 2) Customize and view your site

Enter your site name, description, avatar and many other options by editing the _config.yml file. You can easily turn on Google Analytics tracking, Disqus commenting and social icons here too.

Making a change to _config.yml (or any file in your repository) will force GitHub Pages to rebuild your site with jekyll. Your rebuilt site will be viewable a few seconds later at <https://yourgithubusername.github.io> - if not, give it ten minutes as GitHub suggests and it'll appear soon

> There are 3 different ways that you can make changes to your blog's files:

> 1. Edit files within your new username.github.io repository in the browser at GitHub.com (shown below).
> 2. Use a third party GitHub content editor, like [Prose by Development Seed](http://prose.io). It's optimized for use with Jekyll making markdown editing, writing drafts, and uploading images really easy.
> 3. Clone down your repository and make updates locally, then push them to your GitHub repository.

![_config.yml](/images/config.png "_config.yml")

### Step 3) Publish your first blog post

Edit `/_posts/2014-3-3-Hello-World.md` to publish your first blog post. This [Markdown Cheatsheet](http://www.jekyllnow.com/Markdown-Style-Guide/) might come in handy.

![First Post](/images/first-post.png "First Post")

> You can add additional posts in the browser on GitHub.com too! Just hit the + icon in `/_posts/` to create new content. Just make sure to include the [front-matter](http://jekyllrb.com/docs/frontmatter/) block at the top of each new blog post and make sure the post's filename is in this format: year-month-day-title.md

## Local Development

1. Install Jekyll and plug-ins in one fell swoop. `gem install github-pages` This mirrors the plug-ins used by GitHub Pages on your local machine including Jekyll, Sass, etc.
2. Clone down your fork `git clone https://github.com/yourusername/yourusername.github.io.git`
3. Serve the site and watch for markup/sass changes `jekyll serve`
4. View your website at http://127.0.0.1:4000/
5. Commit any changes and push everything to the master branch of your GitHub user repository. GitHub Pages will then rebuild and serve your website.

## Moar!

I've created a more detailed walkthrough, [**Build A Blog With Jekyll And GitHub Pages**](http://www.smashingmagazine.com/2014/08/01/build-blog-jekyll-github-pages/) over at the Smashing Magazine website. Check it out if you'd like a more detailed walkthrough and some background on Jekyll. :metal:

It covers:

- A more detailed walkthrough of setting up your Jekyll blog
- Common issues that you might encounter while using Jekyll
- Importing from Wordpress, using your own domain name, and blogging in your favorite editor
- Theming in Jekyll, with Liquid templating examples
- A quick look at Jekyll 2.0’s new features, including Sass/Coffeescript support and Collections

## Jekyll Now Features

✓ Command-line free _fork-first workflow_, using GitHub.com to create, customize and post to your blog  
✓ Fully responsive and mobile optimized base theme (**[Theme Demo](http://jekyllnow.com)**)  
✓ Sass/Coffeescript support using Jekyll 2.0  
✓ Free hosting on your GitHub Pages user site  
✓ Markdown blogging  
✓ Syntax highlighting  
✓ Disqus commenting  
✓ Google Analytics integration  
✓ SVG social icons for your footer  
✓ 3 http requests, including your avatar  

✘ No installing dependencies
✘ No need to set up local development  
✘ No configuring plugins  
✘ No need to spend time on theming  
✘ More time to code other things ... wait ✓!  

## Questions?

[Open an Issue](https://github.com/barryclark/jekyll-now/issues/new) and let's chat!

## Other forkable themes

You can use the [Quick Start](https://github.com/barryclark/jekyll-now#quick-start) workflow with other themes that are set up to be forked too! Here are some of my favorites:

- [Hyde](https://github.com/poole/hyde) by MDO
- [Lanyon](https://github.com/poole/lanyon) by MDO
- [mojombo.github.io](https://github.com/mojombo/mojombo.github.io) by Tom Preston-Werner
- [Left](https://github.com/holman/left) by Zach Holman
- [Minimal Mistakes](https://github.com/mmistakes/minimal-mistakes) by Michael Rose
- [Skinny Bones](https://github.com/mmistakes/skinny-bones-jekyll) by Michael Rose

## Credits

- [Jekyll](https://github.com/jekyll/jekyll) - Thanks to its creators, contributors and maintainers.
- [SVG icons](https://github.com/neilorangepeel/Free-Social-Icons) - Thanks, Neil Orange Peel. They're beautiful.
- [Solarized Light Pygments](https://gist.github.com/edwardhotchkiss/2005058) - Thanks, Edward.
- [Joel Glovier](http://joelglovier.com/writing/) - Great Jekyll articles. I used Joel's feed.xml in this repository.
- [David Furnes](https://github.com/dfurnes), [Jon Uy](https://github.com/jonuy), [Luke Patton](https://github.com/lkpttn) - Thanks for the design/code reviews.
- [Bart Kiers](https://github.com/bkiers), [Florian Simon](https://github.com/vermluh), [Henry Stanley](https://github.com/henryaj), [Hun Jae Lee](https://github.com/hunjaelee), [Javier Cejudo](https://github.com/javiercejudo), [Peter Etelej](https://github.com/etelej), [Ben Abbott](https://github.com/jaminscript), [Ray Nicholus](https://github.com/rnicholus), [Erin Grand](https://github.com/eringrand), [Léo Colombaro](https://github.com/LeoColomb), [Dean Attali](https://github.com/daattali), [Clayton Errington](https://github.com/cjerrington), [Colton Fitzgerald](https://github.com/coltonfitzgerald), [Trace Mayer](https://github.com/sunnankar) - Thanks for your [fantastic contributions](https://github.com/barryclark/jekyll-now/commits/master) to the project!

## Contributing

Issues and Pull Requests are greatly appreciated. If you've never contributed to an open source project before I'm more than happy to walk you through how to create a pull request.

You can start by [opening an issue](https://github.com/barryclark/jekyll-now/issues/new) describing the problem that you're looking to resolve and we'll go from there.

I want to keep Jekyll Now as minimal as possible. Every line of code should be one that's useful to 90% of the people using it. Please bear that in mind when submitting feature requests. If it's not something that most people will use, it probably won't get merged. :guardsman:
</details>
