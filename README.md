# Calendar

https://observablehq.com/@d3/calendar/2@1169

View this notebook in your browser by running a web server in this folder. For
example:

~~~sh
npx http-server
~~~

Or, use the [Observable Runtime](https://github.com/observablehq/runtime) to
import this module directly into your application. To npm install:

~~~sh
npm install @observablehq/runtime@5
npm install https://api.observablehq.com/d/8994272dc06e0549@1169.tgz?v=3
~~~

Then, import your notebook and the runtime as:

~~~js
import {Runtime, Inspector} from "@observablehq/runtime";
import define from "@d3/calendar/2";
~~~

To log the value of the cell named “foo”:

~~~js
const runtime = new Runtime();
const main = runtime.module(define);
main.value("foo").then(value => console.log(value));
~~~

## GitHub Pages

This repo ships with a GitHub Pages workflow that publishes the repository
contents as a static site. To deploy:

1. Push to the `main` branch.
2. In GitHub, open **Settings → Pages** and set the source to **GitHub Actions**.
3. The workflow will publish `index.html` to your Pages URL.
