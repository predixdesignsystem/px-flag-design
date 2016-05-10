# Flag

The Predix UI Flag module is similar in appearance to the classic OOCSS' [media object](http://www.stubbornella.org/content/2010/06/25/the-media-object-saves-hundreds-of-lines-of-code/), however it utilises `display: table[-cell];` to give us control over the vertical alignments of the text and image (http://csswizardry.com/2013/05/the-flag-object). This module is a fork of the [inuitcss Flag module](https://github.com/inuitcss/objects.flag).

## Dependency

Predix UI's Flag module depends on one other Px module:

* [px-defaults-design](https://github.com/PredixDev/px-defaults-design)

## Installation

Install this module and its dependency using bower:

    bower install --save px-flag-design

Once installed, `@import` into your project's Sass file in its Objects layer:

    @import "px-flag-design/_objects.flag.scss";

## Usage

These flags are available and, if needed, should be set to `true` prior to importing the module:

    $inuit-enable-flag--tiny
    $inuit-enable-flag--small
    $inuit-enable-flag--large
    $inuit-enable-flag--huge
    $inuit-enable-flag--rev
    $inuit-enable-flag--flush
    $inuit-enable-flag--top
    $inuit-enable-flag--bottom
    $inuit-enable-flag--responsive

The following variables are available for use in the module:

    $inuit-flag-collapse-at

Basic usage of the Flag module uses the required classes:

    <figure class=flag>
        <img src=... alt=... class=flag__img>
        <figcaption class=flag__body>
            ...
        </figcaption>
    </figure>

The only valid children of the `.flag` node are `.flag__img` and`.flag__body`.

## Options

Other, optional classes can supplement the required base classes:

* `flag--flush`: remove the space between the image- and text-content.
* `flag--[tiny|small|large|huge]`: alter the spacing between the image and text-content.
* `flag--top`: Vertically top aligned flag objects.
* `flag--bottom`: Vertically bottom aligned flag objects.
* `flag--rev`: reverse the horizontal rendered order of the image and text-content.
* `flag--responsive`: a very basic responsive implementation of the flag object. Pragmatic; far from perfect.

For example:

    <figure class="flag flag--flush flag--rev">
        <img src=... alt=... class=flag__img>
        <figcaption class=flag__body>
            ...
        </figcaption>
    </figure>

view the full API [here](http://predixdev.github.io/px-flag-design/)
