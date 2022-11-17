# RichTextEditor

A TinyMCE like in-field-editor written in LiveCode as a group object
The goal of this stack was to provide an in-field text formatting capability much like TinyMCE does for Javascript. You can format a character or group of characters or anything selected in the text field and change the way it is formatted. Features include Bold, Italic, Underline, Strikeout, Hyper(URL)Link,List, change Font, change Font size, change Font Color and insert an image as a character image source to display an image in the field.

The default card in this stack file has a group (grpRichEditor) that contains a text field, edit button, a group of text fromating buttons, a group containing the button icons, a grpPopup that allows input to create URL links, and grpPicFile that stores any images that were inserted into the text as character imagesources.

Everything is contained in the group (grpRichEditor).

The Edit Text button unlocks the text field so the text can be edited which also unhides the group of formatting buttons. Once the editing and formatting is completed, the Stop Editing button hides the the group of formatting buttons and locks the field so URL hyperlinks will launch in a browser window.

Selecting any group of text (selectedChunk of fld "fldEditor" into tChunk) will allow the different formatting buttons to operate. They will be hilited if their property has been applied to the selection. Clicking on the hilited button again removes the formatting on the selection. Font, Font Size, and Font Color require you to select a new value for any change. You can apply multiple button formats on the same selected text at the same time.

The Image button opens a pick file dialog for selecting an image. Canceling the Dialog box removes the image currently applied to the selected text as an imagesource and deletes it from the hidden group grpPicFile. When you select a new image from the dialog box, the image is created in the hidden group grpPicFile so it can be referenced as an image source to insert the image into the text field on the selected character. Be careful selecting multiple characters will insert multiple copies of the same image, once for each selected character.

Maybe LiveCode could convert this to a script widget!
