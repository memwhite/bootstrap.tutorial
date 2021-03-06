# bootstrap.tutorial

This follows the Bootstrap tutorial on Net Ninja:
https://www.youtube.com/channel/UCW5YeuERMmlnqo4oq8vwUpg

Getting Started

-Go to www.getboostrap.com
  -Click Download Bootstrap
  Then,
  -You have a couple options:
    1. Use the CDN links provided (you must be online for these to work)
    2. Download the actual files and put them in your project (you can work offline)
    3. You can click 'Customize' at the top of the page and build your own
      bootstrap package

For this tutorial, I coped the CDN link and pasted it into my html.
  -I placed the minified CSS in the head
  -I placed the minified JavaScript at the very bottom of the body
  -I deleted the optional theme link because I don't need it for this project

  -Lastly, it's important to include a link to jQuery, because Bootstrap has a
    dependency on jQuery.
    -You'll want to go to www.code.jquery.com and copy the minified version,
      then paste it right above the minified JavaScript bootstrap link in the body.

/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/
Bootstrap Tutorial
1. Bootstrap is made up of a 12-column grid system
2. Add you content into the 'rows' and 'columns' using Bootstrap CSS classes
3. Bootstrap will take care of the responsive work for us

Containers, Rows & Columns
-Because Bootstrap takes care of the responsiveness for us, we have to
  format things in a particular way:
  1. Containers surround the whole section of rows and columns
  2. Rows represent a horizontal line of elements
  3. Columns represent the horizontal space that elements take up
    in a row

/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/
Containers:
-Fixed container: 'container'
  -Has a fixed width, which changes at certain breakpoints
  -Has built-in padding of 15px all the way around

-Fluid container: 'container-fluid'
  -Has a fluid width, which stretches to 100% of it's parent element
  -Has built-in padding of 15px all the way around

*once you get down to mobile size screens, they look pretty much
  identical, it's at medium and large screens where you can see the
  differences*

  /\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/
Columns:
  -We assign elements within a row, a column width
  -We do this by using Bootstrap classes:
    ex: col-{size}-{number}
    {size} = the size of the viewport (ex:md,sm,xs)
    {number} = number of columns you want the element to span

Viewport sizes:
  xs(<768px), sm(>=768px), md(>=992px), lg(>=1200px)
Number of Columns:
  any integer between 1 and 12
Example: "col-xs-12" or "col-md-6"

/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/

Offsetting Columns:
-In the example below, the first thumbnail will be offset on xs screens, and then
  will re-set on md screens. On xs screens, it will be offset by 2 columns on each side,
  and will have a total of 8 columns. You then have to tell it when to re-set, which is why
  the following part is included: "col-md-offset-0".

Example of offsetting a column:

  <div class="col-xs-offset-2 col-xs-8 col-md-4 col-md-offset-0 thumb">thumbnail</div>
  <div class="col-xs-12 col-md-4 thumb">thumbnail</div>
  <div class="col-xs-12 col-md-4 thumb">thumbnail</div>

  /\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/

Pushing and Pulling Columns
  Push = moving something to the right
  Pull = moving something to the left
*If you want certain classes to switch places on different screen sizes,
     you should use push and pull on the columns.
*format: col-{size}-{push/pull}-{number of columns to push/pull}
Ex:
<div class="col-xs-12 col-md-6 col-md-push-6 col-lg-8 col-lg-push-0 thumb">Content area</div>
<div class="col-xs-12 col-md-6 col-md-pull-6 col-lg-4 col-lg-pull-0 thumb">Sidebar area</div>

**Remember to reset the next screen size to push/pull = 0 so the formatting
  continues to look as it should as you adjust screen size**

/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/

Text Styles:
-You can override/manipulate the bootstrap default font styles...below are a couple examples:

-See below with the p tag. This will change that first chunk of words within the p tag
  to bolded and larger text.
-See below with the span tag, this will give the word 'fez' the same styling as
  the h2 tags.

h1>They're not aliens, they're Earth…liens!</h1>
<p class="lead">No… It's a thing; it's like a plan, but with more greatness. It's a fez.
  I wear a <span class="h2">fez</span> now. Fezes are cool. It's a fez. I wear
  a fez now. Fezes are cool. Heh-haa! Super squeaky bum time!
</p>
<p>You've swallowed a planet! <strong> I am the last of my species, and I know
  how that weighs on the heart so don't lie to me!</strong> <em> *Insistently* Bow
  ties are cool!</em> Come on Amy, I'm a normal bloke, tell me what normal blokes do!
</p>


/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/

List Styles:

//list-unstyled will take the default styling out of the
list. This includes removing bullet points or numbers.
Example format:
<ul class="list-unstyled"></ul>

//list-inline will change the list from being one on top
of each other, to side by side...as well as remove styling.
Example format:
<ul class="list-inline"></ul>

//You can't add list-inline to <dt> tags, so there is
  another option. This is dl-horizontal
Example format:
  <dt class="dl-horizontal"></dt>
