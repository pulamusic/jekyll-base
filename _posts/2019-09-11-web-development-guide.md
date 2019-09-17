---
layout: post
title: "web development guide"
date: 2019-09-11 11:38:00
categories: coding
---
I know the title of this post sounds a bit highfalutin, but it is actually just notes from a [YouTube video on the state of web development in 2019](https://youtu.be/UnTQVlqmDQ0) done by Brad Traversy of Traversy Media. I'm just going to list out my notes, since that seems to be my style in Markdown.

* **Basic tools**: No big secrets here.
  - Text editor (I use [Atom](https://atom.io/) though Brad prefers [VSCode](https://code.visualstudio.com/));
  - web browsers ([Chrome](https://www.google.com/chrome/), [Firefox](https://www.mozilla.org/en-US/firefox/), etc.);
  - design & mockup ([XD](https://www.adobe.com/products/xd.html?sdid=12B9F15S&mv=Search&ef_id=CjwKCAjwtuLrBRAlEiwAPVcZBpvFA88xnL4E9f202-tz5zVyEc5HeqW7gmlg1b971DRmIE-JvkIqZhoC2Y0QAvD_BwE:G:s&s_kwcid=AL!3085!3!315233773899!b!!g!!experience%20design%20adobe), [Photoshop](https://www.adobe.com/products/photoshop.html), [Sketch](https://www.sketch.com/), [Figma](https://www.figma.com/), etc.);
  - 3rd party terminal ([Git Bash](https://gitforwindows.org/), [WSL](https://github.com/goreliu/wsl-terminal), [iTerm2](https://www.iterm2.com/), [Hyper](https://hyper.is/), etc.)
* **What to learn**: Elements of HTML & CSS (the first thing to learn)
  - Semantic HTML5 elements;
  - basic CSS (positioning, box model, etc.);
  - flexbox & CSS grid;
  - CSS variables (custom properties);
  - browser dev tools.
* **Responsive layout**: A modern necessity in web development for different devices
  - set viewport;
  - fluid widths;
  - media queries;
  - rem instead of px;
  - mobile first, stacked columns.
* **Basic deployment**: Learn how to deploy a static website
  - Register a domain name ([Namecheap](https://www.namecheap.com/?gclid=CjwKCAjwtuLrBRAlEiwAPVcZBnQDnaDyomFkWftM67kv1xWYm6eyVMGgGeOjhOjtpDiNsR2Fn8JmBxoCpz8QAvD_BwE), [Google Domains](https://domains.google/?gclid=CjwKCAjwtuLrBRAlEiwAPVcZBpkRmnV0Z5Otpbu6_jPeYOTPnZ_jB91PMK-sB8e9pPbdkcrcmMAxmBoCnAgQAvD_BwE#/?utm_source=google&utm_medium=cpc&utm_campaign=na-US-all-en-dr-bkws-all-all-lead-b-domains-1007025&utm_content=text-ad-none-none-DEV_all-CRE_323133597017-ADGP_Hybrid+%7C+AW+SEM+%7C+BKWS+~+BMM+%7C+%5B1:1%5D+Google+Domain-KWID_43700040074073940-kwd-22740955676&utm_term=KW_%2Bgoogle%20%2Bdomain-ST_%2Bgoogle+%2Bdomain), etc.);
  - Managed shared hosting or VPS ([Inmotion](https://www.inmotionhosting.com/home-y?gclid=CjwKCAjwtuLrBRAlEiwAPVcZBhUvovqtWsPN60SfLpeDbEuvlDLGck_VL_IYkyftHWcAig0sB1uvohoC6xMQAvD_BwE), [Hostgator](https://www.hostgator.com/web-hosting?utm_source=google&utm_medium=brandsearch&kclickid=008209db-fed7-480b-92be-7a744f8f63f6&kenshoo_ida=NotAssigned&campaign=2025448454&adgroup=79038776529&adid=381262868395&utm_term=hostgator&matchtype=e&addisttype=g&gclid=CjwKCAjwtuLrBRAlEiwAPVcZBgHQPd732wLdJzy_r-SHxQzlhLBOeSU5a4x-LxWnf9wc3_-lh6zSpRoCPiQQAvD_BwE), [Bluehost](https://www.bluehost.com/?utm_source=google&utm_medium=brandsearch&kclickid=008209db-fed7-480b-92be-7a744f8f63f6&kenshoo_ida=Blue%20Host%20IDA&gclid=CjwKCAjwtuLrBRAlEiwAPVcZBrhqmcY__6i9pXapBK99ba7nJwBP8iGydcF07iwV2p6ta_mEGG6rgxoCD7cQAvD_BwE&utm_campaign=affiliate-link_searchbrandpromo_PPC), etc.);
  - FTP, SFTP file upload ([Filezilla](https://filezilla-project.org/), [Cyberduck](https://cyberduck.io/), etc.);
  - Static hosting ([Netlify](https://www.netlify.com/), [GitHub Pages](https://pages.github.com/), etc.)
    - Need to know [Git](https://git-scm.com/) with these options.
* **SASS pre-processor**: Recommended, but not mandatory.
* **Vanilla JavaScript**: Learn the language without libraries or frameworks.

All of this leads one to becoming a **basic front-end developer**, ready for an entry-level job or a freelancing gig.

What's next? Moving toward **full fledged front-end development**.
* HTML/CSS frameworks ([Bootstrap](https://getbootstrap.com/), [Tachyons](https://tachyons.io/), [Foundation](https://foundation.zurb.com/), etc.);
* [Git](https://git-scm.com/) and tooling ([NPM](https://www.npmjs.com/), [Gulp](https://gulpjs.com/), [Webpack](https://webpack.js.org/), etc.);
* Front-end JS frameworks ([React](https://reactjs.org/), [Angular](https://angular.io/), [Vue](https://vuejs.org/), etc.);
* State management ([Redux](https://redux.js.org/), [VueX](https://vuex.vuejs.org/), etc.).

Then, moving on to **back-end development**.
* Server-side languages and databases ([Node.js](https://nodejs.org/en/), [Python](https://www.python.org/), [PHP](https://www.php.net/), etc.);
* Server-side frameworks
  - **Node.js**: [Express](http://expressjs.com/), [Koa](https://koajs.com/), [Adonis](https://adonisjs.com/)
  - **Python**: [Django](https://www.djangoproject.com/), [Flask](https://flask.palletsprojects.com/en/1.1.x/)
  - **PHP**: [Laravel](https://laravel.com/), [Symfony](https://symfony.com/)
* **Databases**: Learn a few databases
  - Relational databases ([MySQL](https://www.mysql.com/), [PostgreSQL](https://www.postgresql.org/), etc.);
  - NoSQL databases ([MongoDB](https://www.mongodb.com/), [Couchbase](https://www.couchbase.com/), etc.);
  - Cloud databases ([Firebase](https://firebase.google.com/), [AWS](https://aws.amazon.com/), etc.);
  - Lightweight databases ([SQLite](https://www.sqlite.org/index.html), [Redis](https://redis.io/), etc.).
* **Content Management Systems**: [Wordpress](https://wordpress.org/) is the king. There are others such as [Drupal](https://www.drupal.org/), but Wordpress really covers a lot.
* **DevOps, Deployment & More**:
  - Deployment: [Linux](https://www.linux.org/), [SSH](https://www.ssh.com/), [Git](https://git-scm.com/), etc.
  - Platforms: [Digital Ocean](https://www.digitalocean.com/), [AWS](https://aws.amazon.com), [Heroku](https://heroku.com), [Azure](https://azure.microsoft.com/en-us/), etc.
  - Virtualization: [Docker](https://www.docker.com/), [Vagrant](https://www.vagrantup.com/), etc.
  - Testing: [Jest](https://jestjs.io/), [Mocha](https://mochajs.org/), etc.

There are a few more topics Brad covered such as machine learning, TypeScript, web assembly, blockchain technologies, etc., but I think I'll stop with the regular old full-stack stuff. This is quite a bit to chew on as it is. I have to say that I have touched on quite a bit of this, though I always feel as if I am starting from scratch where JavaScript and Node are concerned. The idea is to keep moving forward, I guess.
