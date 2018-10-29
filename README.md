# How to use Parcel

1. `npm init -y`

2. `npm i parcel-bundler -D`

```bash
X:\final-projects\parcel
├── how-to.md
├── package-lock.json
├── package.json
└── src
   ├── index.html
   └── scripts
      └── index.js
```

3. In `packgae.json`:

```js
 "scripts": {
    "dev": "parcel src/index.html"
  }
```

4. Run `npm run dev`

5. You can use **ES6 module system** without any extra configuration.

6. To use **source maps**, refresh the page.

7. To use **ES6 class properties**:

```js
npm i @babel/plugin-proposal-class-properties -D
```

8. In `.baberc` file:

```js
{
  "plugins": ["@babel/plugin-proposal-class-properties"]
}
```

```bash
x:\final-projects\parcel
├── dist
|  ├── index.html
|  ├── scripts.bcf3243b.js
|  └── scripts.bcf3243b.map
├── how-to.md
├── package-lock.json
├── package.json
└── src
   ├── index.html
   ├── scripts
   |  ├── index.js
   |  └── utils.js
   └── styles
      └── index.scss
```
9. For SCSS Support:

```js
npm i sass
```

10. For production, in `package.json`:

```js
"scripts": {
  "build": "parcel build src/index.html --out-dir prod"
}
```