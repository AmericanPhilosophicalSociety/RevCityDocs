---
layout: page
title: Metadata Guidelines
permalink: /metadata/
last_modified_date: May 16 2024
---

# {{ page.title }}

This document is intended as a guide to data entry and descriptive cataloging for _The Revolutionary City: A Portal to the Nation’s Founding_, a collaborative digital project using Islandora and Drupal software. It is designed to help the creator of the record metadata decide what information is required, which field is the best choice for the information, and the format in which the information should be entered.  It will be updated as modifications in the software and/or metadata schema necessitate.

## **Table of Contents**


## **Quick Links**
The Revolutionary City Workbench spreadsheet  
The Revolutionary City authority values  
The Revolutionary City Digitization Workflow Guide  


## **Each field includes the following information**
**Field name:** Display label for the name of the field in Islandora.  
**Definition:** A combination of MODS definitions, Islandora Workbench definitions, and APS modifications as appropriate.  
**Obligation:** A statement about whether the field is required, required if applicable, recommended, or optional; and information about whether or not you can have more than one value in the field (i.e. repeatable or not repeatable).  
**Enter Data in Spreadsheet Column:** The corresponding column heading in the Workbench spreadsheet to enter the data. The column name indicates to Workbench which field to add value and must be exactly as the drupal machine name is spelled/formatted.  
**Type of field:** The type of data that can be entered into a particular field.  
**Application:** Specification on formatting and tips for entering data into a particular field.  
**Example(s):** Sample data that would be acceptable in this field.  

## **General Information and Guidelines**
* The terms “item,” “resource,” and “object” have been used interchangeably throughout these guidelines. An “item,” “resource,” or “object” can be a number of different things including a an individual document, a folder of documents, a photograph, a photo album (filled with many photographs), a journal, a diary, an account book, a published book, a recorded oral history, a scrapbook, a map, an atlas, a postcard, a video or audio recording etc.
* Be consistent in your use of the metadata fields.
* One row in the Workbench spreadsheet equates to one Drupal node. A node is created to hold descriptive metadata about content in the repository.
* If you have no data for a metadata field, **leave it blank**; do not enter “N/A” or “None” or question mark.
* Ending punctuation is not required for field content and is only recommended in fields where complete sentences are used (e.g. abstract, notes).
* Do not use ampersands (“&”) to connect sentence elements. An ampersand should only be used when it is part of an official corporate name or logo.
* Where multiple values are appropriate in a repeatable field (names, subjects, languages, etc.), you **must** separate them with a pipe "\|" and no spaces in between values when entering into the workbench spreadsheet.
* Avoid the use of abbreviations. Writing words out enables users to find items consistently and also helps to avoid confusion (such as abbreviating both County and Company to “Co.”). An exception to this rule is the use of “St.” in a city or place name (e.g. St. Peter, St. Paul or St. Benedict).
* **Spell-check your metadata.** After entering your information into the MIK spreadsheet, run the spell check to catch any misspelled words. Also, verify the spelling of local place names and individual’s names that may not be caught during the spell-check process.

**For contributors:**
* Review the list of metadata fields prior to beginning data entry for your collections. You should look for fields that are designated as “Required.” Required fields must contain a value (if one is known). Contributing organizations must complete all required fields.

## **Required Metadata**

### **File**
**Definition:** The location of files that are used to create Drupal Media.  
**Obligation:** Required; not repeatable  
**Enter Data in Spreadsheet Column:** file  
**Type of field:** Text  
**Application:**  
* If you are uploading multiple **Book objects** (objects with multiple pages), the file column should be formatted:
  *  Enter the folder name that contains the media
  *  The folder name must be the same root as the file name
  
      Folder name = Mss_Coll_190  (this is entered in the _file_ field only)
      Filenames within folder = Mss_Coll_190-001.tif, Mss_Coll_190-002.tif, etc.

* If you are uploading multiple **Single Graphics, Audio, or Video objects**, the file column should be formatted:
  *  Enter the appropriate **directory path** and individual filename with file extension.

For file names in general:
* Only use alphanumeric characters without diacritics, and underscores and hyphens, i.e. [a-z] [A-Z] [0-9] [_] [-]
* Periods should only be used for the file extension.
* File names generally follow this pattern:

Prefix (root) | Separator | Number | Period | Extension 
--- | --- | --- | --- | --- |
Mss_Ms_Coll_190 | - | 001 | . | tif 

  *  The **prefix** identifies the file as part of a collection, and should contain the collection call number, item identifier, or any other useful information. It should not be long, and is not intended to include all necessary metadata. It cannot contain hyphens, but can contain underscores.
  *  The **separator** (a hyphen) separates the prefix from the file number.
  *  The **number** is used to distinguish sequential files, e.g. pages in a folder or book, or photographs in an album. It should be padded to at least three digits, resulting in e.g. [001, 002,..., 099, 100] instead of [1, 2,..., 99, 100], which may alphabetize differently on different systems.
  *  The **period** separates the main file name from the extension, and should only be used once.
  *  The **extension** identifies the type of file, and is typically added automatically.

The Bulk Rename Utility application can be used to apply bulk changes to both folder and file names. 

**Examples:**
* Book object:
  *  Mss_B_F_327_001
  *  Coll_190_001
  *  Am_23
* Other content types (Graphic, Audio, Video):
  *  /mnt/ingest/data/Mss_497_3_Am4-001.mp4
  *  /mnt/ingest/data/Mss_B_P31_F8_62_5.tif
  *  /mnt/ingest/data/audio9177.wav


### **Total Scans**
**Definition:**  
**Obligation:** _Required for Book objects only!_; not repeatable  
**Enter Data in Spreadsheet Column:** total_scans  
**Type of field:** Integer  
**Application:**  


### **Resource Type**
**Definition:** A broad term that specifies the characteristics or general physical aspect of the content of the resource.   
**Obligation:** Required; not repeatable  
**Enter Data in Spreadsheet Column:** field_resource_type  
**Type of field:** Entity reference  
**Application:**  
* Enter the term from the controlled list below that best characterizes or describes the item. Only one value may be assigned.
* The first letter of the term must be capitalized.
