title: Dynamic Reactive Tables with LemonadeJS,
keywords: LemonadeJS, two-way binding, frontend, javascript library, javascript plugin, javascript, reactive, react, examples, table,
description: How to create a reactive dynamic table from an array of objects using the loop attribute.

Table
=====

How to create dynamic tables from a JavaScript array of objects. The following example uses `:loop` attribute.  
  

Basic example
-------------

Creating a dynamic HTML table using LemonadeJS.  

### Source code

```html
<html>
<script src="https://lemonadejs.net/v4/lemonade.js"></script>
<div id='root'></div>
<script>
function Component() {
    const self = this;

    self.rows = [
        { title:'Google', description: 'The google search engine...' },
        { title:'Bing', description: 'The microsoft search engine...' },
        { title:'Duckduckgo', description: 'Privacy in the first place...' },
    ];

    // Dynamic table
    return `<table>
        <thead><tr><th>Title</th><th>Description</th></th></thead>
        <tbody :loop="self.rows">
        <tr><td>{{self.title}}</td><td>{{self.description}}</td></tr>
        </tbody>
    </table>`;
}
lemonade.render(Component, document.getElementById('root'));
</script>
</html>
```
```javascript
import lemonade from "lemonadejs";

export default function Component() {
    const self = this;

    self.rows = [
        { title:'Google', description: 'The google search engine...' },
        { title:'Bing', description: 'The microsoft search engine...' },
        { title:'Duckduckgo', description: 'Privacy in the first place...' },
    ];

    // Custom components 
    return `<table>
        <thead><tr><th>Title</th><th>Description</th></th></thead>
        <tbody :loop="self.rows">
        <tr><td>{{self.title}}</td><td>{{self.description}}</td></tr>
        </tbody>
    </table>`;
}
```