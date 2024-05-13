# Links and images

- See links-and-images

## Opening link in a new tab

- The method shown above opens links in the same tab as the webpage containing them. This is the default behaviour of most browsers and it can be changed relatively easily. All we need is another attribute: the target attribute.

- While href specifies the destination link, target specifies where the linked resource will be opened. If it is not present, then, by default, it will take on the _self value which opens the link in the current tab. To open the link in a new tab or window (depends on browser settings) you can set it to _blank as follows:

- <a href="https://www.theodinproject.com/about" target="_blank" rel="noopener noreferrer">About The Odin Project</a>

- target specifies where the linked resource will be opened - if not present - will default to _self, which opens the link in the current ab

- To open in a new tab or window, you can set it to _blank

- rel is used to describe the relation between the current page and the linked document

- noopener value prevents the opened linnk from gaining access to the webpage from which it opened

- The noreferrer value prevents the opened link from know which webpage or resouce was a link or reference

## Absolute and relative links

### Absolute links

- Links to pages on other websites on the internet are called absolute links
- typical is protocoll://domain/path

### Relative links

- Links to other pages within our own website are relative links

- Do not include the domain name

## Images

- Display via <img> ~ it is self closing

- Alt: alternative text ~ will describe the image for screen readers