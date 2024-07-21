This demonstration seeks to resolve <https://github.com/sveltejs/kit/issues/7320>.

Things to note:

1. `vite.config.js` features `build.sourcemap = true`
2. Added some flags for Node.js in `package.json`

    ```json
    {
      "scripts": {
        "dev": "NODE_OPTIONS=--enable-source-maps vite dev",
        "build": "vite build",
        "preview": "NODE_OPTIONS=--enable-source-maps vite preview",
      }
    }
    ```

Despite the above, I could not set up breakpoints for server-side source maps in
Chrome Dev tools. The source maps appears, but they are apparently not linked to
Node.js when the dev or preview server launches.
