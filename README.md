# ANDROMEDA-SHOCK-2 summary

Live site: https://wmebemandromeda2.netlify.app

The page source is `src/App.jsx`. `app.js` and `styles.css` are built from it and committed, so Netlify serves the folder as it is with no build step.

To rebuild after editing `src/App.jsx`:

```
npm i react@18 react-dom@18 lucide-react@0.460.0 esbuild@0.24 tailwindcss@3.4
npx esbuild src/main.jsx --bundle --minify --jsx=automatic --define:process.env.NODE_ENV='"production"' --outfile=app.js
npx tailwindcss -i <(echo '@tailwind base; @tailwind components; @tailwind utilities;') -o styles.css --minify
```
