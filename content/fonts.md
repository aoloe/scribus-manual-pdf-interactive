# Fonts for the PDF fields

The PDF specifications specify 14 base fonts that can always be safely used for the content of PDF forms:

- Courier
- Courier
- Courier Bold
- Courier Oblique
- Helvetica
- Helvetica Bold
- Helvetica Bold Oblique
- Helvetica Oblique
- Symbol
- Time Bold Italic
- Time Italic
- Times Bold
- Times Roman
- ZapfDingbats

> PDF prescribes a set of 14 standard fonts that can be used without prior definition. These include four faces each of three Latin text typefaces (Courier, Helvetica*, and Times*), as well as two symbolic fonts (Symbol and ITC Zapf Dingbats ® ). These fonts, or suitable substitute fonts with the same metrics, are required to be available in all PDF consumer applications
>
> [PDF Reference, sixth edition](https://archive.org/details/pdf1.7)

If the target PDF version is higher than 1.4, True Type font fonts can also be used, if they meet all of the following criteria:

- must not be a Type 1 font,
- must not be an OpenType font with PostScript outlines,
- must be fully embeddable.

If the font size is too big to be fully embeddable, one first need to override the default behavior for that specific font in _File > Preferences > Fonts_ and uncheck "Subset".  
Be warned that the size of the PDF will lead to a bigger PDF and might also have issues with some PDF readers.

# Applying the font

The font is applied from the the frame properties. No further formatting on the frame is taken into account for PDF form fields.

## Reader compatibility

Firefox and MS Edge do not seem to respect the font defined in the PDF (neither for the PDF 1.3 nor the PDF 1.4 variant).

Adobe Reader does correctly use the selected PDF standard font when filling a form exported to PDF 1.3 and switch to the TTF option when the form is exported to a PDF version higher than 1.4.
