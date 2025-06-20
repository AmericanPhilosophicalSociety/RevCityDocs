---
layout: page
title: Transcription Workflow
permalink: /transcription/
last_modified_date: 2025-06-12
---

# {{ page.title }}
{: .no_toc }

<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
- TOC
{:toc}
</details>

Note: This documentation is meant to supplement, not replace, the complete [eScriptorium documentation](https://escriptorium.readthedocs.io/en/latest/). Please consult the official documentation to learn about using the tool.

## Uploading Documents

### Upload a whole collection

#### For RevCity admins:
{: .no_toc }

Find the Drupal NID for the collection you would like to import and send it to the project managers. They will run a script to upload the documents.

#### For all others:
{: .no_toc }

Send a link to the collection you would like to import to the project managers.

### Upload individual documents

Prepare a CSV following [this template](https://github.com/AmericanPhilosophicalSociety/RevCityDocs/blob/main/templates/transcription-upload-template.csv). Your CSV should include the following:

- the Drupal NID for the document
- the title of the document as you would like it to appear in eScriptorium (should match Drupal)
- the project name you would like to have in eScriptorium
- the machine-readable name for the folder the documents will be stored in

Send your CSV to a project manager who can run the script for upload.

## Transcription Steps

### 1. Assure the pages are in the right order and delete blank pages.

Go through the whole document and make sure the pages are in the right order. If they are not, drag them into the correct order.

Next, delete any pages that do not contain text. If you are unsure whether a page has text, please ask your manager.

### Handling upside down or sideways pages

You can use the Source Image panel to rotate the image to the correct orientation. Note, however, that you must to rotate the image back to its original orientation once segmentation and/or transcription is complete; otherwise, it cannot be used for training.

### 2. Segment the pages

- Select all images you would like to segment automatically
    - Generally this can be used for any plain text page.
    - Pages with strange formats (upside down or sideways text) will not perform well
    - **Warning**: Only segment 2-3 pages at a time. If you select too many, the process may fail and put undue stress on the system.
- Click the "Segment" button.
- After the popup appears telling you that the pages have been segmented, verify that the segmentation is good.
    - Correct any lines that are too small or too large.
    - Delete and extraneous lines.
    - Manually add any lines that the automatic process missed.
    - Verify line masks: does a line mask exist? Does it reasonably cover the text?
      - Note: do **NOT** try to manually adjust masks. Instead, fiddle with the baseline until the mask reasonably encompasses the text. If the mask is truly egregious, ask a project manager for assistance. 
- Manually segment any pages that cannot be automatically segmented.

Please see the [official documentation](https://escriptorium.readthedocs.io/en/latest/segment/#text-line-segmentation) to learn how the segmentation tool operates.

### 3. Assign regions

#### For correspondence
{: .no_toc }

- Add the regions you need for this document under "Region types" on the "Ontology" tab. Make sure you click "Update" at the bottom of the page to save your changes. For correspondence, we use the following regions:
    - Salutation
    - Date and Address (use this even if there is only a date and no location)
    - Closing (includes the closing of the letter)
    - Addressee (use for the recipient’s name at the bottom of the page of the main text)
    - Address (use for the recipient’s information on the outside/back of the letter)
    - Postscript
    - Marginalia (use this for all other text regions, including anything besides the address on the outside/back of the letter)
- For each image, enter region mode by selecting the button with four squares  
![eScriptorium image toolbar]({{ site.baseurl }}/assets/image-toolbar.png)
- Draw the regions for each section. Each region should be large enough to encompass all of the lines it covers. Note that if you automatically segmented the page, the model will have guessed region areas (but not types). These will likely need to be deleted and redrawn.
- Assign region types. For the body of the letter, use the default region "Main." If a letter has two pages on one scan, use the regions "Main A" and "Main B" as you would for journals.

#### For journals
{: .no_toc }

- Use a model finetuned for journals. These will usually have "journal" or "two_page" in their names.
- When checking the work, assign the left side of the page the region "Main A" and the right side of the page the region "Main B."

**Note**: Once you are pleased with the segmentation, you must associate the lines and the regions. To do this, press ```Ctrl + A``` to select all lines, then ```Y``` to associate lines and their regions. Lines can only be associated with one region and will be grouped with the region closest to their centroid.

Please consult the [official documentation](https://escriptorium.readthedocs.io/en/latest/segment/#region-segmentation) for more information on regions.


### 4. Transcribing the document

#### If using machine-assisted transcription
{: .no_toc }

- Confirm with your manager that you are approved for using machine assisted transcription.
- Select all images you would like to automatically transcribe.
- Click on the "Transcribe" button.
  - You will be prompted to select a model from the dropdown list. Choose an appropriate model. Consult with your manager about which model to use.
  - You will be prompted to select a transcription. This is the destination layer for your transcription. You may leave it blank to create a new layer, but it is recommended to use "manual". The transcription you would like to be used on the portal should **always** end up on the "manual" layer.
- After the transcription is completed, go through the document line by line and correct any errors.
- In the project log, notate that the document was automatically transcribed and list which model you used.

**Note**: For long documents, greatest accuracy can be achieved through a mixed method: transcribe a representative sample of the document, then fine-tune the generalized model on that sample. Please ask your manager if you would like to experiment with this.

#### If transcribing manually
{: .no_toc }

- Open the "Transcription" panel.
- Click on the first line.
- Transcribe each line, writing exactly what you see.

Please follow our [transcription conventions and guidelines]({{ site.baseurl }}/transcription-guidelines).

Consult the [official documentation](https://escriptorium.readthedocs.io/en/latest/transcribe/#editing-with-the-transcription-panel) if your question is not answered here.

### 5. Reorder the lines

- Open the "Text" panel.
- On the image panel, click the button with a downward arrow and two numbers to see the line order.
![image toolbar with the reorder button highlighted]({{ site.baseurl }}/assets/reorder-toolbar.png)
- On the text panel, drag the lines into their correct order to match the natural reading order of the page.

See the [official documentation](https://escriptorium.readthedocs.io/en/latest/transcribe/#sorting-lines).

### 6. Document what you did

- Record the document in the Project Log or for volunteers using the [Google form](https://docs.google.com/forms/d/e/1FAIpQLSf1JwO4Lzb5cQs9JSpxyF1wHMqWJ3su4BKL1gCVafcLhtvrIw/viewform?usp=dialog).
- Notate any difficulties you had in transcribing the page.
