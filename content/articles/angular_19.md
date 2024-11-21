---
title: 'Angular 19 is here!'
description: 'They released a bunch of very interesting stuff, including doubling down in the signals direction'
published_on: 'Nov 21, 2024'
---

::blog-title
Angular 19 just went live!
::

Angular has been doing it again - breaking everything they set up over the last many years and then rebuilding it up. 

But they have been doing a better job of making things easy to migrate compared to what they did when they moved from Angular Js to Angular 2.

<!--more-->

In case you havent watched it you can watch it here - 

<iframe class="my-5 w-full aspect-video h-[300px] sm:h-[450px] md:h-[600px] lg:h-[450px] xl:h-[600px]" width="560" height="315" src="https://www.youtube.com/embed/JvkX2_46gUY?si=GG52xdRFDo22oCHO" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

In case you dont like watching videos much, heres the summary of what they said - 

::blog-list{title="Components & Signals"}
---
itemList:
  - 'Standalone will be true by default (ng update will take care of clearing the existing
    standalone: true wala stuff)'
  - Angular is doubling down on signals
  - input, model, output, viewchild, viewchildren, contentChild, contentChildren signals
    are stable
  - Heres a nice article on viewChild and viewChildren signals here
  - 'This is react hooks all over again '
  - Bunch of new and experimental signals they are pushing out. These will change the
    way we write angular code
---
::

::blog-list{title="Refactoring Tools"}
---
itemList:
  - Automated refactoring tools to convert existing code into signals
  - ng g @angular/core:signal-input-migration moves existing inputs to signal based
    inputs
  - ng g @angular/core:signal-queries-migration moves view child and contentchild to
    respective signals
  - ng g @angular/core:output-migration updates function components to the new output
    signals api (didnt understand this well)
---
::

::blog-list{title="Incremental Hydration"}
---
itemList:
  - Incremental Hydration
  - Instead of hydrating the application all at once
  - This builds upon the deferable views
  - Hydration is built into chunks directly in the server and loaded into
  - defered views in the client. This is for some ultra level optimizations
  - never hydration option makes sure that no javascript is loaded for a given section,
    making static content we put anywhere run much faster
---
::
