---
title: "Documentation Review"
teaching: 0
exercises: 0
questions:
- "Why is documentation important for reproducibility?"
- "What types of documentation are necessary to support reproducibility?"
- "What curation activities are associated with documentation review?"
objectives:
- "Understand why it is important to review deposited documentation, and create additional documentation."
- "Recognize documentation and documentation review best practices."
keypoints:
- "Study Identification is critical to ensure re-users are able to use the correct reproducibility package, contact study authors, and locate files and communications related to the study."
- "Keep the instructions succinct."
- "Using relative paths in your codes and a master file to execute them helps in simplifying the instructions." 
- "Information about the computing environment and the date the analysis was last run are crucial to rebuild the environment should the need arise."  
- "The Data Availability Statement should be clear enough for researchers to be able to access the same data used in the analysis and apply the same names used in the code so that the data may be called properly."
- "A codebook or data dictionary is critical to the interpretation of data and output files."
---
In this episode, we unpack the Data Quality Review Framework, focusing on Documentation Review. Other episodes in this lesson elaborate on File, Data, and Code Review.

## Documentation Review in Practice

Documentation supporting the use of data must be comprehensive enough to enable others to explore the resource fully, and detailed enough to allow someone who has not been involved in the data creation process to understand how the data were collected ([Digital Preservation Coalition, 2008, p. 25](http://127.0.0.1:4000/03-doc-review/index.html)).

This review step includes a review of the contextual documentation about the files, an assessment of whether the descriptive information about the files and about methods and sampling is comprehensive and sufficient for independent informed reuse, and the application of corrective actions where this information is missing, including creating documentation compliant with community standards and linking all other known related research products (e.g., publications, registries, grants) ([Peer et al., 2014](https://doi.org/10.2218/ijdc.v9i1.317)).

## Documentation Requirements

In addition to metadata, covered in Episode 2: File Review, robust stand-alone documentation is needed. This includes a README File, a Codebook or Data Dictionary, as well as other contextual Documentation.

> ## Documentation for Reproducibility
>
> “Documentation for data analysis workflows can come in many forms, including comments describing individual lines of code, README files orienting a reader within a code repository, descriptive commit history logs tracking the progress of code development, docstrings detailing function capabilities, and vignettes providing example applications. Documentation provides both a user manual for particular tools within a project (for example, data cleaning functions), and a reference log describing scientific research decisions and their rationale (for example, the reasons behind specific parameter choices).”
>
> Stoudt, S., Vásquez, V. N., & Martinez, C. C. (2021). Principles for data analysis workflows. *PLoS Computational Biology, 17*(3), e1008770. [https://doi.org/10.1371/journal.pcbi.1008770](https://doi.org/10.1371/journal.pcbi.1008770) 
{: .callout}

## README File

One of the key elements to successfully reproduce a study is clear instructions. A README file fulfills the author’s responsibility to include key information about the study (see this [README template](https://z.umn.edu/readme)). 

Review of a README file includes verification that key information is included and suggests areas for remediation if it is not. When it comes to information about reproducibility, a README file should also include information to provide context for the computation. This covers the following identifying information about the study and the files.

1. GENERAL INFORMATION
  - Title of the study 
  - Authors and institutional affiliation including ORCID
  - Corresponding author contact information (e-mail, address, phone number) 
  - Date published or finalized for releasePublisher, issue, and DOI (if published) 
  - Date of data collection
  - Geographic location
  - Information about funding sources that supported the collection of data
  - Overview of the data (similar to an abstract but about the dataset)

2. SHARING/ACCESS INFORMATION
  - Licenses/restrictions on the data also referred to as Data Availability Statement or Data Access Statement, signposts where the data associated with a paper are available, and under what conditions the data can be accessed, including links (where applicable) to the data set. 
  - Links to publications that cite or use the data (current manuscript as well as previous if any)
  - Source if data was derived from another source
  - Terms of use

3. DATA & FILE OVERVIEW
  - File list
       - Filename (for each file in dataset)
       - Short description (for each file in the dataset - what is this file)
  - Relationship between all the files (how they work together)

4. METHODOLOGICAL INFORMATION
  - Description of methods used for collection/generation of the data
  - Methods for processing the data(how the submitted data were generated from the raw or collected data)
  - Instrument or software specific information needed to interpret the data (include version, and the year of the software, additional libraries and  packages required to run the analysis). If the code takes more than a few minutes to run, consider adding an estimated time “Code takes 37 minutes to run) and the date it was last run successfully. Over time, some commands may not work because of updates made to the software or packages installed. Thus, it is very important to provide details about the computing environment at the time the researchers did their analysis so researchers have information to work on to help in rebuilding the environment should the program files no longer work in the future.
  - Description of any quality-assurance procedures performed on the data.

5. DATA-SPECIFIC INFORMATION FOR: [FILENAME] Create sections for each file of the dataset
  - Number of variables
  - Number of cases/rows:
  - Missing data code/ definition
  - Variable list
       - Variable name (for each variable):
       - Description (description of the variable) (value labels if appropriate)

6. COMPUTATIONAL ENVIRONMENT INFORMATION
  - Specify in detail the computing environment you have used to run your analysis:
       - Operating System and version (e.g., Windows 10, Ubuntu 18.0.4, etc.).
       - Number of CPUs/Cores.
       - Size of memory.
       - Statistical software package(s) used in the analysis and their version.
       - Packages, ado files, or libraries used in the analysis and their version.
       - Specify the file encoding if necessary. Example: UTF-8.
       - Estimate the time to complete processing (from beginning to end) using this computing environment.

Remember to keep the information and instructions succinct.

> ## Resource: README File
>
> See this resource for comprehensive guidance on writing a README file, including a list of recommended content, formatting standards, and a README document template.
>
> Cornell University Research Data Management Service Group. (n.d.). Guide to writing "readme" style metadata. [https://data.research.cornell.edu/content/readme](https://data.research.cornell.edu/content/readme) 
{: .callout}

### Data Availability Statement

It is possible that a research compendium may not include data due to data provider restrictions. For others to find, access, and use the data to reproduce results, a Data Availability Statement should include information about where to download the files, what to name them, and where to put them. For example: “Download this <specific file> from this website and put it in this <specific folder> in the active directory.” 

The Data Availability Statement should include the following essential elements: 

1. Name of Data Provider 
2. Title of Dataset 
3. Location or url of dataset 
4. License of dataset 
5. Date data was accessed 
6. Data citation (if available) 
7. Detailed instructions on how to gain access to the data (especially for restricted data) 
   - URL to Data Provider instructions if available 
   - Contact information of person with authority to grant access to data (if necessary)  
8. Name to assign the data (if has to be renamed) and where to put them in the reproducibility package, so it can be properly read by the code. 
9. Other notes  
 
Some examples of Data Availability Statements: [Taylor and Francis](https://authorservices.taylorandfrancis.com/data-availability-statement-templates/), [Springer Nature](https://www.springernature.com/gp/authors/research-data-policy/data-availability-statements/12330880)

Data Availability Statements can seem abstract when thinking about them hypothetically. This exercise is tailored to further our understanding of these statements by spending writing brief ones for different scenarios.

> ## Exercise: Data Availability Statement Exercise
>
> Write a data availability statement for the following: 
>
> 1. Data openly available in a public repository – (link to example) 
> 2. Data subject to third-party (data provider) restrictions – link to example
>
> > ## Solution
> >
> > 1. Published and public access data  
> > The data that support the findings of this study are openly available in [repository name] at http://doi.org/[doi], reference number [reference number].  Date accessed by the authors [dd-mmm-yyyy].  Download the <specific file> , use the default name, and put it in the  <specific folder> of the reproducibility package. 
> >
> > 2. Published, but with third-party restrictions  
> > The data that support the findings of this study are available [from] [third party]. Restrictions apply to the availability of these data, which were used under license for this study. Data are available [from the authors] at [URL] with the permission of [third party].  Date accessed by the authors [dd-mmm-yyyy].  Download the <specific file>, use the default name <or rename it to …>, and put it in the  <specific folder> of the reproducibility package. 
> >
> {: .solution}
{: .challenge}

## Codebook/Data Dictionary

A codebook or data dictionary is critical to the interpretation of data and output files. According to the [ICPSR](https://www.icpsr.umich.edu/web/ICPSR/cms/2042), a codebook generically includes information on the structure, contents, and layout of a data file.

Codebooks accompanying social science data typically include the following information about each variable, 

1. **Variable name and label.** For example, “g2004: Voted in the general elections of 2004.”
2. **Value labels.** A clear label to interpret each of the codes assigned to the variable. For example, “g2004: 1=yes, 0=no.”
3. **The exact question wording or the exact meaning of the datum.** Sources should be cited for questions drawn from previous surveys or published work. For example, “q2: political leaning (exact Q wording: “Do you lean more toward the Democratic or Republican party?” source: ANES)”
4. **Location in the data file.** Ordinarily, the order of variables in the documentation will be the same as in the file; if not, the position of the variable within the file should be indicated.
5. **Missing data codes.** Codes assigned to represent data that are missing. Different types of missing data should have distinct codes. For example: “g2004: 9=system missing.”
6. **Universe information, i.e., from whom the data was actually collected.** If this is a survey, documentation should indicate exactly who was asked the question. If a filter or skip pattern indicates that data on the variable were not obtained for all observations, that information should appear together with other documentation for that variable.
7. **Imputation and editing information.** Documentation should identify data that have been estimated or extensively edited.
8. **Details on constructed and weight variables.** Datasets often include variables constructed using other variables. Documentation should include “audit trails” for such variables, indicating exactly how they were constructed, what decisions were made about imputations, and the like. Ideally, documentation would include the exact programming statements used to construct such variables. Detailed information on the construction of weights should also be provided.
9. **Variable groupings.** For large datasets, it is useful to categorize variables into conceptual groupings.

> ## Resource: Creating a Codebook
>
> See this document on codebooks: Stephenson, Libbie, 2015, "About_Codebooks.rev072015.pdf", All About Codebooks, [https://doi.org/10.7910/DVN/U5FWYL/KLY4KT](https://doi.org/10.7910/DVN/U5FWYL/KLY4KT), Harvard Dataverse, V1
>
> Some statistical software can generate a codebook from the data file. For example, 
> 
> - Stata [https://www.stata.com/manuals/dcodebook.pdf](https://www.stata.com/manuals/dcodebook.pdf) 
> - R [https://cran.r-project.org/web/packages/codebook/index.html](https://cran.r-project.org/web/packages/codebook/index.html) 
> - SPSS (great resource from Kent State) [https://libguides.library.kent.edu/spss/codebooks](https://libguides.library.kent.edu/spss/codebooks)
{: .callout}

## Other Contextual Documentation

To help determine if data are “independently understandable for informed reuse,” other documentation may be helpful. Such contextual documentation helps inform the scholarly record. Some examples include the following. 

**Survey data**

- Interview schedules
- Interviewer and coder instructions (e.g., instructions for humans who are classifying open-ended survey responses, see [Pew Research Center example](https://www.pewresearch.org/global/2021/11/18/meaning-of-life-spring-2021-appendix-c-codebook/)). 
- Screening forms
- Call-report forms
- Consent form language
- Other disclosure requirements, see for example, the [American Association for Public Opinion Research (AAPOR)](https://www.aapor.org/Standards-Ethics/AAPOR-Code-of-Ethics/Disclosure-Standards.aspx) disclosure standards

**Experimental data**

- Electronic copies of materials used to administer the intervention (treatment). For example, mailings, transcripts of robo-calls, summary of curriculum, TV ads, audio files (see [ISPS example](https://isps.yale.edu/research/data/d003)). 
- Randomization procedure. The instructions should be presented in a way that, together with the design summary, conveys the protocol clearly enough that the design could be replicated by a reasonably skilled experimentalist.
- Informed Consent Statement.
- Pre-Analysis Plan. A document that formalizes and declares the design and analysis plan for the study. See [EGAP’s 10 Things to Know About Pre-Analysis Plans](https://egap.org/resource/10-things-to-know-about-pre-analysis-plans/).

**Administrative data**

- Data collection forms for transcribing information from records.

Utilizing the knowledge we have accumulated in Lesson 2, let’s put this theory into practice by interacting with existing data and its codebook. Digging in and interacting with real data and codebooks is the best way to familiarize yourself with the many possibilities. While there may not be one size fits all, there are various ways to include better practices by being proactive to what future users of data need to know to successfully reuse the data.  

> ## Title
>
> See data and codebook made available via OpenICPSR. 
>
> [check if codebook is complete; potentially use the same dataset as the one in the README exercise]
>
> Seltzer, Andrew J. Union Bank of Australia, Data and Codebook. Ann Arbor, MI: Inter-university Consortium for Political and Social Research [distributor], 2020-02-28. [https://doi.org/10.3886/E117971V1](https://doi.org/10.3886/E117971V1) 
>
> > ## Solution
> >
> > solution
> >
> {: .solution}
{: .challenge}

{% include links.md %}