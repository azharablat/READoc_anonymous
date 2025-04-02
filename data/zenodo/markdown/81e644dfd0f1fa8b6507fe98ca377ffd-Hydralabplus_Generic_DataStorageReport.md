Data Storage Report

[Title of Project]

[photo(s) taken during experiment]

[TEXT IN SQUARE BRACKETS IS A GUIDE FOR COMPLETING DOCUMENT IT SHOULD BE REMOVED AND REPLACED AS DOCUMENT IS WRITTEN]

Project Information

| **Acronym** |  |
| --- | --- |
| **Title** |  |
| **Location(s)** |  |
| **WWW link(s)** | [e.g. Web page links] |
| **Social Media** | [e.g. twitter handle or blog links] |
| **Start date** | [dd-mm-yyyy] |
| **End date** | [dd-mm-yyyy] |

Project Personnel

| **Name** | **Institution** | **Email** | **OCRID-iD** |
| --- | --- | --- | --- |
|  |  |  |  |
|  |  |  |  |

Document History

| **Date** | **Status** | **Author(s)** | **Reviewer** | **Approver** |
| --- | --- | --- | --- | --- |
|  | Draft |  |  |  |
|  | Final |  |  |  |

Document objective

This data storage report describes the project and how data were collected. The data are described so that others can use them.

Acknowledgement

[Give Funding information- HYDRALAB+ acknowledgement given below]

The work described in this publication was supported by the European Community’s Horizon 2020 Research and Innovation Programme through the grant to HYDRALAB-PLUS, Contract no. 654110.

Disclaimer

This document reflects only the authors’ views and not those of the European Community. This work may rely on data from sources external to the HYDRALAB-PLUS project Consortium. Members of the Consortium do not accept liability for loss or damage suffered by any third party as a result of errors or inaccuracies in such data. The information in this document is provided “as is” and no guarantee or warranty is given that the information is fit for any particular purpose. The user thereof uses the information at its sole risk and neither the European Community nor any member of the HYDRALAB-PLUS Consortium is liable for any use that may be made of the information.

License

 <http://creativecommons.org/licenses/by/4.0/>

Contents

1 Introduction 4

1.1 Scientific background 4

1.2 Aims and Objectives 4

2 Experimental setup 5

2.1 General description of experimental setup 5

2.2 General data storage principles and organization of data files 5

2.3 Definition and application of spatial and temporal reference systems 5

2.4 Relevant fixed parameters 5

2.5 Test Programme 5

3 Instrumentation – NAME1 [Add chapters for each instrument used in project] 6

3.1 Instruments 6

3.2 Measured parameters 6

3.3 Experimental procedure 6

3.4 Data post-processing 6

3.5 Organization of data files 6

3.6 Remarks 6

4 Instrumentation – NAME2 [Add chapters for each instrument used in project] 7

4.1 Instruments 7

4.2 Measured parameters 7

4.3 Experimental procedure 7

4.4 Data post-processing 7

4.5 Organization of data files 7

4.6 Remarks 7

5 References 8

6 Appendices 9

The draft Data Storage Report should be completed BEFORE the tests have started. After the tests, the the final Data Storage Report should be completed, but this may be an iterative process. The report describes the data and how it is stored in order to make it available for those interested. Note that for HYDRALAB ACCESS user groups, they have the first right of publication during a period of two years, but after that any European researcher should be able to use the data.

The data storage report should contain a list of instruments, tests conducted, a full explanation of parameters, and all other relevant information. It also contains a list of files, and a description of what is in the files (identify what is in each column in the table that is stored in the file, such as 'time (s)', 'pressure at location 1 (Pa)', etc., including type of column separator). It should be made clear which test corresponds with which file. Give also the data type: binary / ascii.

The report should be updated as often as necessary, particularly during the tests.

Remove this text box when using this format for a data storage report.

# Introduction

## Scientific background

[This should briefly describe the context for the project]

## Aims and Objectives

[This should describe the aims and objectives of the data collection and the intended use for the data]

# Experimental setup

## General description of experimental setup

[Description of the project setup(s), dimensions of the project domain(s), list of instrumentation used for data collection (details for each given in subsequent chapters]]

[Drawing of the experimental setup]

Figure 2.1: [figure title]

## General data storage principles and organization of data files

[Projects are recommended to follow a data storage hierarchy similar to that outlined below, to clearly distinguish raw and processed data and identify the type of data linked to the data storage report, some reports may only contain L0 and L1 data and only some L1 data may be processed to L2 level]

Data are stored at a maximum of three levels:

1. L0 as raw as the instruments allow (all data);
2. L1 with standard instrument filtering/processing (only usable data, i.e. measurements with incorrect settings, test bursts etc. removed), including (reference to) processing tools and settings
3. L2 (optional) with advanced processing, e.g. combining multiple data sources or statistics, sub-sampled for interesting relevant periods (fully processed), including (reference to) processing tools and settings

All data needs to be stored in at least L0 and L1; storage of L2 data is only relevant for selected subsets.

[The format of the data files can be chosen freely for efficient and easy storage and handling, as long as it is well described in the metadata.]

## Definition and application of spatial and temporal reference systems

[Origin of axis system, positive directions of axes. Explain how instrument positions are measured (e.g. survey system) or how instrument movement is controlled (e.g. traverses)]

[Describe the time system used (absolute or relative). If measurements are collected simultaneously and with the same data acquisition system, describe this system. If measurements are synchronized, describe how this is achieved. If measurements are asynchronous explain how they can be compared to each other]

## Relevant fixed parameters

[Independent variables that will not change during the tests and their values]

## Test Programme

[Describe the test programme including which instruments are used and (if appropriate) applied changes to boundary conditions. This could be presented in a table].

# Instrumentation – NAME1 [Add chapters for each instrument used in project]

## Instruments

[Description of the instrument used in the tests. Manufacturer, model and serial numbers should be identified where appropriate]

[Positions of the instruments, could be tabulated]

Table 3.1: [table title]

|  |  |  |  |
| --- | --- | --- | --- |
|  |  |  |  |

## Measured parameters

[Which parameters are measured by the instrument and give units of measurement]

## Experimental procedure

[Description of how measurements were taken; instrument settings and calibration. This should be like the methods section of a paper].

## Data post-processing

[Describe applied processing/filtering]

## Organization of data files

[Description of the data files:

* format (ASCII or binary)
* column separator (in case of ASCII)
* type of data (video of measurement data)
* units of data
* structure of file content
* organization of files in directories]

## Remarks

[Use this section for comments that cannot be placed in other sections]

# Instrumentation – NAME2 [Add chapters for each instrument used in project]

## Instruments

[Description of the instrument used in the tests. Manufacturer, model and serial numbers should be identified where appropriate]

[Positions of the instruments, could be tabulated]

Table 3.1: [table title]

|  |  |  |  |
| --- | --- | --- | --- |
|  |  |  |  |

## Measured parameters

[Which parameters are measured by the instrument and give units of measurement]

## Experimental procedure

[Description of how measurements were taken; instrument settings and calibration. This should be like the methods section of a paper].

## Data post-processing

[Describe applied processing/filtering]

## Organization of data files

[Description of the data files:

* format (ASCII or binary)
* column separator (in case of ASCII)
* type of data (video of measurement data)
* units of data
* structure of file content
* organization of files in directories]

## Remarks

[Use this section for comments that cannot be placed in other sections]

# References

# Appendices

[For example: test diary, technical drawing of experiment]