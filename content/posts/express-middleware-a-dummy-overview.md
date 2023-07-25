---
title: 'Express Middleware: A Dummy Overview'
date: Thu, 19 Jan 2023 00:07:52 +0000
draft: false
tags: ['back-end', 'express', 'nodejs', 'technology']
---

Specific aspects of Web Development elude me even after getting my Associate's in Web Development. Specifically moreover, a lot of the back-end terminology, tools, and concepts. Middleware started off as something which eluded me, but hopefully, I can clarify it and put it in a way that my brain understood it.

Middleware
----------

Express provides some key points I want to highlight in this condensed lesson provided by [expressjs.com](https://expressjs.com/en/guide/using-middleware.html). Middleware can:

*   Execute any code
*   Make changes to teh request and response objects
*   End the request-response cycle
*   Call the next middleware function in the stack

What you can take away from that is middleware allows you to do stuff between the request-response cycle, not only limited to injecting, pulling, and creating information but notably checking credentials as well. You can use middleware as a catch-all solution to direct users to error pages, verify authority, and pull/push information from the client.

An easy example: A user requests a page from you, but you want to inject the current date in the response. Using middleware, we can get the date, and then next() to send the user to the page they requested with whatever information you put in the middleware, in this case. The date.