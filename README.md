# Deploying Vite App to GitHub Pages

Go to your vite.config.js file. And add your base url to it.

```
import { defineConfig } from 'vite'
import vue from '@vitejs/plugin-vue'

export default defineConfig({
  base: '/learning-deploy/',
  plugins: [vue()]
})
```

_To be more precise, your base url will be /repo-name/._

$ npm run build
$ git add dist -f


$ git commit -m "Adding dist"

$ git subtree push --prefix dist origin gh-pages
