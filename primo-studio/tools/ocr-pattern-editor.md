# OCR pattern editor

The OCR pattern editor is a plus-in for the studio and is used for developing patterns for reading scanned documents. To open the editor, click Tools -> OCR pattern editor. At the moment, the editor only supports Microsoft OCR when working with patterns (it is built into Windows OS starting from version 8). This tool is still young and will be improved as we receive feedback from users.

**Screenshot**

The editor is composed of the following components:

* Main menu
* The pattern document recognized image
* Toggle tabs for switching between a pattern document rotations
* Text groups
* Properties

The main menu contains buttons

* Create a pattern
* Open a pattern
* Save a pattern
* Save a pattern as ...
* Test a pattern
* Test an image
* Settings

When creating a new pattern, click the «Create pattern» button, then select the file with the scanned reference document. This file will be recognized by OCR, text blocks will be highlighted in it (marked with red rectangles), and the resulting image along with the blocks will be displayed on the screen.

When working with recognized documents, the main entities are anchor and group. An anchor is a text block that is a reference point when searching for text groups (top, bottom, left, and right of the anchor). A group is a text blocks group that form useful data and are positioned in an unambiguous position relative to the selected anchors, or located in the specified coordinates (proportional to the image size).

To work with block properties, click on the desired block red rectangle. Each text block found has the following properties:

* Name
* Text
* Anchor
* Case
* Whitespaces
* Regular expression
* Fuzzy

The Name property is mnemonic and is used for further pattern development. The Text property is the basis for searching for anchors in recognized documents. The Anchor property determines whether this block can be considered an anchor. The Case property determines whether the text should be case-sensitive when searching for an anchor. The Space property determines whether to include spaces in the text when searching for an anchor. The Regular expression property allows to enter the regular expression text used during text comparison when searching for an anchor. The Fuzzy property determines whether to use fuzzy logic when comparing texts during anchor search. Anchors can be located on different document rotations, so it makes sense to go through all the rotation tabs (0, 90, 180, 270).

After the pattern initial recognition, it is needed to define anchor blocks (using the Anchor property) and enter the values in the properties that are necessary for searching for anchors in documents that will be recognized by this pattern. After defining anchors, you need to create text groups,to do this, click on an empty string in the groups' panel and enter the new group name. Text blocks are included in the group only if they are completely located in the search coordinate area. Each group has the following properties:

* Name
* Rotation
* Coordinates
* Anchor - \*

The Name property is mnemonic and is used when working with documents from the Recognize form element. The Rotate property determines the document's which rotations to search for this group on(0, 90, 180, 270). The coordinates' property determines which the document area to search for this group (% relative to the document size). The Anchor properties determine which anchors to use when searching for a given group. There are four such anchors in total: left, right, lower and upper, and each has the following properties:

* Name
* Upper
* Left
* Lower
* Right

The Name property defines the anchor name used in this search. The Upper, Left, Lower, Right properties define the search area beginning and end offsets relative to the anchor (determined in% relative to the anchor block size).

If you use coordinates, it is important to remember that the processed documents frames and sizes must be identical to the reference and cut off parts, or additional blank areas in the scanned image are unacceptable. It is also important to remember that OCR technology only works with good quality and high-resolution documents. The studio comes with several recognition patterns. These patterns are not final and require customization for your scan formats.

To test the pattern, you can click either the Test pattern button or the Test image button. After testing, the screen will display the image processing results by the pattern.

**Screenshot**

Testing a pattern differs from testing an image in that in a pattern case, the image attached to the pattern is tested, and in an image case, it will be necessary to select a file for testing**.**

The created pattern must be saved to disk, after which it can be used in the Recognize shape element**.**

To configure OCR, you must click the Settings button, after which, in the window that opens, you can edit the properties:

* Language (defines the document language)

![](../../.gitbook/assets/bn\_2.JPG)

The selected OCR language must be installed in the operating system (see item description  [Microsoft OCR](https://rondem.gitbook.io/primo-rpa-eng/els\_ocr/microsoft-ocr)).
