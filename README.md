## How to reproduce

This demonstration is concerned with Nuxt's static generation. As the code is, running `npm run generate`, followed by `npx serve .output/public`, will correctly show a red square in the page.

To reproduce the bug, first **delete the `.output` directory** so as to to avoid any form of caching. Then, in the file `pages/index.vue`, change the initial value of `render` to `ref(false)` instead of `ref(true)`.

Then, once again, run `npm run generate` followed by `npx serve .output/public`. As you will see, the `_ipx/` directory **will not** be generated, even though the page requests something from it. In turn, the image will not be available.