# SkyWay JS

## Including the sdk from the CDN

Include the following script tag in your html.

```html
<script type="text/javascript" src="https://cdn.webrtc.ecl.ntt.com/skyway-latest.js"></script>
```

You can then use the `Peer` object to start connecting.
For more details, check out the [Tutorial](https://webrtc.ecl.ntt.com/en/js-tutorial.html).

## Installing using npm

With [npm](https://npmjs.org/) installed, run

    $ npm install -g skyway-sdk

You can then use `require` or `import` to import the package.

```js
// require
const Peer = require('skyway-sdk');
const peer = new Peer({key: 'your-api-key'});

// import
import Peer from 'skyway-sdk';
const peer = new Peer({key: 'your-api-key'});
```

## Examples

You can use `/examples` directory for checking your development code.

Follow these steps.

- Modify your key
  - e.g.) `sed -i -e "s/<YOUR_KEY_HERE>/12341234-abcd-1234-abcd-1234567890ab/g" examples/key.js`
  - The key can be obtained from https://webrtc.ecl.ntt.com/en/ .
- Start server on project root
  - e.g.) `python -m SimpleHTTPServer 8000`

## Contributing

### Setting up

Make sure you have nodejs installed. Run `npm install` to get started and to set up dependencies.

```sh
# run eslint
npm run lint

# run all unit tests
npm run test # OR npm test OR npm t

# build the library
npm run build
```

After making changes in `src/`, you run

- `npm run lint` to validate
- `npm test` to run tests

then the `npm run build` and build `skyway(.min).js` which is stored in `dist` directory!
