An experimental way of displaying Bill information in Github, using data from [the UK Parliament Bill pages](https://web.archive.org/web/20100423150332/http://services.parliament.uk/bills/2009-10/digitaleconomy/documents.html "The Digital Economy Bill on www.parliament.uk")

Bill information published subject to [Parliamentary Copyright](https://web.archive.org/web/20100423150332/http://www.parliament.uk/site_information/parliamentary_copyright.cfm "Parliamentary Copyright")

Uses [pdftotext](http://www.foolabs.com/xpdf/download.html) and a [simple ruby parser](http://github.com/lizconlan/bill-pdf-parser) to convert the pdf documents into comparable text

Github tags are used to reflect Parliament's Bill numbering system which allocates each printed Bill a number which is unique within a Parliamentary session (the part of the tag name after the dash represents the current session in terms of 2 digit years - this is not how Parliament does this on the Bill documents, but I think this approach is readable at a glance, despite the obvious looming Century Bug I've built in)

Each commit of the Bill text represents a printed version of the Bill with the commit text set to the Bill stage, with the House name in brackets at the end where applicable. "House of " was deliberately omitted from the House names to try to minimise the risk of the information being lost when running certain comparison functions which may truncate the commit messages; "HoC" and "HoL" were judged to be too cryptic and too easy to mix up, especially if the messages were not displayed in full

You can compare 2 different versions of a Bill using Github's compare function:  
[http://github.com/lizconlan/bill-compare-proto/compare/HL032-0910...HL044-0910](http://github.com/lizconlan/bill-compare-proto/compare/HL032-0910...HL044-0910)

Or you can run blame against the latest version of the Bill to see when the current text was introduced:  
[http://github.com/lizconlan/bill-compare-proto/blame/master/DigitalEconomyBill.txt](http://github.com/lizconlan/bill-compare-proto/blame/master/DigitalEconomyBill.txt)


