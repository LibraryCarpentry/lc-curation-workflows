---
title: File Review
teaching: 0
exercises: 0
---

::::::::::::::::::::::::::::::::::::::: objectives

- Understand why it is important to review deposited files
- Recognize file review best practices

::::::::::::::::::::::::::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::: questions

- Why is file review important for reproducibility?
- What curation activities are associated with file review?

::::::::::::::::::::::::::::::::::::::::::::::::::

In this episode, we unpack the Data Quality Review Framework, focusing on File Review. Other episodes in this lesson elaborate on Documentation, Data, and Code Review.

## File Review in Practice

File review is an important part of the Data Quality Review (DQR) covered in the previous episode. This episode will outline best practices to ensure the integrity of files in the reproducibility package.

Data reuse relies on clearly identified, functional, and long-term accessible files. Tasks associated with file review include inspecting the files and identifying file format-specific curation tasks, creating persistent identifiers and metadata, and creating preservation file formats. Preservation-oriented steps, such as implementing a migration strategy for file formats, and ongoing bit monitoring, are also part of file review.

File review is especially important as a preparation for packaging the files for deposit into a trustworthy repository for long-term access and sharing (see [Lesson 4: Compendium Packaging](https://curating4reproducibility.org/cure-carpentry-04-packaging/)).

## File Inspection

Files must be inspected to ensure that they are all present and correctly named, and that they open. File sizes and formats may be recorded and checksums created.

File inspection tasks may include the following:

- Review list of files to verify that they are all present
- Check files for viruses using anti-virus software
- Open each file to verify that it opens as expected and is not corrupt or inoperable
- Verify the content of each file matches the expected format
- Ensure that file names conform to any applicable naming convention, and that they are internally consistent if one file references another by name
- Identify any missing metadata that the depositor had been expected to submit

## File Format-specific Curation Tasks

Some aspects of file review may vary based on the file format or subject domain. The [Data Curation Network Primers](https://hdl.handle.net/11299/202810) have helpful curation process recommendations for particular file formats.

:::::::::::::::::::::::::::::::::::::::::  callout

## Spotlight: Data Repository Metadata

Data curation involves the creation of metadata at both the file level and the study level to facilitate further data quality review and discoverability. Required metadata fields vary by repository, but should be mapped to standard metadata schemas for preservation and interoperability.

Metadata librarians or other metadata experts on staff may create a Metadata Application Profile for the data repository that data curators refer to to know what metadata to create for each deposit they curate.

Here are some resources for identifying metadata fields to include:

- [Digital Curation Centre list of research data metadata standards](https://www.dcc.ac.uk/resources/subject-areas/general-research-data)
- [DataCite list of core metadata properties for minting a DOI](https://schema.datacite.org/)
- [Citation and domain-specific metadata schemas supported by Dataverse](https://guides.dataverse.org/en/latest/user/appendix.html#user-appendix)
  

::::::::::::::::::::::::::::::::::::::::::::::::::

## Verify and Enhance File-Level Metadata

Verify and enhance metadata associated with each individual file. Metadata-related tasks may include:

- Verify any file-level metadata provided by the depositor
- Create or enhance any necessary file-level metadata, such as:
  - File format or resource type
  - File size
  - Author/Creator/Source
  - Rights
  - Persistent Identifier
  - Checksum
  - Last verified date

:::::::::::::::::::::::::::::::::::::::::  callout

## Spotlight: Fixity in Digital Preservation

Fixity, in the preservation sense, means the assurance that a digital file has remained unchanged, i.e. fixed. Fixity helps establish trust between data producers, stewards (e.g. repositories and archives), and users.

Fixity checking is the process of verifying that a digital object has not been altered or corrupted. A checksum on a file is a 'digital fingerprint' used to detect if the contents of a file have changed.  Checksums can be generated using a range of readily available and open source tools.

See more information here:

- <https://www.dpconline.org/blog/wdpd/jmitcham-wdpd21>
- <https://www.dpconline.org/handbook/technical-solutions-and-tools/fixity-and-checksums>
- <https://blogs.loc.gov/thesignal/files/2014/02/>
- <https://en.wikipedia.org/wiki/Checksum>
  

::::::::::::::::::::::::::::::::::::::::::::::::::

### Code File Metadata

Curators may want to enhance the metadata for code files, which includes some specific fields. For example,

- Date the code was last updated
- Date the code was last executed
- Code citation with DOI
- Code license
- Character encoding
- Software, version, and operating system information

:::::::::::::::::::::::::::::::::::::::::  callout

## Spotight: Software Metadata

If the research compendium includes software, curators may add or enhance associated metadata.
The Software Metadata Recommended Format Guide (SMRF) summarizes and defines the
metadata elements recommended by the Software Preservation Network to describe
software materials in the context of a wide range of collections.

Christophersen, Allan. Colón-Marrero , Elena. Dietrich, Dianne. Falcao, Patricia. Fox, Claire. Hanson, Karen. Kwan, Allen. McEniry, Matthew. (2022, February 8). Software Metadata Recommended Formats Guide. Software Preservation Network. <https://www.softwarepreservationnetwork.org/smrf-guide/>


::::::::::::::::::::::::::::::::::::::::::::::::::

## Transform or Migrate to Preservation Formats

Files that are not in a preservation format (e.g., .csv, .txt, .pdf), and do not have a built-in converter, should be manually converted to a preservation format. Transforming files into non-proprietary formats facilitates potential reuse and ensures the files remain accessible long term. For files from proprietary statistical software (e.g. .dta, .sav, .do, and others), both a converted preservation format file and the original file may be included in the reproducibility package.

:::::::::::::::::::::::::::::::::::::::::  callout

## Spotlight: Preservation Formats

Some resources for identifying recommended preservation formats:

- Library of Congress Recommended Formats
- Cornell eCommons' recommended file formats and probability for long-term preservation matrix
- OpenAIRE Data formats for preservation
- National Archives Tables of File Formats
- UK Data Service Recommended formats
- UK National Archives
  

::::::::::::::::::::::::::::::::::::::::::::::::::

## Verify and Enhance Study-Level Metadata

Verify and enhance metadata to be applied at the level of the study. Metadata-related tasks may include:

- Verify any study-level metadata provided by the depositor
- Create or enhance any necessary study-level metadata, such as:
  - Creator, creator affiliation, ORCID or researcher unique identifier
  - Title
  - Description
  - Language
  - Publication Date
  - Rights \& License
  - Temporal coverage, spatial coverage
  - Funding Source
  - Citations to related work
- Create a study-level citation
- Create the catalog record and assign it a persistent identifier

:::::::::::::::::::::::::::::::::::::::::  callout

## Study Mnemonic

Following good data management practice, researchers would have created a project folder for the study that contains all the files used in the study. The name of the project folder should be unique to identify the particular set of files. This study mnemonic is also useful for reviewers who can use it to tag communications with authors and as codebook identifiers in archives.

An example reproducibility package done by CISER's Results Reproduction Service team with study mnemonic ("R2-2019-MEEMKEN-1") used as Codebook Identifier and e-mail subject tags to track communications with authors: <https://archive.ciser.cornell.edu/reproduction-packages/2828>.


::::::::::::::::::::::::::::::::::::::::::::::::::

Reviewing deposited research files quality can seem abstract when thinking about it hypothetically. The exercise below is tailored to further our understanding of file review by spending some time with example files. The exercise asks you to identify problems with the files and suggest resolutions. The Solution copy of the example files shows ways of resolving the issues.

:::::::::::::::::::::::::::::::::::::::  challenge

## Exercise: File Review Challenge

Review the example files for inclusion in a research compendium. Make recommendations to resolve any issues. In real life, you would communicate with the researchers to resolve any missing files or problematic issues you found.

- The depositors submitted a file list document: 2018-Kim-Documentation.docx. Are all files present?
- The study mnemonic "2018-Kim" will be used for this example. Do the files follow the appropriate naming convention?
- Do all the files open? If not what is the problem?
- Record file sizes. Does anything look off?
- What study-level metadata could be suggested based on these files?
- Should any files be converted to a different file format for preservation?

:::::::::::::::  solution

## Solution

**Are all files present?**

- The file 2018-Kim-anonymized\_participants.xlsx, listed in 2018-Kim-Documentation.docx is missing.

**Do files follow the appropriate naming convention?**

- One file "analysis\_final.do" disobeys the convention.

**Do all the files open?**

- One file 2018-Kim-Acknowledgements.xlzx has a typo in the file extension that prevents it from opening.
- One file is a .dta file, which requires Stata
- The .do file is run in Stata, but can be viewed in any text editor

**Record file sizes**

- One file 2018-Kim-questionnaire.txt is 0 Kb.

**Suggest study-level metadata**

- Dc.creator = Kim, Hyuncheol Bryant
- Dc.title = Reproduction Materials for: The Role of Education Interventions in Improving Economic Rationality
- Dc.language = english
- Dc.language.iso = eng
- Dc.creator.orcid = 0000-0001-5304-0274
- Dc.relation.isreferencedby = Choi, Syngjoo, Kim, Hyuncheol Bryant, Kim, Booyuel, et al. "The role of education interventions in improving economic rationality." Science. Volume 362, Issue 6410 (2018-10-05): 83-86. <https://doi.org/10.1126/science.aar6987>.

**Recommend a preservation format for each file**

- .xlsz → .csv
- .docx → .txt
- .dta → .csv
- .do → .txt
- For proprietary file formats, it is best practice to include both a preservation format version and the original proprietary format version of the file in the reproducibility package. E.g. include both the submitted .dta file and a .csv version
  
  

:::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::::::::::::::::



:::::::::::::::::::::::::::::::::::::::: keypoints

- Files must be inspected.
- Study and file metadata should be detailed, accurate, and formatted in a standard schema.
- Aspects of file review may vary based on file format.
- Transforming files into non-proprietary formats facilitates reuse and ensures long term accessibility.

::::::::::::::::::::::::::::::::::::::::::::::::::


