<!-- slide:break -->

### Thoughts on Documentation
My general thought process is that if I see something that I think I can be improved, just don't complain about it, but offer a suggestion.

So my thoughts turned to the documentation that's available for JNode. What could we do to improve the documentation, and what do I mean when I say improve it. Documentation is difficult, and can be boring if you don't have the mindset for it. It's also extremely important for new and old users to have a robust level of documentation to support the project.

One of the obvious solutions is a wiki, however wiki's require monitoring and administration and servers. Another solution, which JNode is currently doing, is centralizing the documentation on a CMS but limiting the rights of the people who can modify it. This can work pretty well but can suffer for the same reason that wiki's do which is the lack of man power in a slow moving, large project.

#### My recommendation is to push the core documentation into the source code, as a project in it's own right.
Which provides the following benefits

Documentation is now available offline
There is a history of the documentation
"patches" to the documentation can be made by any user, and in the case of github a pull request can be made.
independent of the lifecycle of the website
The question would be, how would you put the documentation there and in what format.

Documentation needs to be human readable, and editable
Interface into the documentation should be via a browser to provide a professional look and feel
Documentation should try to avoid html Smiling
I put a smiley at the end of the list since I just listed two requirements that would seem to indicate web pages, the problem with web pages is that they really aren't readable and a pain to upkeep and write documentation in without an editor.

So my thoughts went to a combined approach. I would have a main index page which would provide the structure and visual look and feel of the documentation. The documentation itself would be maintained in markdown script to make it as readable as possible in a simple text viewer. The index would also include some javascript that would monitor any anchors for hash locations(#example). An anchor tag that begins with a path formatting(#/foo/bar) would trigger an ajax request that would suck in the defined path, run it through a markdown to html converter, then populate the body with the result. If the anchor link doesn't start with a path (#foo) it would act like the default behavior and update the page accordingly.
