# print-job

This small JavaScript library prints a single HTML container.

## Features

* No popup windows or iFrames
* No moving and replacing HTML


## Documentation


### Print a container
You can pass in any valid selector, but only the first element found will be printed.
```javascript
PrintJob.print('#areaYouWantToPrint');
``` 

You can alternatively pass in an element instead of a selector:
```javascript
let element = document.getElementById('areaYouWantToPrint');
PrintJob.print(element);
```

---

### Print an external image
Because smaller images are used where possible, you can print just the full-size versions of the image by supplying an
external URL
 ```javascript
PrintJob.image('url/to/image/jpg');
```

_**Note:** Because the image has to be fetched, your application code will continue to run after calling this method.
The image will be printed the moment it loads._ 

### Upcoming Features
* Use custom print CSS
* Lifecycle callbacks
    * Before print
    * After print
* Preset jobs (set up the job and print later)
