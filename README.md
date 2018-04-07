# Pagination component for Vue

## Props

| Name       | Type     | Default   | Description       | Required |
| ---        | ---      | ---       | ---               | --- |
| perItem    | String   | null      | item limit for one page | True |
| data     | Array   | []      | Array of objects which represent your data | False |
| buttonStyles   | Object   | {}      | Styles for button customization | False |
| activeButtonColor   | String   | 'transparent'      | Current active page button color | False |

e.g for buttonStyles `btnStyles: {
          boxSizing: 'border-box',
          cursor:'pointer',       
          border: '1px solid #ddd',
          verticalAlign:'center',
          background: 'transparent',
          padding: '8px 10px',
          fontSize: '14px',
          lineHeight: '10px',
          height: '30px',
          //marginRight:'5px'
        }`


## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build
```

For detailed explanation on how things work, consult the [docs for vue-loader](http://vuejs.github.io/vue-loader).
