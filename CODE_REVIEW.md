### Task 1: Code fixes and review

**Are there any problems or code smells in the app?**

* There should not be a hardcoded label, names, placeholder etc in the html file. we can use it from any common constant file. 
* Avoid the use on type any. 
* Should add types to each of the parameters and to the function itself to add a return type where it returns some value. 
* Avoid use of `subscribe`, instead use a `async` pipe for Observable. (file `book-search.component.html`).
* Avoid duplication of async pipe for same observable it will cause multiple subscription which is harmfull. (file `reading-list.component.html`).


**Are there other improvements you would make to the app? What are they and why?**

* As its a web application design should be correctly allign for all devices. for small mobile devices its not correctly aligned.
* As a standard practice on click of logo `okreads` we should navigate to home page.
* avoid `subscribe` we need to `unsubscribe` always to avoid memory leak, we can add `async` pipe instead. 
* in html files instead of only `b` in ngfor, can use more discriptive variable. 
* We can use `safe navigation operator` to prevent error throwing when object doesn't exist. (`.html` files).


**Lighthouse accessibility issue**

* Buttons do not have an accessible name. (added aria label to the search button in `book-search.component.html`)
* Background and foreground colors do not have a sufficient contrast ratio. (changing .header background color to dark pink `app.component.scss`)
* Background and foreground colors do not have a sufficient contrast ratio. (changing .empty background color to dark grey `book-search.component.scss`)


**Manual accessibility issue**

* Best practice to use <a> tag on navigation and for inpage click activity we can use button and with the help of css we can clear the button css to look like link. (file `book-search.component.html`)
* Image should have `alt` attribute which describes about the image. (file `book-search.component.html` and `reading-list.component.html`)
* With the help of `attr.aria-lable` we can give meaningful name to the element. (file `book-search.component.html` and `total-count.component.ts`)
* For organize content need to add landmark. (file `book-search.component.html`).


