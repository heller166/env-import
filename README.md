# env-import
Configure environment variables with dotenv in one absolute import using ES6 import syntax.

I made this because ESLint was complaining about my enviroment variables configuration file relative import being before the absolute imports
```js
// import dotenv in env.js file and run dotenv.config() there
import './env';
// other absolute imports
``` 
or any code being before imports 
```js
import dotenv from 'dotenv';
dotenv.config();
// other absolute imports
``` 
and some of dependecies rely on environment variables being configured to function properly (like [api-error-handler](https://github.com/expressjs/api-error-handler) in [here](https://github.com/expressjs/api-error-handler/blob/master/index.js#L4))  

## Usage

```js
// With .env in your root directory

import 'env-import'

// Now all environment variables are configured
```

