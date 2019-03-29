# This is a bug relevent to viewport
My original intention is to set page's viewport to 1080px on iPhone8 Plus. Since its device-width is 414px, I set its viewport to `<meta name="viewport" content="width=1080px, initial-scale=0.38333" />` on Chrome 75.0.3736.0 canary (64bit Mac OS). However, font-size of p tag is rendered incorrectly. In `with-a.html`, it should be 16px but rendered with 41.7391px. In `without-a.html`, p tag's content is roughly the same except one `a` charactor in the end. `without-a.html` is rendered correctly. I found font-size in p with this viewport settings is relevent to its length. In other cases, I found it's related to html's struture(which is hard to figure out what difference of structure cause this issue) and `overflow-x` css property.

- `without-a.png` and `with-a.png` shows the different render result.
- `without-a.html` and `with-a.html` is the minimum case to reproduce the issue.

## without-a.png
![without-a.png](https://github.com/07akioni/may-be-a-bug-of-chrome/blob/master/without-a.png?raw=true)
## with-a.png
![with-a.png](https://github.com/07akioni/may-be-a-bug-of-chrome/blob/master/with-a.png?raw=true)