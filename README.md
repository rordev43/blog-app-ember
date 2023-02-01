# EmberJS Blog Platform

**Disclaimer**: If you are here to deploy or use the EmberJS Blog Platform for your own blogging purposes, please jump to the **Quick Start** section. This repository is tailored for those who wish to contribute to or modify the EmberJS Blog Platform.

The EmberJS Blog Platform is a static site solution that is designed to be a robust and SEO-friendly blogging system. Built atop the EmberJS framework, it can be hosted on numerous static site hosting platforms including AWS S3.

Our platform offers compatibility with various shallow forked themes from popular blogging systems. Crafting your own theme for our platform is straightforward. Utilize the `create-empress-blog-template` utility and you're set to kickstart your theme development.

The EmberJS Blog Platform is user-friendly. Even if you aren't a web developer, you can use this platform effortlessly. Simply author your posts in markdown, and EmberJS's powerful build system will handle the rest.

## Quick Start

```bash
npx ember-cli@latest new your-blog-name
cd your-blog-name
npx ember install empress-blog empress-blog-casper-template
npm start
npm run build -- -prod
```

### Creating Content

```bash
npx ember g author author-name
npx ember g post "Your Blog Post Title"
```

```bash
let ENV = {
  // ... other configurations ...

  blog: {
    title: "Your Blog Title",
    description: "A brief about your blog",
    logo: "/images/logo.png",
    coverImage: "/images/cover.jpg",
    twitter: "your_twitter_handle",
    navigation: [
      { label: 'Home', route: 'index' },
      // ... other navigation items ...
    ]
  },
}
```


### Custom themes

```bash
npm init empress-blog-template theme-name
```