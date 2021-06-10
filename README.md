# Enfocus_Switch
Scripts and flows for Enfocus Switch

This package highlights the ability of Switch Scripting to create a best-fit imposition using Apago PDF Constructor. 

Prerequisites:
- Enfocus Switch
- Switch Scripting Module
- Apago PDF Constructor
- PitStop Server

The script looks at trim size vs sheet size and creates a best-fit imposition. In the case of business cards 3.5 x 2 on a 12 x 18 or 13 x 19 sheet size, the script creates a 24-up imposition on the center of the sheet. Bleed is set to 0.625"

Things it does not do, as is:
- Dutch cut impositions
- Cut and stack
- Work with more than one two-sided PDF (no booklets, no multi-page documents)

About the flow:
The Switch flow first checks a PDF file for bleed by checking if the bleed box is bigger than the trim box. Very basic, just to show how and where it can be done. Then the PDF is renamed with "_bleed" or "_no_bleed". PitStop Server is used to adjust the PDF page geometry to accommodate bleed and to set the media box origin consistently to get expected placement from PDF Constructor. Next, the script executes, getting some values directly from the PDF. On successful creation of the imposition, the flow sorts imposed PDF, original PDF and XML file into respective folders.

Sorry, no support is offered for this solution. It is for educational purposes or for a starting point in development. 
