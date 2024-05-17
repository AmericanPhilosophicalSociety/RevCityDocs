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

Term name | External link  
--- | --- 
Collection | http://purl.org/dc/dcmitype/Collection 
Data Set | http://purl.org/dc/dcmitype/Dataset 
Image | http://purl.org/dc/dcmitype/Image 
Interactive Resource | http://purl.org/dc/dcmitype/InteractiveResource 
Moving Image | http://purl.org/dc/dcmitype/MovingImage 
Physical Object | http://purl.org/dc/dcmitype/PhysicalObject 
Service | http://purl.org/dc/dcmitype/Service 
Software | http://purl.org/dc/dcmitype/Software 
Sound | http://purl.org/dc/dcmitype/Sound 
Still Image | http://purl.org/dc/dcmitype/StillImage 
Text | http://purl.org/dc/dcmitype/Text 

Note: The Born-Digital Islandora 2.0 theme requires specific combinations of Resource Type and Model terms in order for compound objects, collections, and paged objects to display correctly. Please refer to Appendix B: Born-Digital Islandora 2.0 Theme Object View Configurations.

**Example:**   
Object Type | Resource Type term | Islandora Model term  
--- | --- | --- 
Collection | Collection | Collection 
Audio | Sound | Audio 
Basic Image (jpeg) | Still Image | Image 
Book (parent of pages) | Still Image | Image 
Large Image (tiff) | Still Image | Image 
Page | Text | Page 
PDF | [any] | Digital Document 
Video | Moving Image | Video 


### **Model**
**Definition:** Type of content being represented by a node (e.g. an image, a video, a collection of other items, etc...)  
**Obligation:** Required; not repeatable  
**Enter Data in Spreadsheet Column:** field_model  
**Type of field:** Entity reference  
**Application:**  
* Enter the term from the controlled list below that best characterizes or describes the item. Only one value may be assigned.
* The first letter of the term must be capitalized.

Term Name | External URI  
--- | --- 
Audio | http://purl.org/coar/resource_type/c_18cc 
Binary | http://purl.org/coar/resource_type/c_1843 
Collection | http://purl.org/dc/dcmitype/Collection#Model 
Compound Object | http://vocab.getty.edu/aat/300242735 
Digital Document | https://schema.org/DigitalDocument 
Image | http://purl.org/coar/resource_type/c_c513 
Newspaper | https://schema.org/Newspaper 
Page | http://id.loc.gov/ontologies/bibframe/part 
Paged Content | https://schema.org/Book 
Publication Issue | https://schema.org/PublicationIssue 
Video | http://purl.org/coar/resource_type/c_12ce 

Note: The Born-Digital Islandora 2.0 theme requires specific combinations of Resource Type and Model terms in order for compound objects, collections, and paged objects to display correctly. Please refer to Appendix B: Born-Digital Islandora 2.0 Theme Object View Configurations.

Object Type | Resource Type term | Islandora Model term  
--- | --- | --- 
Collection | Collection | Collection 
Audio | Sound | Audio 
Basic Image (jpeg) | Still Image | Image 
Book (parent of pages) | Still Image | Image 
Large Image (tiff) | Still Image | Image 
Page | Text | Page 
PDF | [any] | Digital Document 
Video | Moving Image | Video 

### **Member of**  
**Definition:** Determines the parent of the object. It is used to identify the collection to which an object belongs, or the parent/container object if the object is a page or compound object.  
**Obligation:** Required (if adding to a pre-existing collection); not repeatable  
**Enter Data in Spreadsheet Column:** field_member_of  
**Type of field:** node reference  
**Application:**  
* For the purposes of Workbench, the Member Of column is used if you have a pre-existing collection in Drupal into which you want to ingest an object. In this case, you will enter the collection’s node ID in the Member Of column in the object row that belongs to the collection.
* If you are adding a new collection to Drupal, you will leave this column blank. However you will not delete the column when ready for ingest.

### **Title**  
**Definition:** A word, phrase, character, or group of characters, normally appearing in a resource, that names it or the work contained in it.  
**Obligation:** Required; not repeatable (Exactly one main title is required; for additional titles, use Alternative Title or Subtitle fields)  
**Enter Data in Spreadsheet Column:** title AND field_metadata_title  
**Type of field:** Text  
**Application:**  
* _title_ column must be contain a value for Islandora Workbench purposes. This will be the header on the object page, and will display as the object title on collection and search results pages.
* _field_metadata_title_ column must contain the same value as above in _title_ field. This will display as the object title in the metadata portion of the object page.
* For correspondence and like materials: its title should be entered as “Last Name, First Name to First Name Last Name”

   Montgomery, Dorcas Armitage to Sarah Franklin Bache, 1783 July 26
  
* If the date is part of an item’s title, generally the case with items of correspondence or several documents with the same name (like ‘Lecture Notes,’ etc.), the date will appear in the title following the title text and a comma. It should follow the format of ‘YYYY Month (spelled out) DD - Month (spelled out) DD’.

  Lecture Notes, 1802 January 31 - February 2

* If an item spans multiple years, it should follow the format of ‘YYYY-YYYY’.

  Lecture Notes, 1802-1805

**Additional information regarding titles:**
* An item should have a brief, descriptive, and unique title. The title should describe the item in basic terms, but should not attempt to supply an exhaustive description.
* If there are multiple items with the same title, additional information is needed to make each title unique. This could be a date, a location, or a number.
* The title may be transcribed from the item itself (book title, photograph caption, artist's title, item name, etc.). 
  *  Write out the title the way it appears.
  *  If the material has been published, format title following sentence structure (first word and proper nouns capitalized)
  *  Keep other capitalization the same as it is found on the item.
* If no title exists: 
  *  Construct one using accepted standards (DACS 2.3).
  *  Compose a title for the item similar to one found in a digital library or similar resource (including OCLC Worldcat)
  *  Do not put the call number, file name, or other identification numbers in the title
  *  Use the same capitalization for all titles in a record unless there is a reason not to do so (e.g., authorized series titles)
  *  Write out abbreviations or acronyms
* Separate titles and subtitles with a colon
* When a name is unknown/guessed:
  *  Use “Unknown recipient” or “Unknown author” - for unknown name
  *  Use brackets for guessed name (e.g. [Sabrina] Bocanegra) in the description field
 
**Examples:**  

Type of Object | Title  
--- | --- 
Correspondence | Adams, Samuel to Sally Preston Adams, 1778 July 20 
Diary/Journal | Elizabeth Farmer letter book, 1774-1789 
Broadside | In committee, December 14, 1774. Resolved, that the proceedings of this committee on November 30th, concerning the killing of sheep be republished in the English and German newspapers, and also in hand bills, to be dispersed through the markets of this city, viz. ... 
Minutes | Society of Friends minutes 

### **Id**  
**Definition:** A unique identifier specifically used for Islandora Workbench as a reference to match objects with its parent collections.
**Obligation:** Required; not repeatable  
**Enter Data in Spreadsheet Column:** id  
**Type of field:** Number (integer)  
**Application:**  
* Each row in the spreadsheet should have a value in this field. 
* No row should have the same id.
* Numbers should start sequentially from 1.
* Note: This field  is only used by Workbench and is not migrated into the Repository Item node.

Example:
 [screenshot of Rev City workbench sheet]

### **Parent**  
**Definition:** Defines the relationship between parent and child objects or nodes.  
**Obligation:** Required, not repeatable  
**Enter Data in Spreadsheet Column:** parent_id  
**Type of field:** Number (integer)
**Application:**
* For new collections, you must enter the proper number from the _id_ field into the _parent_id_ column. 
* If the collection into which you are ingesting the object already exists in the Portal, you can use field_member_of to identify the parent using its node ID. 
  *  In that case, the Book Parent would not have anything in the _parent_id_ column, but would include the collection node ID in the _field_member_of_ column.
* Note: This is only used by Workbench and is not migrated into the Repository Item node.

Example:
 [screenshot of Rev City workbench sheet]

### **Weight**  
**Definition:** Indicates the order of a resource in a collection of resources (used for compound objects and paged content).  
**Obligation:** _Required for Book Objects only!_; not repeatable  
**Enter Data in Spreadsheet Column:** field_weight  
**Type of field:** Number (integer)  
**Application:**  
* This value will be added by **Administrator** through a python script; leave blank and do not delete the column
* This is only used by Workbench and is not migrated into the Repository Item node.

Example:
 [screenshot of Rev City workbench sheet]

### **Digital Origin**
**Definition:** The method by which a resource achieved digital form.  
**Obligation:** Required; not repeatable  
**Enter Data in Spreadsheet Column:** field_digital_origin  
**Type of field:** Entity reference  
**Application:**   
* Enter the term from the controlled list below that best characterizes or describes the item.
* Most content will be "Reformatted digital" indicating that it is a digital facsimile of an original physical object.
* Use "digitized other analog" only when the digital resource was created by digitizing an intermediate form other than microform, such as a photocopy, of the original.
* The first letter of the term must be capitalized.

Digital Origin Term | Definition 
--- | ---
Reformatted digital | A resource was created by digitization of the original which was in a non-digital form (except original microforms). This value will be used most commonly.
Born digital | A resource was created in and is intended to remain in digital form.
Digitized microfilm | A resource was created by digitizing a microform [microfilm/microfiche].
Digitized other analog | A resource was created by digitizing an intermediate form of the original resource (but not microform) such as photocopy, transparency, slide, 2nd generation analog tapes, etc. [might include carbon copies]


### **Parent Collection Call Number**
**Definition:** Local call number or accession number for the original source object.  
**Obligation:** Required if applicable; not repeatable  
**Enter Data in Spreadsheet Column:** field_parent_collection_call_num  
**Type of field:** Text (plain)  
**Application:**  
* Enter the item’s specific/named collection number identifier located within the contributing organization’s larger collection.
* Do not leave spaces between periods.

**Examples:**
* Mss.B.F327
* Mss.Ms.Coll.73
* Mss.497.3.Sp5
* Amb.1752
* Coll740

### **Parent Collection Title**
**Definition:** The name of a collection of which the item being described is a part.  
**Obligation:** Required; not repeatable  
**Enter Data in Spreadsheet Column:** field_collection2  
**Type of field:**  Entity reference  
**Application:**  
* Enter the item’s specific/named collection located within the contributing organization’s larger collection.
* Enter the title exactly as it appears in the accession record or finding aid

**Examples:**
* The Sol Feinstone collection of the American Revolution, ca. 1760s-1850s
* Julia Rush letters, 1776-1809
* Spokane primer, 1976

### **Parents Finding Aid URL**
**Definition:** Internet address of the finding aid, collection description, or other guide for understanding and accessing the repository collection to which the resource belongs.  
**Obligation:** Required if applicable; not repeatable  
**Enter Data in Spreadsheet Column:** field_collection_url  
**Type of field:** Link  
**Application:**  
* Enter the URL of the finding aid or other collection guide. **Enter the URL only.**
* Do not include entire URL when pulling from a search 

  Correct: https://search.amphilsoc.org/collections/view?docId=ead/Mss.DLAR.Film.706-ead.xml
  Incorrect: https://search.amphilsoc.org/collections/view?docId=ead/Mss.DLAR.Film.706-ead.xml;query=Jasper%20Yeates%20papers;brand=default

  



