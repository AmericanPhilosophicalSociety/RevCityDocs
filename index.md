---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---

# The Revolutionary City: A Portal to the Nation's Founding

## Documentation and Workflows

![Rev City logo]({{ site.baseurl }}/assets/APS_Revolutionary-City_NestedLogo.jpg)

### About RevCity

This project was created by the [American Philosophical Society (APS)](https://www.amphilsoc.org){:target="_blank"}, the [Historical Society of Pennsylvania (HSP)](https://www.portal.hsp.org/){:target="_blank"}, and the [Library Company of Philadelphia (LCP)](https://librarycompany.org/){:target="_blank"}. The APS and LCP, founded by Benjamin Franklin, and the HSP, founded to celebrate the memory of the Revolution, hold large and invaluable collections related to the American Revolution and the early national period. But whereas the stories of founders like Franklin and Jefferson are well known, the scattered nature of the records of lesser-known actors has made those lives less accessible to wide audiences. Over the past three years, these institutions created a [shared online portal](https://therevolutionarycity.org){:target="_blank"} of digitized archival material related to the American Revolution (1774-1783) to break down the institutional barriers between these archives. In an unprecedented way, this portal allows users to discover stories highlighting the lives of a more diverse Philadelphia that have previously been obscured by the physical separation of collections.

The Revolutionary City will educate Americans on the founding moment and its legacy, engage them to better understand and participate in civil dialogue through historical examples, and unite them in an appreciation of the diversity of the American experience and the common bonds that hold its citizens together. This project has been shaped by extensive public-facing, publicly engaged experience of stakeholders from Philadelphia-area research libraries, history museums, and community colleges to make heretofore hidden collections broadly available. 

### About this repository

This repository aggregates documentation for workflows and best practices for RevCity. Its goal is to provide a public point of reference for interns, staff, and current and future partners. It will also document technical project activities and planning and serve as a guide for future projects that would like to replicate RevCity. At present, the guide covers two broad topics, but will be expanded as the project grows.

- [Digitization Guidelines]({{ site.baseurl }}/digitization)
- [Transcription Guidelines]({{ site.baseurl }}/transcription)

### Technical information

RevCity is built in [Islandora](https://www.islandora.ca/){:target="_blank"}, an open-source, [Drupal](https://www.drupal.org/){:target="_blank"}-based Digital Assets Management System. RevCity's Islandora instance was built and is maintained by [Born Digital](https://www.born-digital.com/){:target="_blank"}.

Active development is underway to leverage [IIIF](https://iiif.io/){:target="_blank"} and [OAI-PMH](https://www.openarchives.org/pmh/){:target="_blank"} to import content from partner institutions.

Transcriptions are managed in a [local instance](https://transcription.amphilsoc.org){:target="_blank"} of [eScriptorium](https://gitlab.com/scripta/escriptorium){:target="_blank"}, a Django-based transcription platform that integrates the HTR software [kraken](https://github.com/mittagessen/kraken){:target="_blank"}. Additional HTR work is being conducted with [TrOCR](https://huggingface.co/docs/transformers/en/model_doc/trocr){:target="_blank"}.

The code used for interoperability between these two platforms and for the processing of transcriptions is forthcoming.
