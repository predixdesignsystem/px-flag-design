# Flag

The Predix Experience Flag module is similar in appearance to the classic OOCSS' [media object](http://www.stubbornella.org/content/2010/06/25/the-media-object-saves-hundreds-of-lines-of-code/), however it utilises `display: table[-cell];` to give us control over the vertical alignments of the text and image (http://csswizardry.com/2013/05/the-flag-object). This module is a fork of the [inuitcss Flag module](https://github.com/inuitcss/objects.flag).

## Demo

You can review button styles and recommended markup and required here: https://github.build.ge.com/pages/PXd/px-flag-design

## Sass Documentation

You can review Sass Documentation here: https://github.build.ge.com/pages/PXd/px-flag-design/sassdoc

## Dependency

Px's Flag module depends on one other Px module:

* [px-defaults-design](https://github.build.ge.com/PXd/px-defaults-design)

## Installation

Install this module and its dependencies using bower:

    bower install --save https://github.build.ge.com/PXd/px-flag-design.git

Once installed, `@import` into your project's Sass file in its Objects layer:

    @import "../px-flag-design/objects.flag";

See [px-getting-started](https://github.build.ge.com/PXd/px-getting-started#a-note-about-relative-import-paths) for an explanation of the `../`

## Import once

All rulesets are wrapped in the following `@if` statement:

    @if import-once('objects.flag') { ... }

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

Flag images have a space between them and the body of the object, the distance defined by these variables:

    $inuit-flag-gutter
    $inuit-flag-gutter--tiny
    $inuit-flag-gutter--small
    $inuit-flag-gutter--large
    $inuit-flag-gutter--huge

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
