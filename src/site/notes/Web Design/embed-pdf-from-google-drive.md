---
{"dg-publish":true,"permalink":"/Web Design/embed-pdf-from-google-drive/","title":"Embed PDFs from Google Drive","noteIcon":"1","created":"2024-09-16T02:15:54.860+08:00","updated":"2024-09-16T03:22:54.123+08:00"}
---


Some of you might be curious about why I put this snippet here, especially since Google already provides a function called "Embed item...".
![Imgur](https://imgur.com/VRmPTQ1.jpeg)

However, if you paste the code that Google gives you, it works locally but breaks after being published to DG:
![Imgur](https://imgur.com/ocYRDuH.jpeg)

I don't know why 😑

---

```html
<iframe src="https://drive.google.com/file/d/1PacJp3YdhrNR9wzc5ylpH6nkcmLvHjVM/preview" 
width="640" height="480" allow="autoplay" aspect-ratio="4 / 4">
</iframe>
```

The result:
<iframe src="https://drive.google.com/file/d/1PacJp3YdhrNR9wzc5ylpH6nkcmLvHjVM/preview" 
width="640" height="480" allow="autoplay" aspect-ratio="4 / 4">
</iframe>

---

# References

1. sharp_blade_457. (2023, February 9). _How to preview external web page link in Obsidian?_ [Reddit Post]. R/ObsidianMD. [www.reddit.com/r/ObsidianMD/comments/10xy6au/how_to_preview_external_web_page_link_in_obsidian/](https://www.reddit.com/r/ObsidianMD/comments/10xy6au/how_to_preview_external_web_page_link_in_obsidian/)

2. _Unable to embed pdf from google drive - Ask for Help_. (2024, February 23). Glide Community. [https://community.glideapps.com/t/unable-to-embed-pdf-from-google-drive/71076/5](https://community.glideapps.com/t/unable-to-embed-pdf-from-google-drive/71076/5)
