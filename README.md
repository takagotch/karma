### karma
---
https://github.com/karma-runner/karma

```
npm install karma --save-dev
npm install karma-jasmine karma-chrome-launcher jasmine-core --save-dev
./node_modules/karma/bin/karma start
npm intall -g karma-cli
```

```js
// karma.conf.js
module.exports = function(config){
  config.set({
    basePath: '../..',
    frameworks: ['jasmine'],
  });
};

module.exports = (config) => {
  config.set({
    basePath: '../..',
    frameworks: ['jasmine'],
  });
}

require('ts-node').register({
  compilerOptions: {
    modules: 'commonjs'
  }
});
require('./karma.conf.ts');

costomHeaders: [{
  match: '.*foo.html',
  name: 'Service-Worker-Allowed',
  value: '/'
}]

httpsServerOptions: {
  key: fs.readFileSync('server.key', 'utf8'),
  cert: fs.readFileSync('server.crt', 'utf8')
},

function CustomMiddlewareFactory (config){
  return function (request, response, /* next */){
    response.writeHead(200)
    return response.end("content!")
  }
}

middleware: ['custom']
plugins: [
  {'middleware:custom': ['factory', CustomMiddlewareFactory]}
]

mime: {
  'text/x-typescript': ['ts', 'tsx']
  'text/plain': ['mytxt']
}

proxis: {
  '/static': 'http://gstatic.com',
  '/web': 'http://localhost:9000',
  '/img/': '/base/test/images/',
  '/prxyfied': {
    'target': 'https://myserver.localhost',
    'changeOrigin': true
  }
}

proxyReq: function(proxyReq, req, res, options){
  proxyReq.setHeader('Referer', 'https://www.example.com/')
}

proxyRes: function(proxyRes, req, res){
  if(proxyRes.headers['set-cookie']){
    proxyRes.headers['set-cookie'] = proxyRes.headers['set-cookie'].map(function(cookie){
      return cookie.replace(/\s*secure;?/i, '');
    })
  }
}
```

```
{
  level: string,
  format: string,
  path: string,
  terminal: boolean
}
```


