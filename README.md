# Parcel React Setup with HMR and CSS Modules
I like Webpack, its super powerful, but its a headache to setup. I thought I'd give Parcel a go for this React setup. Once you bend your head around some of the more trivial concepts, it was painless to get going. While I still advocate Webpack as a bundle tool, mainly because of its highly customizable interface, Parcel does a great job of making things super easy and blazing fast. :ghost:

## :straight_ruler: Development
To get started with development:

:clipboard: Clone down the repository

```
git clone https://github.com/dainemawer/parcel-setup.git my-new-project
```

:computer: Start up your local development server

```
yarn start
```
_This will spin up a development server at `http://localhost:1234` - Hot Module Replacement and CSS Modules ready. This should open up your default browser and display:_

![Image of default page for Parcel app](https://i.imgur.com/pBxIEuJ.png)

It can sometimes take a while on the first run to bundle assets.

## :gem: Production

:hammer: To build assets for the server:

```
yarn build
```

# :file_folder: Important Folders

### :nut_and_bolt: src

- All development work should take place here.
- Add components to the components folder
- Use `index.js` for components so that you dont need to important single JS files
- Name component CSS after the component.

### :wrench: dist

- `dist` is created on the fly. any images, js, css and html are added to this folder with hashed keys for cache busting.
- `dist` should be deployed to the server.

# :page_with_curl: Important Files

### .postcssrc

- Enables CSS Module Support
- Configures Autoprefixer
- Feel free to add more PostHTML plugins here

### .posthtmlrc

- Configures a standard PostHTML image plugin that sets width and height on images where `width="auto"`
- Feel free to add more PostHTML plugins here

### .browserslistrc

- Configures what browsers PostCSS / Autoprexifer should support
- Use [http://browserl.ist/](http://browserl.ist/) to grab easy configurations for this file.

### .babelrc

- Configures Babel transpiler plugins, currently it supports `react` as well as `react-hot-loader`

Have a :beer:

