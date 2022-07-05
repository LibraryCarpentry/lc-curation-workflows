---
title: "Data Review"
teaching: 0
exercises: 0
questions:
- "Why is data review important for reproducibility?"
- "What curation activities are associated with data review?"
objectives:
- "Understand why it is important to review deposited data"
- "Recognize data review best practices"
keypoints:
- "Data must be checked for missing or ambiguous variable and value labels."
- "Observation counts should be consistent across files."
- "Data values should be in range, and error-free."
- "Metadata and references to the data in associated files should be checked for consistency and accuracy."
- "PII should be identified and anonymized or removed."
- "Clear metadata about who created, owns, and stewards the data, and what the licensing terms are for reuse, should be created."
---
In this episode, we unpack the Data Quality Review Framework, focusing on Data Review. Other episodes in this lesson elaborate on File, Documentation, and Code Review.

## Data Review in Practice

A data quality review also involves some processing – examining and enhancing – of the data. These actions require performing various checks on the data, which may be automated or manual procedures. It often requires opening the data file with the appropriate software.

The United Kingdom Data Archive (UKDA) provides a comprehensive list of things to check: ‘double-checking coding of observations or responses and out-of-range values, checking data completeness, adding variable and value labels where appropriate, verifying random samples of the digital data against the original data, double entry of data, statistical analyses such as frequencies, means, ranges or clustering to detect errors and anomalous values, correcting errors made during transcription’ ([UKDA, n.d]()). 

In addition, data need to be reviewed for risk of disclosure of research subjects’ identities, of sensitive data, and of private information… and potentially altered to address confidentiality or other concerns.” ([Peer et al., 2014](https://doi.org/10.2218/ijdc.v9i1.317))

Reviewing deposited data can seem abstract when thinking about it hypothetically. The exercises throughout this episode are tailored to further our understanding of data review by spending some time with example files. The exercises ask you to identify problems with the data and suggest resolutions. The Solution copies of the example data highlight issues and show ways of resolving them.

## Variables and Values

Confirm that all variables in the data files contain variable and value labels. Look for ambiguous variable labels, and clarify the units of measurement for the variables. Clarify what the use of “blanks” means for this data.

Confirm that the variable and value labels are consistent across metadata and other associated files. For each variable, review the documents for metadata about that variable and ensure the metadata exists and is consistent. Confirm also that any recoded or transformed variables are properly described in metadata and other associated files.

> ## Exercise: Variables and Values
>
> Review the sample questionnaire, codebook, and data file.
>
> - Do all the variables have labels?
> - Are there discrepancies between variables or values in the data and other associated files?
>
> > ## Solution
> >
> > Do all the variables have labels?
> > - One column of the .csv data has a missing label (should be: GENDER)
> > 
> > Are there discrepancies between variables or values in the data and other associated files?
> > - Gender variable: data has values ‘nonbin’, while codebook and questionnaire indicate the value was recorded as ‘nonbinary’ 
> > - Gender = ‘other’ occurs 3 times in the data, but codebook indicates its frequency is 0
> {: .solution}
{: .challenge}

## Dataset Errors

Data must be examined for inconsistencies and errors.

### Observation counts
Confirm that the number of observations in the data file matches the number of observations the study claims to have had, either in published articles or associated files such as the codebook or readme.

### Out of range or wild codes
Identify any out-of-range or wild codes (response codes that are not authorized for a particular question or variable)

### Missing values and other errors
Identify any missing (undefined null) values or other potential errors in the data. Check for invalid values, or for metadata that incorrectly specifies the constraints for a variable. Be sure no data look double-entered, or incorrectly transcribed.

It can help here to compare a sample of the data to any original data files, including physical ones, if data has been copied over or transcribed. Review summary statistics to verify that they fall within the expected values for the variable. 

Familiarizing oneself with common errors is a strategic method that can be integrated into workflow processes. Understanding key areas to concentrate on can offset some of the more laborious parts of the work. The more we do, the more confident we can become which can lead to more efficiency. Let’s get more familiar by engaging in the next challenge. 

> ## Exercise: Dataset Errors
>
> Review the sample study article, codebook, and data file.
>
> - Are there any observation count discrepancies?
> - Are all the data in bounds for each variable?
> - Are there undefined null values or other errors?
>
> > ## Solution
> >
> > Are there any observation count discrepancies?
> > - The data has 2810  rows of observations, while the codebook and published article indicates observations were collected from 2812 participants
> >
> > Are all the data in bounds for each variable?
> > - Some of the ages listed are 0, 100, 200, and are clearly out of bounds (participants are in high school)
> >
> > Are there undefined null values or other errors?
> > - The Form data field has text values and blank values, when the codebook indicates it should be numeric and only values 1 or 2
> {: .solution}
{: .challenge}

## Personally-Identifiable Information (PII)

If a research compendium is being prepared for public access, and human subjects data is present, identify any variables that contain data that could identify study participants.

Two kinds of variables could endanger research participants' confidentiality: direct identifiers and indirect identifiers.

Direct identifiers are variables that point explicitly to particular individuals or units, such as names, addresses, and identifying or linkable numbers (e.g. student IDs, Social Security numbers, driver's license IDs, etc.). Any direct identifiers should be removed or masked prior to depositing.

Indirect identifiers are variables that can be used together or in conjunction with other information to identify individual respondents. Examples include detailed geographic information, exact job, office or organization titles, birthplaces, and exact event dates. Indirect identifiers may be re-coded in various ways, such as converting dates to time intervals, and geographic codes to broader levels of geography.

> ## Spotlight: Removing PII
> Remove or anonymize any personally identifiable information in the data files. 
>
> Removing PII from a data file may be a manual process, or could involve either using statistical software (e.g., Stata, R) to edit or write new code, or running a program/script that deletes or otherwise transforms these variables and writes out a new revised version of the data file, and adding the resulting data file to the catalog record (as well as any new code file).
{: .callout}

There are times when data authors are too close to their data and not able to easily see PII when it is time to share their data widely. The following challenge helps us think about how the nuances of a variable can lead to PII and the workarounds that curators can assist with to allow for sharing the data. Knowing these better practices and advocating for  them with data authors will allow data to be shared which may not have been if the data was not de-identified.

> ## Exercise: Anonymizing Data
>
> Review the example data file: 2018-Kim-dataset_final.csv.
>
> - Which information counts as personally identifiable information (PII)?
> - How would you anonymize the PII in this file?
>
> > ## Solution
> >
> > Which information counts as PII in the example file?
> > - Name, Address
> >
> > How would you anonymize any personally identifiable information in the example data file?
> > - Name → redact this column
> > - Address → transform to City or Country only
> {: .solution}
{: .challenge}

{% include links.md %}