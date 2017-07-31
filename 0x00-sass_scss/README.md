# 0x00. Sass & Scss

#### Web Stack programming ― Front-end

### Tasks:

Task 0: prints Hello world in the debug output.

File: 0-debug_log.scss

```
$ sass 0-debug_log.scss | head -n 0
0-debug_log.scss:2 DEBUG: Hello world
$
```

Task 1: A Sass file that assigns the text color #3D3D3D to the HTML tags body and p.

File: 1-color_variable.scss
```
$ sass 1-color_variable.scss | tail -n +2
body {
  color: #3D3D3D; }

p {
  color: #3D3D3D; }
$
```

Task 2: Write a Sass file that assigns:

* The text color #3D3D3D to the HTML tags body and p
* The background color #6D6D6D to the HTML tags body and h2

File: 2-color_variables.scss

```
$ sass 2-color_variables.scss | tail -n +2
body {
  color: #3D3D3D;
  background-color: #6D6D6D; }

p {
  color: #3D3D3D; }

h2 {
  background-color: #6D6D6D; }
$
```

Task 3: Write a Sass file that assigns:

* No margin or padding in body tags
* Margin 10px to all of the p tags inside body tags
* Must use nested declarations

File: 3-nested_tag.scss

```
$ sass 3-nested_tag.scss | tail -n +2
body {
  margin: 0px;
  padding: 0px; }
  body p {
    margin: 10px; }
$
```

Task 4: Write a Sass file that assigns:

* Text color #3D3D3D to elements inside body tags
* Text color #FF0000 to any elements of class .red inside body tags
* Must use nested declarations

File: 4-nested_class.scss

```
$ sass 4-nested_class.scss | tail -n +2
body {
  color: #3D3D3D; }
  body .red {
    color: #FF0000; }
$
```

Task 5: Write a Sass file that assigns:

* Text color #3D3D3D to elements inside body tags
* Text color #FF0000 to any elements of class .red that are the first children of the body
* Must use nested declarations

File: 5-nested_child.scss

```
$ sass 5-nested_child.scss | tail -n +2
body {
  color: #3D3D3D; }
  body > .red {
    color: #FF0000; }
$
```

Task 6: Write a Sass file that assigns:

* Text color #FF0000 to button tags
* When the user hovers over button tags, text color should change to #00FF00
* Must use nested declarations

File: 6-nested_hover.scss

```
$ sass 6-nested_hover.scss | tail -n +2
button {
  color: #FF0000; }
  button:hover {
    color: #00FF00; }
$
```

Task 7: Write a Sass file that assigns:

* Font size 14px to all body tags
* Font size 16px to all h1 tags inside body tags
* Font size 12px to h1 tags of class .smaller inside body tags
* Must use nested declarations

File: 7-nested_deeper.scss

```
$ sass 7-nested_deeper.scss | tail -n +2
body {
  font-size: 14px; }
  body h1 {
    font-size: 16px; }
    body h1.smaller {
      font-size: 12px; }
$
```

Task 8: Write a Sass file that assigns:

* Margin left and right at 10px to body tags
* Margin left and right at 15px to div tags
* Must use a mixin

File: 8-mixin_margins.scss

```
$ sass 8-mixin_margins.scss | tail -n +2
body {
  margin-left: 10px;
  margin-right: 10px; }

div {
  margin-left: 15px;
  margin-right: 15px; }
$
```

Task 9: Write a Sass file that assigns:

* Font size 12px to all tags of class .info
* Text color #00FF00 to all tags of class .success and extend style of the class .info
* Text color #FF0000 to all tags of class .warning and extend style of the class .info

File: 9-extend_list.scss

```
$ sass 9-extend_list.scss | tail -n +2
.info, .success, .warning {
  font-size: 12px; }

.success {
  color: #00FF00; }

.warning {
  color: #FF0000; }
$
```

Task 10: Write a Sass file that assigns:

* Text color $red from 10-colors.scss to the class .red
* Text color $green from 10-colors.scss to the class .green
* Text color $blue from 10-colors.scss to the class .blue
* Must use @import

File: 10-import_colors.scss

```
$ cat 10-colors.scss
/* All my colors */
$red: #FF0000;
$green: #00FF00;
$blue: #0000FF;
$ sass 10-import_colors.scss | tail -n +3
.red {
  color: #FF0000; }

.green {
  color: #00FF00; }

.blue {
  color: #0000FF; }
$
```

Task 11: Write a Sass file that creates a class for each name in the list $list-names and assigns the background image based on the name (example below):

* Must use @import
* Must use @each statement

File: 11-loop_photos.scss

```
$ cat 11-photos.scss
/* All names */
$list-names: julien john sam damian;
$ sass 11-loop_photos.scss | tail -n +3
.photo-julien {
  background: image-url("photos/julien.jpg") no-repeat; }

.photo-john {
  background: image-url("photos/john.jpg") no-repeat; }

.photo-sam {
  background: image-url("photos/sam.jpg") no-repeat; }

.photo-damian {
  background: image-url("photos/damian.jpg") no-repeat; }
$
```

Task 12: Write a Sass file that creates H* tags, where '*' is the size of the font used.

* h1 must have font size equal to 1px, h2 must have font size equal to 2px, etc.
* Must create H* tags from 1 to 5
* Must use @for statement

File: 100-loop_header.scss

```
$ sass 100-loop_header.scss | tail -n +2
h1 {
  font-size: 1px; }

h2 {
  font-size: 2px; }

h3 {
  font-size: 3px; }

h4 {
  font-size: 4px; }

h5 {
  font-size: 5px; }
$
```

Task 13: Write a Sass file that creates classes with different width:

* col-1 with width equals to 100%
* col-2 with width equals to 50%
* col-3 with width equals to 33.3333333333%
* col-4 with width equals to 25%
* Must create .col-* class from 1 to 4
* Must use a @for statement

File: 101-loop_col.scss

```
$ sass 101-loop_col.scss | tail -n +2
.col-1 {
  width: 100%; }

.col-2 {
  width: 50%; }

.col-3 {
  width: 33.3333333333%; }

.col-4 {
  width: 25%; }
$
```

Task 14: Write a Sass file that assigns:

* Font size 20px to h1 tags
* Font size 14px to h1 tags, when your screen width is smaller than 320px

 File: 102-media_query.scss

```
$ sass 102-media_query.scss | tail -n +2
h1 {
font-size: 20px; }
@media screen and (max-width: 320px) {
  h1 {
    font-size: 14px; } }
$
 ```

Task 15: Write a Sass file that assigns:

* Font size 20px to h1 tags
* Font size 18px to h1 tags, when your screen width is smaller than 960px
* Font size 16px to h1 tags, when your screen width is smaller than 640px
* Font size 14px to h1 tags, when your screen width is smaller than 320px
* Text color #1D1D1D to h1.small tags, when your screen width is smaller than 320px

File: 103-media_query.scss

```
$ sass 103-media_query.scss | tail -n +2
h1 {
  font-size: 20px; }
  @media screen and (max-width: 960px) {
    h1 {
      font-size: 18px; } }
  @media screen and (max-width: 640px) {
    h1 {
      font-size: 16px; } }
  @media screen and (max-width: 320px) {
    h1 {
      font-size: 14px; }
      h1.small {
        color: #1D1D1D; } }
$
```

Task 16: Write a Sass file that sorts the variable $list_to_sort and prints the sorted list in the debug output.
File: 104-sort_strings.scss

```
$ cat 104-sort_list.scss
$list_to_sort: john anna zoe kim felicia carrie;
$ sass 104-sort_strings.scss | tail -n +2
104-sort_strings.scss:64 DEBUG: anna carrie felicia john kim zoe
$
```


## Useful Links:

Read:

* [Sass Basics](http://sass-lang.com/guide)
* [Sass control directives: @if, @for, @each and @while](http://thesassway.com/intermediate/if-for-each-while)

References:

* [Sass references](http://sass-lang.com/documentation/file.SASS_REFERENCE.html)
* [The Sass Way](http://thesassway.com/)
* [Intro to Sass](http://callmenick.com/post/an-introduction-to-sass-scss)
