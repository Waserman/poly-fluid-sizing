# test-project

> A Vue.js project

## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

```

## Testing

> Right after you run ``npm run dev`` your browser should automatically launched (and make sure it is google Chrome. If not open Chrome manually and navigate to localhost:8081)
> Open Dev Tool and start playing... resize the window width. Should behave as expected. 
> 1. When the width is 640px or less the font size should be 24px
> 2. when the width is 1920px the font size should be 40px

> Now use the device toolbar. Use the responsive option. It seeme like that if you resize the window under 980px you'll notice that the value of the view port width remain the same 980px!
> For that reason, it never reach the 640px media query, hence never set the font size to the right value of 24px at the right view port width. 