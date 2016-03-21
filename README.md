# toomanynames_theme

## How to import into a current theme (sub theming)

Go to your new theme's root:
```
  $ cd themes/mytheme/
```
Initialize `npm` if you haven't yet.
```
  $ npm init
```
Then add toomanynames_theme as a dependancy:
```
  $ npm i --save toomanynames_themes
```

### Add Styling

To add the `toomanynames_theme` styling, import the `css/toomanynames_base` file found in the npm package into your main styling file. 

For example, if your theme styling looks like this:
```
mytheme/
|-- layout/
|-- node_modules
|-- source/
    |--css/
      main.styl
```
Then, add the following line in `main.styl`

```
@import "../../node_modules/toomanynames_theme/source/css/toomanynames_base

```

### Add Partials

You don't need to do anything more to access the toomanynames partials. If you had a file like `layout/index.ejs` in your main theme, you could just do this:

```
<%- partial('_partial/navigation') %>
```
This will first look for definitions of partial in your local partials, if not in there it will grab it from `toomanynames_theme`.
