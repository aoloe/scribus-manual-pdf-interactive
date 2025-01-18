# Notes

## (Ab)Using intearctive PDF-Forms

This manual is being written because many people are asking question about creating interative PDF Forms with Scribus.

Before helping you to achieve your goals, we would like to warn you that:

- Scribus is a tool aimed at creating PDFs for print. It can do other things of course, but not always in the most comfortable way.
- PDF is a file format that has been created for sending your printable jobs to a print shop. That's what it can do best.
- Many PDF readers do not or only partially let you fill, send, and/or automate PDF forms: it's very likely that people will have issues with your forms.
- Revisioning and debugging of javascript code in your PDF is painful.

Abusing of PDFs as a poor man's application platform is probably a bad idea. But people want to do it and since Scribus does at least partially support the task, we need to document it, as good as we can.

Alternatives are survey tools and online form builders.

## Alternatives

### Webforms

There are both hosted and self hosted solution:

- https://framaforms.org/ (drupal + webform)
- http://www.formtools.org/
- google

## Date and time

Setting the current date and time in an input field:

    this.getField("Time").value = util.printd("mmm dd, yy h:M", new Date());

## Fonts

Jean Ghali, https://bugs.scribus.net/view.php?id=17379 :

PDF Text Fields have specific limitations vs fonts. If not using one of the base 14 fonts defined by PDF specifications, a font used in a PDF Text Field must follow these properties :
- must not be a Type 1 font
- must not be an OpenType font with PostScript outlines
- must be fully embeddable
Calibri fails the last requirement due to its size. You can change the subsetting behavior of Calibri by going to File > Preferences > Fonts, but changing this behavior can lead to bigger PDF files or unexpected behaviors in PDF Readers.
## Links

- [How to enable the debugger in Acrobat Reader](http://blogs.adobe.com/dmcmahon/2011/05/26/reader-how-to-enable-the-javascript-debugger/)
- [Date and time in PDF forms](https://acrobatusers.com/tutorials/date_time_part2)
