## Web Components Overview

**Problems we're solving**

* Difficult to create simple UI widgets
* Frameworks require lots of code to create UI widgets
* Not interoperable

Web components == less code, less confusion

**What are web components?**

Not just one particular thing.  It's a collection of technologies.

**Custom Elements**

* Declarative
* Meaningful (semantic?)
* Common way to extend / reuse

**Templates**

Native client side templating

* Use DOM to scaffold DOM
* Parsed not renderd
* Content is inert until cloned

**Shadow DOM**

DOM and CSS scoping

**HTML Imports**

Mainly used for importing custom elements

Vulcanize

## Polymer

Polymer's job is to do two things:

1. Polyfill with webcomponents.js
2. Syntactic sugar with polymer.js

(data binding?)

**Creating Custom Elements**

    document.registerElement('paper-tabs', {
        prototype: Object.create(HTMLElement.prototype)
    });

And with Polymer...

    <polymer-element name="paper-tabs">
        ...
    </polymer-element>

**Creating Templates**

    <template>
    
    </templates>

And with Polymer...

    <template>
        <ul>
            <template repeat="{{user, i in users}}">
                <li>{{user.name}}</li>
            </template>
        </ul>
    </template>

(you get two way data binding)

**Shadow DOM**

    var shadow = el.createShadowRoot();
    shadow.innerHTML = "<style>h1 {color: red;}</style>";

And with Polymer...just add a stylesheet within your template.

## Components

Defined interface for interacting with components

Google has developed two sets of elements.

1. core-elements
2. paper-elements

**Core Elements**

Use `core-header-panel` with a `core-toolbar` and a `div.content`.

`core-drawer-panel` is a responsive container with a `div[drawer]` and `div[main]`.

**Paper Elements**

These elements are based on the principles of material design.

`paper-checkbox` provides ink effect animations when you're checking the box

`paper-ripple` is a reactive ink effect for indicating a click/touch action

`paper-shadow` is a dynamic shadow for conveying depth and spatial relationships (changed in new release, so wrap your component in `paper-shadow`)

**Styling**

`/deep/` and `::shadow`

## Apps

* Chrome Status
* Polymer designer tool

## In production

* Github
* Salesforce Mobile SDK

## APIs as Elements

* Google Maps
* Google Analytics
* Google Drive
* Google Calendar

