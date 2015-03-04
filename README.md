# Flag

The Predix Experience Flag module is similar in appearance to the classic OOCSS' [media object](http://www.stubbornella.org/content/2010/06/25/the-media-object-saves-hundreds-of-lines-of-code/), however it utilises `display: table[-cell];` to give us control over the vertical alignments of the text and image (http://csswizardry.com/2013/05/the-flag-object). This module is a fork of the [inuitcss Flag module](https://github.com/inuitcss/objects.flag).

## Dependencies

Px's Flag module depends on two other Px and inuitcss modules:

* [settings.defaults](https://github.com/inuitcss/settings.defaults)
* [px-functions-design](https://github.sw.ge.com/pxc/px-functions-design)

## Installation

Install this module and its dependencies using bower:

    bower install --save https://github.sw.ge.com/pxc/px-flag-design.git

Once installed, `@import` into your project's Sass file in its Objects layer:

    @import "../px-flag-design/objects.flag";

#### A note about relative @import paths

Paths to a project's Bower dependencies differ depending on whether you are in the project itself (dependencies in some
a Bower managed directory in the project) vs. using the project 'downstream' (dependencies are siblings of the project).
Ideally we want to be able to 'build' in both cases without a lot of magic.

For Sass imports, can use the 'includePaths' option on the Grunt sass task to name a starting point to look for
relative paths. IncludePath 'bower_components/*' in the 'sass' task allows the actual @import paths in Sass files to start
with '../' so that they will resolve in either case described above and make editors happy.

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

    <div class="flag">
        <img src="/path/to/image.png" alt="Alternative text" class="flag__img" />
        <div class="flag__body">
            <p>Text-like content goes here.</p>
        </div>
    </div>

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

    <div class="flag flag--flush flag--rev">
        <img src="/path/to/image.png" alt="Alternative text" class="flag__img" />
        <div class="flag__body">
            <p>Text-like content goes here.</p>
        </div>
    </div>
