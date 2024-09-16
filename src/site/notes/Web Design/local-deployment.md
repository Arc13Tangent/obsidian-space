---
{"dg-publish":true,"permalink":"/Web Design/local-deployment/","title":"Local deployment of digital garden","noteIcon":"1","created":"2024-09-17T01:14:59.200+08:00","updated":"2024-09-17T01:53:19.177+08:00"}
---


The [Digital Garden plugin](https://github.com/oleeskild/obsidian-digital-garden) is fantastic. It's free and open source, and the service it depends on, Vercel, has a free version.
However, the free version of Vercel has a limit on the number of deployments, which is 100 per day. We may run out of the quota if we want to tune some details.
Thankfully, the plugin's author provided a local deployment method that works well.
I just put some further details in here for documentation.
Full discussion: [Local deployment · oleeskild/obsidian-digital-garden · Discussion (github.com)](https://github.com/oleeskild/obsidian-digital-garden/discussions/160)

1. Clone the digital garden repo (we might have done this before if we've already modified the `custom-style.scss` or other files to customize our garden)
2. In terminal, cd to the repo folder, type `npm install express --save`
```shell ln:false
> cd <path to the repo>
> npm install express --save
```

3. On the same place, add a new file `app.js` with the following content:
```js
const express = require('express')
const app = express()
const port = 8080; 

app.use(express.static('dist'))

app.get('*', (req, res)=>{
  res.redirect("/404")
})

app.listen(port, () => {
  console.log(`Digital garden running on port ${port}`)
})   
```

> [!info] Some modifications
> If we just paste the original code and execute `app.js` in the last step, we might get an error `Error: Cannot find module './netlify/functions/search/search.js'`, so we remove the code related to it.

4. On terminal, execute the following:
```shell ln:false
> npm install
> npm run build
> node app.js
```

5. On the browser, type `localhost:8080`, our garden should appear

After we made some changes, to see the new contents, first type `ctrl` + `c` to interrupt the current one, then type `npm run build` and `node app.js` again.

# References

1. Steensen, O. E. (2024). _oleeskild/obsidian-digital-garden_ [TypeScript]. [https://github.com/oleeskild/obsidian-digital-garden](https://github.com/oleeskild/obsidian-digital-garden) (Original work published 2022)

2. _oleeskild/obsidian-digital-garden · Discussions · GitHub_. (n.d.). GitHub. Retrieved September 16, 2024, from [https://github.com/oleeskild/obsidian-digital-garden/discussions?discussions_q=local](https://github.com/oleeskild/obsidian-digital-garden/discussions?discussions_q=local)
