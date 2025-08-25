# Drawbacks and limitations

> DRAFT

PDF files are one of the most common and simple way for distributing content over the network.

As you proabbly know, there is one big player in the room, Adobe, that offers both PDF creators and readers. They are of high quality but they are also heavy and are not available for every device or are not the most common choice for many users and usages.

There are many alterantives and some are rather popular: so you can't be sure that your PDF will be opened with a Reader by Adobe that support most interactive features.

Nowadays, the biggest contenders are browsers: both on mobile and desktop they provide their own PDF readers.  
While the PDF readers that are built into the browsers are slimmer, and faster, and do a good job in rendering the content, they do not have a great -- if at all -- support for PDF forms and for interactive content.

Generally speaking, it's not advised to distribute PDF forms if you're not in a _controlled environment_:

- Many PDF viewers do not intend to fully implement PDF specifications.
- Often, the primary target is clearly not filling PDF forms.
- They do not support most PDF form submission modes (by design, some can probably only work properly in Adobe products).

One further drawback, is that PDF have a fixed layout and filling a form on mobile devices might be challenging.

## Known issues

- Text typed in Scribus into a PDF text field will be rendered without line breaks at least in some readers (Firefox, Okular).  
  You can switch the fields to a _normal_ text frame by switching _PDF Options > Is PDF annotation_ checkbox_ in the context menu.
