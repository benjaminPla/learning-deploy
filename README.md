# Deploying Vite App to GitHub Pages

_npm 6_
```
npm create vite@latest my-vue-app --template vue
```

_npm 7_
```
npm create vite@latest my-vue-app -- --template vue
```

_vite.config.js (add base property)_
_To be more precise, your base url will be /repo-name/._
```
import { defineConfig } from 'vite'
import vue from '@vitejs/plugin-vue'

export default defineConfig({
  base: '/learning-deploy/',
  plugins: [vue()]
})
```

$ npm run build

$ git add dist -f

$ git commit -m 'Add dist'

$ git subtree push --prefix dist origin gh-pages
