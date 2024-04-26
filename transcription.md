---
layout: page
title: Transcription Workflow
permalink: /transcription/
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

## Transcription Steps

### 1. Assure the pages are in the right order

Go through the whole document and make sure the pages are in the right order. If they are not, drag them into the correct order.

### 2. Segment the pages

- Select all images you would like to segment automatically
    - Generally this can be used for any plain text page.
    - Pages with strange formats (upside down or sideways text) will not perform well
    - If you segment too many pages at once, the process may fail
- Click the "Segment" button.
- After the popup appears telling you that the pages have been segmented, verify that the segmentation is good.
    - Correct any lines that are too small or too large.
    - Delete and extraneous lines.
    - Manually add any lines that the automatic process missed.
- Manually segment any pages that cannot be automatically segmented.

Please see the [official documentation](https://escriptorium.readthedocs.io/en/latest/segment/#text-line-segmentation) to learn how the segmentation tool operates.

### 3. Assign regions

#### For correspondence
{: .no_toc }

- Add the regions you need for this document under "Region types" on the "Ontology" tab. Make sure you click "Update" at the bottom of the page to save your changes. For correspondence, we use the following regions:
    - Salutation
    - Date and Address (use this even if there is only a date and no location)
    - Signature (includes the closing of the letter)
    - Addressee (use for the recipient’s name at the bottom of the page of the main text)
    - Address (use for the recipient’s information on the outside/back of the letter)
    - Return Address (information about the sender on the outside/back of the letter)
    - Postscript
    - Marginalia
- For each image, enter region mode by selecting the button with four squares  
![eScriptorium image toolbar]({{ site.baseurl }}/assets/image-toolbar.png)
- Draw the regions for each section. Each region should be large enough to encompass all of the lines it covers. Note that if you automatically segmented the page, the model will have guessed region areas (but not types). These will likely need to be deleted and redrawn.
- Assign region types. For the body of the letter, use the default region "Main."

#### For journals
{: .no_toc }

- Make sure that each page has its own region.
- Assign each region the type "Main."

Please consult the [official documentation](https://escriptorium.readthedocs.io/en/latest/segment/#region-segmentation) for more information on regions.

### 4. Transcribing the document

#### If using machine-assisted transcription
{: .no_toc }

- Confirm with your manager that you are approved for using machine assisted transcription.
- Select all images you would like to automatically transcribe.
- Click on the "Transcribe" button.
- You will be prompted to select a model from the dropdown list. Choose an appropriate model. Consult with your manager about which model to use.
- After the transcription is completed, go through the document line by line and correct any errors.
- In the project log, notate that the document was automatically transcribed and list which model you used.

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

- Record the document in the Project Log.
- Notate any difficulties you had in transcribing the page.
