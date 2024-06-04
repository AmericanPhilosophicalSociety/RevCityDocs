---
layout: page
title: Metadata Guidelines
permalink: /metadata/
last_modified_date: May 16 2024
---

# {{ page.title }}

This document is intended as a guide to data entry and descriptive cataloging for _The Revolutionary City: A Portal to the Nation’s Founding_, a collaborative digital project using Islandora and Drupal software. It is designed to help the creator of the record metadata decide what information is required, which field is the best choice for the information, and the format in which the information should be entered.  It will be updated as modifications in the software and/or metadata schema necessitate.

<details open markdown="block">
  <summary>
 **Table of Contents**
    </summary>
- TOC
{:toc}
</details>


## **Quick Links**
[_The Revolutionary City_ Workbench spreadsheet](https://docs.google.com/spreadsheets/d/1WacRNrChpRkMAK4PefgRHpRiS3kGFy1qNC4e6gk3-jM/edit#gid=1002365943)  
[_The Revolutionary City_ authority values](https://docs.google.com/spreadsheets/d/1LXrGtfqEMJIF2YMybozO_QUC-3WEP3GQ5GpxhRgTJO0/edit#gid=1692189288)  
[_The Revolutionary City_ Digitization Workflows Guide](https://docs.google.com/presentation/d/1STI-qUVlGjjtBmtEin_qq4iXElq_usPd1lTL0Dxvy1w/edit#slide=id.g583e451791_0_92)  


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

***

### **Total Scans**
**Definition:** Number of digital files for a given object or resource.  
**Obligation:** _Required for Book objects only!_; not repeatable  
**Enter Data in Spreadsheet Column:** total_scans  
**Type of field:** Integer  
**Application:**  
* Enter the number of digital files in a folder for each book object to be ingested.
* This number must match the amount of files in your object’s folder in order for workbench to run the ingest and upload the files.

**Example:**

Object folder | total_scans field
--- | ---
7 tif files | 7
158 tif files | 158
40 jpg files | 40

***

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

***

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

***

### **Member of**  
**Definition:** Determines the parent of the object. It is used to identify the collection to which an object belongs, or the parent/container object if the object is a page or compound object.  
**Obligation:** Required (if adding to a pre-existing collection); not repeatable  
**Enter Data in Spreadsheet Column:** field_member_of  
**Type of field:** node reference  
**Application:**  
* For the purposes of Workbench, the Member Of column is used if you have a pre-existing collection in Drupal into which you want to ingest an object. In this case, you will enter the collection’s node ID in the Member Of column in the object row that belongs to the collection.
* If you are adding a new collection to Drupal, you will leave this column blank. However you will not delete the column when ready for ingest.

***

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

***

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

***

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

***

### **Weight**  
**Definition:** Indicates the order of a resource in a collection of resources (used for compound objects and paged content).  
**Obligation:** _Required for Book Objects only!_; not repeatable  
**Enter Data in Spreadsheet Column:** field_weight  
**Type of field:** Integer (number)  
**Application:**  
* This value will be added by **Administrator** through a python script; leave blank and do not delete the column.
* This is only used by Workbench and is not migrated into the Repository Item node.

Example:
 [screenshot of Rev City workbench sheet]

***

### **Display Hints**  
**Definition:** A term to define which viewer is used on an object page.  
**Obligation:** Required for Workbench; not repeatable  
**Enter Data in Spreadsheet Column:** field_display_hints  
**Type of field:** Entity reference  
**Application:**  
* This value will be added by **Administrator** through a python script; leave blank and do not delete the column
* This is only used by Workbench and is not migrated into the Repository Item node.

Term name | Used for
--- | ---
Open Seadragon | Large Image, Page
PDFjs | PDF
Remote Media | Video or audio files stored externally

***

### **Holding Institution**  
**Definition:** Name of the organization contributing the digital item to Portal.  
**Obligation:** Required; not repeatable  
**Enter Data into Spreadsheet Column:** field_institution  
**Application:**  
* Enter the name of the project member institution contributing the digital resource, selecting from the locally-controlled Rev City Member Authorities Table: [Here.]  
* Institution names should be entered the exact same way in every record.
* Write out abbreviations or acronyms.
* ONLY enter the name of the contributing organization. DO NOT use this field to enter donor information or provenance information from your organization. This information can be included in the Note field if necessary. Other information such as mailing address, email address, phone number, and URL to organization's website will be included on the project partners page.

**Examples:**
* American Philosophical Society  
* Library Company of Philadelphia  
* Historical Society of Pennsylvania  

***

### **Theme**  
**Definition:** A Rev City locally controlled topical term/phrase that best characterizes or describes the general subject or topic of the item.  
**Obligation:** Required; repeatable (max of 2 terms)  
**Enter Data into Spreadsheet Column:** field_theme  
**Application:**  
* There is a subjective element to assigning the topic values. Sometimes an item can span more than one of these topical terms. Think about how users will look for and find this item; select the term that you think BEST describes the item.
* The first letter of each word in the term (except articles) must be capitalized.
* Separate 2 terms by a pipe “\|” with no spaces between terms in the workbench spreadsheet, i.e. Lived Experience\|Economy

Theme term | Description
--- | --- 
Declaring Independence | To declare independence took more than shouting about freedom, it meant having the networks, correspondence, and political, federal, and governmental infrastructure to see it through. Learn more about the broad range of documents — the official texts, treaties, proclamations, and announcements — that allowed the colonies to become states. 
Economy | The fervent cry for “no taxation without representation” confirms the way in which economic concerns were tied up with desires for independence. Waging a war required a complex structure to support it — securing goods, paying soldiers, and even administering taxes. 
Lived Experience | Philadelphians had a wide variety of lived experiences during the Revolution depending on their gender, race, age, class, religion, and political affiliation. Learn more about life in the city as the war unfolded through the eyes of its diverse inhabitants.
Media | Residents of Philadelphia lived in a complex media landscape. They learned about current events through print, manuscript, and word of mouth. Explore the diverse array of formats and learn about the pathways by which different types of information spread during wartime.
Mobilized Populace | Political movements both for and against separation from Great Britain sought to gain support through a variety of means. Learn more about the oaths, petitions, uses of extralegal force, and other methods of persuasion utilized by Patriots and Loyalists alike. 
Political Philosophy | The diverse ideological origins of the American Revolution are documented in the correspondence and diaries written by the women and men of the city and in the broadsides pasted on the walls of the city’s built environment.
Politics and Causes of Revolution | As the capital of the colony of Pennsylvania and home to the Continental Congress, Philadelphia was a center for revolutionary politics throughout the 1770s and 1780s. Read more about politics both in and out of doors through the eyes of the women and men who experienced it.
Slavery | Slavery was a central facet of life in the thriving port of Philadelphia. Learn more about the experiences of bondspeople, and those who enslaved them, during the Revolution through receipts of sale, fugitive notices, advertisements, and other primary sources.
Waging the War | The Revolutionary War was, after all, a violent confrontation. Learn more about the details of military engagements , the execution of campaigns, and the spread of news from the battlefront to those back home.

**Example:** See The Revolutionary City Portal [theme page](https://therevolutionarycity.org/taxonomy/vocab/theme_list) for examples of the types of material under each theme.



## **Recommended Metadata**

### **Abstract**
**Definition:**  A narrative, textual description summarizing the content of the item.  
**Obligation:** Highly recommended; repeatable  
**Enter Data into Spreadsheet Column:** field_description_long  
**Type of field:** Text (formatted, long)  
**Application:**  
* This field is used for a free-text account of the intellectual content of the original item. For this reason, the content in the _abstract_ field can be a little longer than in other fields. It can be taken from the original item or created.
* Captions or inscriptions that are not used in the Title field may be included in the _abstract_ field.
* The _abstract_ should be written in complete sentences and the field should read as a single block of text. The block of text should end with a period.
* Do not use abbreviations, ampersands or paragraph and line breaks. Maintain standard capitalization rules. Do not use all capital letters to set words or phrases apart or to denote importance.
* This field may include information that a user will be able to see in the item. For example, does the item contain a sketch or illustration? How about an inscription or caption?

Additional information regarding Abstract:  
* You may want to include keywords in your text that end users will likely search for that are not already included in the _title_ or _subject_ fields. Incorporating keywords can provide additional access points for searching. This element provides end users with information about the digital resource that assists them in making a judgment about its likely usefulness, and also provides context, if needed, for controlled vocabulary used in the record. For example, a photograph of trolleys would have street railroads in the subject field using the Thesaurus for Graphic Materials (TGM). The more common word, trolleys, could be included in the _abstract_.
* Be descriptive but only include detail that would be helpful to users!

**Examples:**

Type of material | Sample abstract 
--- | ---
Correspondence | Letter from S. Peters to Sally Bache discussing family matters.
Diary/Journal | Collected letters of Eliza Farmer, third wife of Dr. Richard Farmer of Kensington, Pennsylvania, primarily to her nephew, Jack Halroyd, clerk in the East India Company in London, and other recipients. The letters, written from Philadelphia, describe domestic and family life, gardening conditions and production, the impact of political events such as the embargo on tea, the non-importation act, secret session of Congress, rumors of bombardment of Boston, military preparedness, and commercial activities, and war upon the availability of food and household items such as cloth and tea. Included are inventory or transaction records and medical recipes written at a later date. Note the recipes start at the end of the book and are written upside down.
Broadside | Offering bounties to those volunteering to serve with the King George III’s troops.
Minutes | Minutes that record the disciplining of Timothy Davis, who wrote a piece on taxation [A Letter From A Friend To Some Of His Intimate Friends, On the Subject of paying Taxes (1776)], and that record the disownment of Isaac Howell of Philadelphia, who manifested "a disposition to contend for Civil Rights. . . & accepted & acted in a public Station," and the disownment of John Thompson, who sought "to lay wast[e] & establish Government by Military force & to take a Test to that end."

***

### **Alternative Title**
**Definition:** Any form of the title used as a substitute or alternative to the formal title of the resource.  
**Obligation:** Recommended as appropriate; repeatable  
**Enter Data into Spreadsheet Column:** field_alternative_title  
**Type of field:** Text (plain)  
**Application:**  
* Use for titles translated into English, titles with ampersands and numerals spelled out, etc.
* This is not intended to be a repetition of the main title.
* Ensure that the alternative title is for the object, not the title of the series or the collection, or for other related objects.
* Contact Project Supervisor if unsure whether an item requires an alternative title.

**Example:**  
The Sol Feinstone Collection on the American Revolution, ca. 1760s-1850s finding aid contains item-level cataloging. The title of each item in the finding aid contains a “No.” To avoid confusion in the digital library and conform to project standards as given in this guide - we’ve added the finding aid title as the Alternative Title and created a new title following RevCity guidelines.  

   Title = Adams, Samuel to Sally Preston Adams, 1778 June 7  
   Alternative Title = No. 27 Dr. Samuel Adams to Sally Preston Adams  

***

### **Date Created**
**Definition:** The date of creation of the original resource.  
**Obligation:** Highly recommended; repeatable  
**Enter Data into Spreadsheet Column:** field_edtf_date_created **AND/OR** field_date_created_text  
**Type of field:** EDTF and Text (plain)  
**Application:**  
* Use _field_edtf_date_created_ for: known numerical dates – 1776-07-04
  *  Must conform to Extended Date/Time Format (EDTF) standards.
  *  See [EDTF Specification](https://www.loc.gov/standards/datetime/) for more information.
  *  Use the [date validator](https://digital2.library.unt.edu/edtf/) if unsure your date value conforms to EDTF standard.
  *  If the date is unknown, leave this field blank and use the text field below.
* Use _field_date_created_text_ for: plain text dates – undated, approximately 1930s
  *  Never write the date as **n.d.** if the date is unknown, only use the term undated.
  *  If only the Day of the Week is available i.e. Wednesday morning, then add to this field.


Additional information regarding Date:  
* When the resource being described is a collection or folder of items, a date range can be used to describe the creation date range of all the resources.
* Creation date refers to the date of the exact item described in the record, even if it is a derivation.
* If the item is a reprint or revision of an original text:
  *  Use the date of the reprint/revisions
  *  Include a note about the original text and printing date
* If the item is a copy negative:
  *  Use the date that the copy negative was created
  *  The date of the original photographs may be included in a note or description
* If there is no letter or message written on postcards or greeting cards:
  *  The item is treated as a photograph or piece of artwork
  *  Use the date that the photograph was taken or the drawing was done
* If the postcard or greeting card has a letter or message written on/in it:
  *  The item is treated as a piece of correspondence
  *  Use the date that the letter was written or that the card was postmarked
 

Type of Date | Format | Example 
--- | --- | ---
Year only | YYYY | 1776
Year and Month | YYYY-MM | 1778-01
Year, Month and Day | YYYY-MM-DD | 1779-10-31
Date range | YYYY/YYYY | 1774/1783
Date range | YYYY-MM/YYYY-MM | 1775-01/1775-12
Date range | YYYY-MM-DD/YYYY-MM-DD | 1781-02-02/1783-01-31
Seasons | YYYY-21 (Spring), 22 (Summer), 23 (Autumn), or 24 (Winter) | 1778-24
Date uncertain | YYYY? | 1774?
Date approximate | YYYY-MM~ | 1776-07~
Date uncertain and approximate | YYYY-DD-MM% | 1780-06-28%
Year with unknown digit | YYXX | 17XX
Unspecified digit | YYYX-MM-DD | 178X-07-04
Year and Month uncertain | YYYY-MM~-DD | 1774-05~-20
Multiple dates | YYYY\|YYYY\|YYYY | 1771\|1775\|1779

***Please consult [EDTF Specification](https://www.loc.gov/standards/datetime/) for more information on formatting.**

***

### **Date Digitized**
**Definition:** The date on which the resource was digitized or a subsequent snapshot was taken.   
**Obligation:** Recommended; not repeatable  
**Enter Data in Spreadsheet Column:** field_date_digitized  
**Type of field:** EDTF  
**Application:**  
* Must conform to Extended Date/Time Format (EDTF) standards.
*  See [EDTF Specification](https://www.loc.gov/standards/datetime/) for more information.
*  Use the [date validator](https://digital2.library.unt.edu/edtf/) if unsure your date value conforms to EDTF standard.
* If the date is unknown, leave the field blank.

**Examples:**
* 2021
* 2021-04
* 2021-04-01

***

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

***

### **Extent**
**Definition:** A statement of the number of the units (pages), file size, or duration of the resource.  
**Obligation:** Recommended; repeatable  
**Enter Data into Spreadsheet Column:** field_extent  
**Type of field:** Text (plain)  
**Application:**  
* Add the number of pages included in the item except for blank pages.
* A page is considered a page if it contains text, sketches, or any other markings including contemporary writing by creator/recipient/collaborator or later writing by donor/archivist/cataloger
* If pages, format as follows: [Number of pages][lowercase p][period] with no spaces in between.

Type of material | Sample extent
--- | ---
Letter | 4p.
Diary | 156p.
Oral history interview | 1:04:24
Song recording | 0:03:55 

***

### **Genre**
**Definition:** A term or phrase that designate a category characterizing a particular style, form, or content, such as artistic, musical, literary composition, etc.; the type of object it is.  
**Obligation:** Recommended; repeatable  
**Enter Data into Spreadsheet Column:** field_genre  
**Type of field:** Entity reference  
**Application:**  
* Enter a term for the genre of the resource that characterizes its content. The genre field should be used to characterize the content of the resource rather than the resource itself or its physical characteristics.
* Choose applicable genre terms from the Getty Art and Architecture Thesaurus (AAT) (particularly AAT terms denoted as "genre"), or from the MARC Genre Term List (MARCGT).
  *  AAT: <http://www.getty.edu/research/tools/vocabularies/aat/>
  *  MARCGT: <https://www.loc.gov/standards/valuelist/marcgt.html> 
* Be consistent and use Plural terms with the first letter capitalized.
* Separate multiple entries with a semicolon and no spaces in between entries


Additional information regarding Genre:  
* You may also want to include a keyword or phrase in the _abstract_ or _title_ fields that gives the user additional context for the genre term, especially if there is not a term found in a controlled vocabulary/resource. For example, for Correspondence, you may use the term “letters” in the _abstract_.

**Examples:**
* Correspondence
* Letter books\|Personal Correspondence\|Recipes
* Diaries\|Bookkeeping records
* Minutes\|Excerpts

***

### **Language**
**Definition:** A designation of the language in which the content of a resource is expressed.  
**Obligation:** Recommended; repeatable  
**Enter Data into Spreadsheet Column:** field_language  
**Type of field:** Entity reference  
**Application:**  
* Format as: Language term (language abbreviation)  
* Assign a three-letter language code from ISO 639-2 that matches language term	
  *  B for bibliographic
  *  <https://www.loc.gov/standards/iso639-2/php/code_list.php>
* For Indigenous languages use: https://indigenousguide.amphilsoc.org/language_browse 
* Include all relevant languages (do not include languages that are merely referenced or only appear as single words in text of another language)
* If there is more than one language:
  *  separate by pipe with no spaces between terms
  *  Be consistent with both Language text and Language code in terms of order of terms
* If there are special circumstances or additional information about the language uses of the item, include it in the Note field

**Examples:**  
* English (eng)
* Spanish (spa)
* English (eng)\|Chontal Maya (chf)\|German (ger)

***

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

***

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

***

### **Parent Collection URL**
**Definition:** Internet address of the finding aid, collection description, or other guide for understanding and accessing the repository collection to which the resource belongs.  
**Obligation:** Required if applicable; not repeatable  
**Enter Data in Spreadsheet Column:** field_collection_url  
**Type of field:** Link  
**Application:**  
* Enter the URL of the finding aid or other collection guide. **Enter the URL only.**
* Do not include entire URL when pulling from a search 

  _Correct_: <https://search.amphilsoc.org/collections/view?docId=ead/Mss.DLAR.Film.706-ead.xml>  
  
  _Incorrect_: <https://search.amphilsoc.org/collections/view?docId=ead/Mss.DLAR.Film.706-ead.xml;query=Jasper%20Yeates%20papers;brand=default>

***

### **People**
**Definition:** The name of a linked agent (e.g. person, organization, or event) associated in some way with the resource.  
**Obligation:** Recommended; repeatable  
**Enter Data in Spreadsheet Column:** field_linked_agent  
**Type of field:** Typed Relation  
**Application:**  
* Format as: relators:[relationship type abbreviation]:[type of name]:[authorized or local name]
* A ‘Relationship Type’ must be specified. See list of Relationship Types available by default in Appendix A: Default Relationship Types.
* A 'type of name' must be specified: Either person,  corporate_body, or family must be specified
  *  If the linked agent is an individual of the human species, use person
  *  If the linked agent is an organization or group of people identified by a name and that acts, or may act, as a unit, or an institutional position held by a person, use corporate_body
  *  If the creator is two or more people related through marriage, birth, adoption, or other legal manner, or who present themselves as a family, use family
* Use authorized forms of names from LCNAF or VIAF when they exist.
  *  LC Name Authority File: <http://id.loc.gov/authorities/names.html>
  *  Virtual International Authority File: <https://viaf.org/viaf>
* Where no authorized entry exists in LCNAF or VIAF, please construct names according to the standards below:
  *  Enter personal names in inverted form: Last Name, First Name, Middle Name or initial (include birth and death dates if known). 
  *  Do not use honorifics, titles, or nicknames unless it is necessary to disambiguate (e.g., the first name of the person is unknown).
  *  Use initials if the full names are not known
  *  Use spaces between initials (e.g. Rowling, J. K.)
  *  Separate hyphenated first names with a hyphen instead of a space if only initials are known
  *  Put additional middle names after the first name
  *  Consider both parts of a hyphenated name the 'last name'
  *  Consider multiple parts (von, de la, etc.) as part of the last name
  *  Include suffixes that are a part of the name (Jr., Sr., etc.) at the end of the name after a second comma (e.g. Arthur, William A., Jr., 1834-1915)
  *  Use a question mark (?) to indicate a probable date (e.g. Dickerson, Martina, 1829?-)
  *  Use “approximately” for less certain dates (e.g. Barr, Robert, approximately 1725-1808)
  *  Alternate forms of names (such as “Buddy” Jones ; Reverend Murrell ; Dr. Reed) may be used in the Description field but not as the authoritative version.

Additional information regarding People:  
* Additional names are strongly recommended if a creator, contributor, or other named agent is known. If no names associated with the resource can be determined, leave the field blank; do not enter "Unknown" or any variant in a _person_ field. Use the Note field/column instead to denote unknown responsibility for the resource.
* If the creator and the publisher of the original item are the same, repeat the creator's name in the Publisher field.
* DO NOT use this field to enter information on who donated the original object or information regarding the item’s provenance.

Examples:  
* relators:cre:person:Hollingsworth, H. (Henry), 1737-1803
* relators:aut:person:Stockton, Annis Boudinot, 1736-1801\|relators:ill:person:Rush, Julia Stockton
* relators:rcp:person:De Grasse, Isaiah G., Reverend
* relators:pbl:corporate_body:Joshua Fisher & Sons (Philadelphia, Pa.)
* relators:sgn:corporate_body:Society of Friends
* relators:col:family:Biddle family

***

### **Place Published**
**Definition:** The name of the entity that published, printed, distributed, released, issued, or produced the resource.  
**Obligation:** Recommended if applicable; repeatable  
**Enter Data into Spreadsheet Column:** field_place_publisher  
**Type of field:** Entity reference  
**Application:**  
* If the original item was published and the publisher and/pr place is known, enter data in this field.
* If no publishing statement is present on the resource or its documentation, leave the _place published_ field blank.
* Use authorized forms of names from LCNAF (http://id.loc.gov/authorities/names.html) when they exist. 
* If there is no entry in the LCNAF, enter the publisher’s name as printed on the item:
  * Format: [Publisher location] : [Publisher name], [Date of publication]
  * Do not invert names of individuals (for self-publishing)
  *  Do not invert personal names that are parts of organizational names
  *  Use the names as they appear in the item for non-government or single-level bodies
  *  Write out names instead of using acronyms

**Examples:**  
* Philadelphia : Printed by John Dunlap, 1777
* Baltimore : Printed by Mary Katharine Goddard, 1777
* [Philadelphia] : Printed by F. Bailey, [1783]

***

### **Reformatting Quality**
**Definition:** The type of scan done on the original object, e.g. access (JPEG) or preservation (TIFF).  
**Obligation:** Required; not repeatable  
**Enter Data in Spreadsheet Column:** field_reformatting_quality  
**Type of field:** Entity reference  
**Application:**  
* Enter the term from the controlled list below that best characterizes or describes the item.
* The first letter of the term must be capitalized.
* Scanning done for _Rev City_ should always be preservation, however, there may be exceptions. Please talk to the Project Team if there are questions.
* Note: Derivatives are created upon ingest.

***

Reformatting Quality term | Definition 
--- | --- 
Access | The electronic resource is intended to support current electronic access to the original item (i.e., reference use), but is not sufficient to serve as a preservation copy.
Preservation | The electronic resource was created via reformatting to help preserve the original item. The capture and storage techniques ensure high-quality, long-term protection." This value will be used most commonly. 
Replacement | The electronic resource is of high enough quality to serve as a replacement if the original is lost, damaged, or destroyed.

***

### **Subjects**
**Definition:** A formal term or phrase representing the primary topic(s) (people, organizations, events or themes depicted or described) on which an item is focused.  
**Obligation:** Recommended; repeatable  
**Enter Data in Spreadsheet Column:**   

   Topic Subject = field_subject   
   Subjects (Name) = field_subjects_name  
   Location = field_geographic_subject  
   Temporal Subject = field_temporal_subject  

**Type of field:** Entity reference  
**Application:**  
* For all subject fields:
  *  If there is more than one term or phrase in the subject field, separate by pipe with no spaces between terms, i.e. Female friendship\|Social networks--18th century\|War and families 
* Use authorized terms from LCSH, LCNAF, or another thesaurus whenever possible.
  *  LC Subject Headings: <http://id.loc.gov/authorities/subjects.html> (Use for topical subjects)
  *  LC Name Authority File: <http://id.loc.gov/authorities/names.html> (Use for name and location subjects)
  *  LC Authorites (all): <https://authorities.loc.gov/webvoy.htm> 
  *  FAST: <https://fast.oclc.org/searchfast/>
  *  Homosaurus: <https://homosaurus.org/>  
  *  CNAIR controlled vocabulary : <https://indigenousguide.amphilsoc.org/culture_browse/all>
* For Locations:  
  *  Return and Send addresses (mostly cities) should be added to the _field_geographic_subject_. Locations where people are writing from and sending to are important metadata.
* For Name subjects:
  *  Enter any names associated with the resource’s content.
  *  This is distinct from names associated with the creation of the resource; Use when names are described or referenced in the item.
  *  If a person has an alternate name or alias, include their real name under Name subject and aliases as keywords in the Abstract field.
* For hierarchical subjects (mostly topical subjects):
  *  Use 2 hyphens with no spaces on either side between subdivisions for full LCSH (e.g. Indians of North America--Northwest, Pacific--Structures)
  
Specific formatting:  

Drupal term | Format | Example 
--- | --- | ---
field_subject | Only the LCSH authorized term or other controlled vocabulary term is necessary | Marriage\|Quakers
field_subject_name | Must include the type of name (person:, corporate_body:, or family:) | person:Faro,Jarvis\|corporate_body:Society of Friends\|family:Sellers family 
field_geographic_subject | Only the LCNAF authorized term or locally created term is necessary | Philadelphia (Pa.)\|Schuylkill River (Pa.)\|Passy (Haute-Savoie, France)


Additional information regarding Subjects:  
* Information in the subject fields should describe what the content is ‘about’
  *  Subjects/keywords answer questions like: who, what, where, and when
* If there is a term/keyword not found in a controlled vocabulary/resource that will aid users in finding the item, you may include it in the _abstract_ or _title_ field.
* There is a subjective element to assigning the topical subjects. Think about how users will look for and find this item; select the term that you think BEST describes the item.
* Choose as many terms as necessary to capture subject content:
  *  1-2 subjects are recommended, but number varies depending on content.
  *  Avoid terms too general to describe a particular item.
  *  Only include geographic subjects when the particular place is important to the subject content.
* It is not necessary to repeat terms from controlled vocabularies as keywords


 

## **Other Metadata**

### **Administrative Notes**
**Definition:** Administrative textual information relating to a resource.  
**Obligation:** Optional; not repeatable  
**Enter Data into Spreadsheet Column:** field_administrative_notes  
**Type of field:** Text (plain, long)  
**Application:**   
* You may enter notes from the finding aid or guide, digitization notes (i.e. scanning related comments), or other notes not necessary for public knowledge.
* Internal use only; does not appear in Public User Interface

**Examples:**
* Digitized by: Bocanegra, Sabrina
* Digitized by: American Philosophical Society
* Not only copy, see #93 in collection
* Has restrictions, see ASpace record

***

### **Date Modified**  
**Definition:** The date in which a resource is modified or changed.  
**Obligation:** Optional; not repeatable  
**Enter Data into Spreadsheet Column:** field_date_modified  
**Type of field:** EDTF  
**Application:**  
* Enter the date in EDTF format in which the object was modified.

**Examples:** See Date Created for information on formatting.

***

### **Note**
**Definition:** General textual information relating to a resource.  
**Obligation:** Optional; repeatable  
**Enter Data into Spreadsheet Column:** field_note  
**Type of field:** Text (formatted, long)  
**Application:**  
* A less formal description of the item, written using free text.
* Enter notes pertaining to the content of the resource that does not fit in a more specific field.
  *  Such notes should be as concise as possible!
* This field can also be used to note contents, missing pages, or condition notes for the physical item.
* You can use a note to explain discrepancies in dates, i.e. if there is a photograph on a postcard that was taken earlier than the postcard was printed, etc.

**Examples:**  
* "Extract from the Minutes." Signed by T[imothy] Matlack, secretary.
* A "correct copy of the record in the office of the Board of Revision of Taxes"; copied in Philadelphia, July 20, 1868
* Leather bound with blank pages.
* Blank pages were not scanned.
* (example of existing metadata made by an institution) Probably written by Esther Reed who assumed leadership of the women’s relief effort in Philadelphia. See Reed, William B. The life of Esther De Berdt, afterwards Esther Reed, of Pennsylvania (Philadelphia, 1853), p. 313-324.;Followed by, on p. [2]: Ideas, relative to the manner of forwarding to the American soldiers, the presents of the American women.;Imprint from colophon. The American Antiquarian Society copy was found bound after the June 10, 1780, issue of the Pennsylvania packet, printed at Philadelphia by John Dunlap. Articles related to the women’s efforts were printed in the Pennsylvania packet on June 13, 17, 27, July 8, and Nov. 4, 1780.

***

### **URL Alias**  
**Definition:** An alias for a default URL.  
**Obligation:** Optional; not repeatable  
**Enter Data into Spreadsheet Column:** url_alias  
**Type of field:** Text (plain)  
**Application:**  
* In this field, you will put the URL you would like for each of your objects, starting with the “/” following your root domain. 
* So if your site is mysite.com and an object on your existing site with a title of “My Object” has a URL of _mysite.com/islandora/object/islandora:123_, you could put in your CSV a URL alias for that object of _/islandora/object/islandora:123_. On ingest, that object will get a custom URL instead of /islandora/my-object.

 


