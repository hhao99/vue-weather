# Weather App with Vue

# Start the Project

Create the vue application with vue-cli
'''bash
pnpm create vue weather
'''

We will use vue with typescript and add jsx support, and we will add vue-router and pinia library to support route and state management.

# Update the css framework

Tailwindcss v4 is more performant and easy to configure.

```bash
pnpm i -D tailwindcss @tailwindcss/vite
```

and then update the vite configure

```js
// ...
import tailwindcss from '@tailwindcss/vite'

//...
plugins: [...tailwindcss()]
```

now you can use tailwindcss now, but you need update the default css to use tailwindcss

```css
// .src/assets/main.css
@import 'tailwindcss'
```
