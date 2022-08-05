Abstracts

As we’ve talked about a fair deal so far, abstracts are things like variables and mixins that aren’t directly compiled to CSS, but instead are used in other places.
I tend to separate things quite a bit here, with separate files for colors, font related things, breakpoints, and so on. I do group all my mixins into a single mixins file, and the same with my functions though.

Base

This folder contains my reset, my custom properties (inside the \_root.scss file), and all the more generic styling for my body and other simple element selectors where we can set up some general styling and let the cascade take care of things.

Components

Every component I make gets it’s own partial file, making it very easy to find what you’re looking for.

Layout

I try to keep my layout classes fairly generic and separated from specific components.
The idea is layout classes create a layout, and then components live within those layouts.
In here I have things like a layout with a sidebar, equal column layouts, grid systems, etc. Generally, they tend to be as generic as possible.
Once again, every layout I create gets its own partial to make it easy to find.
We’ll add a few layout classes that I use in most of my projects a little later on in the course.

Utilities

As with my components and layout, every utility I create gets its own partial, except for things like colors and font sizes, where all of the respective classes live in the one partial file.

I also include things like my .container here, and a few other things that you might feel like they could go under layout/ instead.

We’ll add some useful utilities I use on most of my projects a little later on.

Vendor

Vendor is for 3rd party CSS, so for plugins or other things you might be bringing in. I use prism for handling syntax highlighting, so I drop their CSS file in there. This could also be the home for some 3rd party lightbox, or even something as big as Boostrap.

main.scss

This is where everything gets brought in, with the exception of my abstracts.

Each folder above with have an \_index.scss, and then I’ll have:

@use 'base';
@use 'components';
@use 'layout';
@use 'utilities'
@use 'vendor';
