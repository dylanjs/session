# Session

Middleware for Dylan which provides cookie based sessions.

## Install

`npm install @dylan/session`

## Usage

``` js
const session = require('@dylan/session');
app.use(session({ cookie: 'foo', secret: 'boo' }));
app.get('/foo', (req, res) => {
  req.session.set('hello', 'world');
});
app.get('/boo', (req, res) => {
  req.session.get('hello'); // returns 'world'
});
```

