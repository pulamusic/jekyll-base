---
layout: post
title: "website security"
date: 2018-11-07 14:36:00
categories: coding
---

Here are some notes I wrote for a freeCodeCamp tutorial on the use of HelmetJS and BCrypt as tools for ensuring website security. The same notes, along with the code, can be found in [this GitHub repository](https://github.com/pulamusic/siteSecurityNotes).

---

# Free Code Camp - Applied InfoSec Challenges
====================================================

*See the `app.js` file from this repo for the implementation of these various HelmetJS modules*

#### Notes on the [freeCodeCamp curriculum](https://learn.freecodecamp.org/) on information security with HelmetJS:

1. [Intro to information security with HelmetJS](https://learn.freecodecamp.org/information-security-and-quality-assurance/information-security-with-helmetjs)
2. Install and Require Helmet: `npm install helmet --save`
3. PassedHide Potentially Dangerous Information Using `helmet.hidePoweredBy()`
4. PassedMitigate the Risk of Clickjacking with `helmet.frameguard()`
5. PassedMitigate the Risk of Cross Site Scripting (XSS) Attacks with `helmet.xssFilter()`
6. PassedAvoid Inferring the Response MIME Type with `helmet.noSniff()`
7. Not PassedPrevent IE from Opening Untrusted HTML with `helmet.ieNoOpen()`
8. Not PassedAsk Browsers to Access Your Site via HTTPS Only with `helmet.hsts()`.
9. Not PassedDisable DNS Prefetching with `helmet.dnsPrefetchControl()`
10. Not PassedDisable Client-Side Caching with `helmet.noCache()`
11. Not PassedSet a Content Security Policy with `helmet.contentSecurityPolicy()`
12. Not PassedConfigure Helmet Using the ‘parent’ `helmet()` Middleware
13. Not PassedUnderstand BCrypt Hashes
14. Not PassedHash and Compare Passwords Asynchronously
15. Not PassedHash and Compare Passwords Synchronously

---
#### Other notes on HelmetJS and general website security:

* [HelmetJS site](https://helmetjs.github.io/). Its documentation on the various Helmet modules is thorough and clear.

* For an overview of website security see this [MDN article](https://developer.mozilla.org/en-US/docs/Learn/Server-side/First_steps/Website_security). For a more comprehensive listing of security threats, see this [Wikipedia article on "web security exploits"](https://en.wikipedia.org/wiki/Category:Web_security_exploits), or this [Wikipedia article on cyber attacks](https://www.owasp.org/index.php/Category:Attack).

* Express has its own article which [recommends the use of HelmetJS](https://expressjs.com/en/advanced/best-practice-security.html).

* Check out this two-part article on using HelmetJS to ensure site security: [part 1](https://www.ca.com/en/blog-developers/fasten-your-helmet-js-part-1-securing-your-express-http-headers.html) and [part 2](https://www.ca.com/en/blog-developers/fasten-your-helmet-js-part-2-locking-down-your-content-security-policy.html).

* Check out this article on [why you should always use https](https://mashable.com/2011/05/31/https-web-security/#A0EYy4E1v5qI), and this [Wikipedia overview of https](https://en.wikipedia.org/wiki/HTTPS).

* The following code comes from number 11 above. I had trouble with the `content-security-policy` on my url shortener project, version 1. I'll bet the issue was created by a conflict with the HelmetJS security settings. Notice, in particular, the use of single quotes inside double quotes, as in `"'self'"`. This is a quirk particular to the use of `contentSecurityPolicy()`.

```javascript
app.use(helmet.contentSecurityPolicy({
  directives: {
    defaultSrc: ["'self'"],
    scriptSrc: ["'self'", "trusted-cdn.com"]
  }
}))
```

* **Important**: According to the [freeCodeCamp explanation of number 12 above](https://learn.freecodecamp.org/information-security-and-quality-assurance/information-security-with-helmetjs/configure-helmet-using-the-parent-helmet-middleware), all of the HelmetJS modules except for `noCache()` and `contentSecurityPolicy()` are included with the use of the parent `helmet()` module. They are each demonstrated in the tutorial just for thorough understanding.

#### BCrypt challenges

For some strange reason, freeCodeCamp has included a discussion of the BCrypt npm plugin within its larger discussion of HelmetJS. Check out my separate [Glitch repository notes on BCrypt](https://glitch.com/~bcrypt-challenges-jim).
* Pay particular attention to the code in the `server.js` file. In fact, this stuff is important. Let me copy the code below.

```javascript
'use strict';
const express     = require('express');
const bodyParser  = require('body-parser');
const fccTesting  = require('./freeCodeCamp/fcctesting.js');
const app         = express();

fccTesting(app); //For FCC testing purposes

const bcrypt = require("bcrypt")
const saltRounds = 12;
const myPlaintextPassword = 'sUperpassw0rd!';
const someOtherPlaintextPassword = 'pass123';

bcrypt.hash(myPlaintextPassword, saltRounds, (err, hash) => {
  console.log(hash)
  bcrypt.compare(myPlaintextPassword, hash, (err, res) => {
    console.log(res)
  })
})

app.listen(process.env.PORT || 3000, () => {});
```
