# Node & Express Bug Hunt!

**READ ALL INSTRUCTIONS BEFORE STARTING**

There are 10 bugs in total, can you find them all? There are hints throughout (???), you should only need to make minor modifcations to 10 lines of code.

**Don't race through the files looking for the issues!** They should all have a console log or error that help you identify them. Read the console so that you know what error will cause each bug. The last one is tricky since it doesn't throw any errors. Document the error, line number and your fix in this README for each of the bugs.

## Setup
```
npm install
npm start
```

> NOTE: A couple of bugs prevent the server from starting.

## Error List

TODO: Add the error here followed by the line of code you fixed.

### Bug 0

`ReferenceError: app is not defined`

Fixed `quote.router.js` line 28: switch `app` to `router`. _This is the solution to the first bug._

### Bug 1

`TypeError: Router.use() requires a middleware function but got a Object`

Added `module.exports = router` to the router file on line 28.

### Bug 2

`Cannot GET /`

Removed quotes from line 8 in the router file: `router.get('/quotes', (req, res)`

### Bug 3

Removed extra curly brace from line 7 of the client file: `url: '/quotes}'`

### Bug 4

Added correct file path to line 17 in server file: `app.use(express.static('server/public'));`

### Bug 5

`TypeError: quotesFromServer is not iterable`

Updated line 5 of router to make the quote list an array: `let quoteList = [];`

### Bug 6

Commented out line 24 of the client because there is no i defined for this loop: `// i += 1;`

### Bug 7

`ReferenceError: quotesList is not defined`

Corrected variable name on line 21 of the router to fix the post request: `quoteList.push(quoteToAdd);`

### Bug 8

`ReferenceError: getQuote is not defined`

Corrected function name in the client on line 52:  `getQuotes();`

### Bug 9

Sourced axios into HTML on line 9 instead of line 10 so that it's sourced above the client.

### Bug 10

## Extra Practice (Optional)

Complete the JS debugging exercises at:

- https://education.launchcode.org/intro-to-professional-web-dev/chapters/errors-and-debugging/exercises.html
