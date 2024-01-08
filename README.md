# simple PWA

### 1. simple html + css + icon

* local + desktop => OK
* online + desktop => OK
* online + mobile => OK

* offline + desktop => OK (blank)
* offline + mobile => ~OK (should be blank)


HTML links href="style.css", href="circle.svg" to refer to root dir


### 2. add manifest + sw

* local + desktop => OK
* online + desktop => OK
* online + mobile => OK

* offline + desktop => OK (blank)
* offline + mobile => ~OK (should be blank)



## Notes
### Paths
- in HTML, to refer to files in the same directory, use “file_name.ext”
(if “/file_name.ext” is used, then this looks into the root directory - which in case of gh-pages is the gh root url therefore cannot find the file)

- in manifest.json, write   "start_url": "./index.html",   (ie include “./“ so that the app goes to that page irrespective of the home url (ie local, or if via gh-pages)

- in sw.js,  write the resources as follows   "./", "./index.html", "./style.css", … for the same reason
