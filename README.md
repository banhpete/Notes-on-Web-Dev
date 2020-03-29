# Notes-on-Web-Deb
## What Can Google Chrome Developer Tools Do:
### March 28th, 2020
#### With CSS
Some of the things the Google Chrome Developer Tools can do with CSS are:
- Edit the styles right there on the page do tests.
- Take a look at the box element which is really helpful when you are trying to what margins, paddings, etc. you should use.
- See what CSS acutally are active or inactive on an element.

See guide from https://developers.google.com/web/tools/chrome-devtools/css/reference

#### With JavaScript
Some of the things the Google CHrome Developer Tools can do with JavaScript are:
- Determine if there is unused JavaScript similiar to determining if there is unused JavaScript. This is through coverage.
- Set breakpoints and follow through the code 
- Set conditional breakpoints so that the code can stop given some variable
- You can purposely call the debugger in your code by just writting "debugger"
- If an element changes and you want to see what happens, you can set a breakpoint on that element
- You can set a breakpoint on specfic AJAX source codes, for example, if you know somewhere in the code the incorrect URL is being called out, you can add a XHR breakpoint so that it breaks when the wrong URL code is called out

#### With Console
Some of the things you can do with the console are:
- Run Javascript as the console is also a REPL (Read–eval–print loop)
- There is a console api where you can use to send more than just simple console messages. For example there's a console.table where you can send a table to the console, and there's a console.error() to send an error message to the console.

See guide from https://developers.google.com/web/tools/chrome-devtools/console/reference

#### With Network
Some of the things Google Chrome Developer Tools can do with network are:
 - Throttle the page so that you can see how long it would take for a page to load on a mobile device. All you have to do is select a throttling option (Fast 3G, Slow 3G, Offline) and then empy cache and hard reload. 
 - Take screenshots while the page loads up to see how it looks like during the build up
 - Block certian resources to see how it changes page or how a page would look without the resource. 
 - View all the files loading, how long it takes to look, see the cookies, headers, etc. This could have been reviewed more but it is hard to find relevancy right now - review further later on.
 
 See guide from https://developers.google.com/web/tools/chrome-devtools/network/reference
 
#### To analyze performance?
Some of the things Google Chrome Developer Tools can do with the website performance are:
- Throttle the CPU so that you can test your website on low-end devices
- Record runtime performance to see data such how much time was used for rendering, scripting, painting, etc.
- See the fps at a given time of the website running
- There's more to this however it is hard to find relevancy right now - to review later on.

## General Web Development
### March 27th, 2020
#### What is Ajax?
AJAX stands for Asynchronous JavaScript and XML
To fully understand what Ajax is, it's importnat to understand how the web worked back in the early 1990s. All websites were based entirely on HTML pages. Anytime someone visited a website, it would be an HTML page that was requested and served, and anytime the website required to change, even for minor reasons, a new HTML page would need to be served, see the model on the left below.
![Model of a webapplication - From Wikipedia](https://upload.wikimedia.org/wikipedia/commons/thumb/0/0b/Ajax-vergleich-en.svg/1024px-Ajax-vergleich-en.svg.png)
Obivously this was extremely inefficient, the website only requires a partial change but the whole page had to be reloaded. This is where a new set of web development techniques was developed in certain browsers which is now known as Ajax. This allowed us to code using Javascript to retrieve data from a server asynchronously (hence 'Aja' in Ajax) to receieve XML data (hence 'x' in Ajax) without disrputing the existing page. So we moved away from the model on the left and moved to the model on the right where servers were not just sending HTML files but data, and there was an additional "Ajax Engine" to coordinate what we were requesting from the server. There has been significant changes to these technologies since its developed, specifically JSON data is used more commonly now instead of XML but the name has stuck.

Some technologies include:
- The XMLHttpREquest
- Fetech()
- jQuery
- Axios 

So Ajax is not a language, or a library, rather it refers to technologies used in web development that allows browsers to send requets to a server in the background while a HTML page is being served or is served already. We often see these technologies in use on pages where changes are always happening like facebook, twitter, etc., and you are only one page. It was developed in certain browsers at first but has long flourished into a staple technologies for browsers.

See notes from https://en.wikipedia.org/wiki/Ajax_(programming) and https://en.wikipedia.org/wiki/XMLHttpRequest.

### March 28th, 2020
#### What is a code linter?
Essentially, it is a tool that goes through your source doe to flag any errors, bugs, etc.

In visual studio code we use ESLint for to analyze Javascript.

These are important for interpreted languages (i.e Javascript or Python) which do not have a compiling phase like C.

See notes from https://en.wikipedia.org/wiki/Lint_(software)

## CSS
### October 27th, 2019
#### Why do we use the "before"?
Based on my experience so far - we use the pseudo element before to add content before an element. W3 does a great example of showing how "before" works: https://www.w3schools.com/cssref/sel_before.asp.
Another great example of using the "before" pseudo element is here: https://codepen.io/banhpete-the-bold/pen/RwwVwPW. What happened here is that the "before" pseudo element was used to insert a background picture before the body tag instead of inserting the background into the body tag itself. This was done so that we can set an image as a background for the whole page and have it fixed such that when we scroll through the page, we only scroll through the contents of the body tag and not the background (see the codepen). If the background picture was inserted into the body this could not happen because - we need to have the image fixed not the content of the body!
