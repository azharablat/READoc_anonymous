**Data-Driven Identification and Analysis of Waiting Times in Business Processes: A Systematic Literature Review**

Review Protocol

# Systematic Literature Review Protocol

# Introduction

Business analysts are in a continuous effort to improve the cycle time of a process by identifying waiting time bottlenecks and adapting strategies to improve the business processes by reducing delays (Ali, 2021). However, there are several sources of waiting times. For example, waiting times may be caused by resource contention — a resource is not starting an activity instance because it is busy with another activity — or by resource unavailability — a resource is off-duty (Toosinezhad, Fahland, Köroglu, & van der Aalst, 2020). In some cases, the source of waiting time may be external to the process, e.g. waiting for a response from a customer, waiting for a delivery from a supplier (Andrews & Wynn, 2017; Chapela-Campa & Dumas, 2022).

Given its prominent role, business analysts are often interested in identifying and quantifying waiting times in business processes, as well as analyzing the sources of these waiting times (Mannhardt, Arnesen, & Landmark, 2019; Nogayama & Takahashi, 2015). Numerous studies have advocated the use of data-driven techniques for identifying and analyzing waiting times in business processes (Andrews & Wynn, 2017; Fracca, de Leoni, Asnicar, & Turco, 2022). These studies have considered different notions and different causes of waiting times, and oftentimes, they rely on different approaches for quantifying waiting times. At present, there is a lack of a consolidated view of data-driven methods and techniques for identifying and analyzing waiting times in business processes.

To fill this research gap, this article presents a systematic literature review (SLR) aiming at cataloging and classifying existing data-driven methods and techniques for identifying and analyzing waiting times in business processes.

# Research Methodology

### This research aims at collecting and structuring existing knowledge about waiting times identification and analysis methods in business processes. The study is performed using a systematic literature review (SLR) and focuses on waiting times identification and analysis methods and what they prescribe. We develop a multi-dimensional taxonomy of waiting time identification, and analysis approaches in terms of their purpose, the techniques they rely upon, and the types of waiting times they address. This document presents the SLR review protocol.

### Planning of Systematic Literature Review

The SLR follows the guidelines suggested by (Webster & Watson 2002; Kitchenham and Charters 2007). SLR can be outlined in three main phases (Kitchenham & Charters 2007) – planning, conducting, and reporting. The first phase includes motivation for a review, the definition of research questions, development and evaluation of the review protocol. The second phase concerns identifying studies, selecting primary studies, quality assessment, data extraction, and data synthesis. Finally, the third phase considers the dissemination, formatting, and evaluation of the report. In this section, we elaborate on the first phase of SLR.

### Motivation for Review

The main objective of the SLR is to explore different data-driven techniques for waiting time identification and analysis in business processes. Therefore, we look for techniques that identify or analyze waiting times, what types of waiting types they address and how these approaches have been validated. As we aim for the notion of completeness, the SLR methodology is particularly suitable. SLR is methodologically rigorous in contrast to ad hoc reviews.

### Research Questions

To address the broader objective of this paper, we decomposed our overall research objective into a set of research questions. These research questions serve to address different aspects of data-driven approaches for waiting times identification and analysis in business processes.

***RQ1.*** *What objectives do existing data-driven approaches aim to achieve, and what techniques do they employ to identify and analyze waiting times in business processes?*

First, we aim to explore data-driven methods applied for waiting time identification and analysis in business processes. This question is the starting point because this involves collecting data on the technique applied and using this data to identify patterns and trends that can provide insight into the sources of waiting times and potential strategies for quantifying and validating the proposed approach.

***RQ2.*** *What sources of waiting times are these approaches designed to analyze?*

The second research question aims to categorize all sources of waiting times data-driven approaches try to identify or analyze and investigate their association with the internal or external factors affecting business processes.

***RQ3.*** *How do the identified approaches measure waiting times in business processes?*

The third research question explores how waiting times can be quantified in business processes.

***RQ4.*** *How have the identified approaches been validated?*

This research question refers to the strategies applied to effectively evaluate the
proposed techniques for waiting time identification and analysis in business processes.

## Search Strategy

The overall search strategy is to find a set of relevant scientific studies. The search strategy used in this SLR is based on the recommendations provided in studies and guidelines on conducting the SLRs (Rowley & Slack 2004; Okoli 2015). The search strategy included two phases, the primary and the secondary search, to secure essential studies were not missed. For the primary search, we used search strings on several electronic databases. Following the primary screening, we conducted a secondary search using backward referencing.

## Primary Search

The primary search aimed at enabling a comprehensive search to identify an initial set of candidate papers.

### Search String

In developing the search strings, we followed the guidelines suggested by (Kitchenham & Charters 2007). The range of terms used for the search included the following:

1. event log
2. process mining
3. workflow mining
4. waiting time
5. delay
6. shelf time
7. idle

*The first search term was event log to define the scope of the research area and the second term was waiting time to achieve our research goals. To further improve the search results, we considered including synonyms and expressions. We used process mining or workflow mining to supplement the event log because process mining and workflow mining derive from business process management. Similarly, we used delay, shelf time, or idle in addition to waiting time for obtaining a wider overview of the specific techniques.*

Based on the search terms, the following search string is formulated.

*(“event log” OR “process mining” OR “workflow mining”) AND (“waiting time ”OR “delay” OR “shelf time ”OR “idle”)*

### Search sources

The electronic databases were selected based on coverage of journal papers, conference proceedings, and workshop papers in the field of computer science, where research on process mining is primarily published (Brereton et al. 2007). The databases were also required to be freely accessible within the university domain. Hence, the following databases were used:

1. ACM Digital Library
2. IEEE Xplore
3. Scopus (includes SpringerLink)
4. Web of Science

**Secondary Search**

After identifying a comprehensive list of potentially relevant papers with the primary search and relevance screening, a secondary search, i.e., the backward search technique (Okoli & Schabram 2010) was used to identify additional relevant papers. We took the final list of papers produced from the primary search as a basis. During the data extraction from the primary list of papers, we marked references used in them that might be potentially relevant to our research. The resulting list of backward references was screened according to the same relevance criteria used for the primary search. The search was stopped when we did not discover any new relevant concepts as recommended by (Webster & Watson 2002).

## Selection Criteria

The purpose of the selection criteria is to identify relevant studies that provide sufficient information to address the research questions. The criteria consist of exclusion and inclusion criteria.

1. Exclusion criteria (EC):
   1. **EC1: The paper is digitally inaccessible.**

Papers accessible via digital libraries subscribed to by the university or available on the internet for free access are considered accessible. Papers provided for payment and not available via mentioned channels are deemed inaccessible.

* 1. **EC2: The paper is written in a language other than English.**

Papers not available in the English language are considered unavailable for review as it is impossible to understand them for the reviewers.

* 1. **EC3: The paper is a duplicate.**

Duplicate papers are papers with the same title from the same authors published in the same year that appear in different digital libraries (exact duplicate). Duplicates are also those published by the same authors with approximately the same topic (version duplicate). Only one is included in an exact duplicate, and the most recent version is included in the case of version duplicates. If some duplicates are the conference and journal versions, the journal version is included as it contains more research data.

* 1. **EC4: The paper is published in a non-peer-reviewed journal or
     other sources.**

Peer-reviewed journals are considered to be more credible and reliable sources of information because they have undergone a rigorous review process. Hence, the papers published in non-peer-reviewed journals or other sources were excluded.

1. Inclusion criteria (IC):
   1. **IC1: The paper presents/demonstrates a method, approach or technique to identify/analyze waiting times in business processes**

This criterion helps to filter out the literature that is out of the scope of the waiting time analysis in business processes. For example, studies related to process mining or workflow mining which mainly focuses on improving business processes by applying process mining techniques.

* 1. **IC2: The method, approach or technique presented/demonstrated in the paper uses event logs**

Based on this selection criterion, the studies that represent any theoretical discussion and/or practical application to identify or analyze waiting times in business processes are included.

## Screening Procedure

The screening is conducted according to a two-step procedure as recommended by (Kitchenham 2004; Brereton et al. 2007). One reviewer identified relevant primary studies based on the review of the title and, if needed, the study's abstract. The criteria used were the exclusion and inclusion criteria previously defined. The assessment was made following the inclusion criteria from top to bottom. If the paper failed to meet a criterion, it was excluded, i.e., the other criteria were not analyzed. To ensure unbiased screening, a second reviewer examined 10% of the list of papers. The sample was randomly selected. The value of 10% was selected following what ( Okoli 2011) proposed.

Papers from the backward search were examined against the inclusion criteria following the same procedure as the first screening. Following a top to bottom approach, if a paper failed an inclusion criterion, it was excluded without the other criteria being considered.

## Data Extraction Strategy

Following the identification of the final list of papers, relevant data were extracted. To ensure an unbiased data extraction strategy, a data extraction strategy was developed as recommended by (Brereton et al. 2007; Okoli 2015).

### Data Extraction Form

To proceed further with the data extraction stage, the data extraction form was developed. Data form allows for collecting data in a structured, unbiased, and consistent way. It is used to map the obtained insights from the paper review during the screening stage (Brereton et al. 2007; Okoli 2015). Based on the formulated research questions, the designed data form includes five categories of data:

1. **Paper metadata.** Data that helps identify the paper: paper title and authors, publication year, and Article Citation Count. Moreover, a unique identifier was assigned to each article to facilitate referencing in the data analysis stage.
2. **Data-Driven Analysis.** This data provides the reader with information regarding data-driven approaches utilized to identify or analyze waiting times in business processes.
3. **Sources Identified.** This data provides the reader with information about different sources of waiting times identified in the literature and their categorization based on the association with the internal or external factors affecting the business process.
4. **Quantification Method.** This data block describes different notions used for the quantification of waiting times in business processes.
5. **Validation Method.** Data about validation approaches used for analyzing waiting times in business processes.

The data extraction form with the definition of each parameter is presented in Table 1.

Table 1: Data Extraction Form

| **Meta Data** | *ID* | Unique paper identifier |
| --- | --- | --- |
| *Document Title* | Title of the paper |
| *Authors* | Authors of the paper |
| *Publication Year* | Year of publication of the paper |
| *Citation Count* | Number of citations received |
| **Data Driven Analysis** | *Data Driven technique (Identification or Analysis)* | Approach utilized to identify or analyze waiting times in business processes |
| *Purpose (As-Is, What-If, Data Quality/ Missing Timestamps)* | Waiting times supported form of analysis |
| **Sources Identified** | *Source of Waiting Time Identified* | Sources responsible for waiting times in business processes |
| *Internal/ External* | Association with the factors affecting the business process, either internal or external |
| **Quantification Method** | *Waiting Times Quantification* | Different notions used for quantification of waiting times in business processes |
| **Validation Method** | *Approach* | Validation approaches used for analyzing waiting times in business processes |

The data was extracted iteratively. First, a test portion of papers was extracted. Once the strategy, approach, and terminology were clarified, one of the authors extracted the data. A second reviewer randomly reviewed the extracted data. When there were questions, uncertainty, ambiguity, or differing views, both reviewers examined the paper and used a consensus approach to resolve discrepancies.

## Data Synthesis and Reporting

The extracted data were summarized and analyzed. The results were used to create a multi-dimensional taxonomy of waiting times identification and analysis approaches in terms of their purpose, the techniques they rely upon, and the types of waiting times they address. Following the research questions, the focus of the analysis was to aggregate and summarize the data and find the link between them.

# Results

This section presents the exact results of the paper search, selection, screening, and data extraction results.

**Primary Search**

The developed search strings were applied to each of the selected databases. The search results per source are shown in Table 2. The search result lists from all databases were downloaded and compounded in a single list that composed a total of 2612 publications.

Table 2: The Total Number of Papers Identified Per Source

| **Source** | **Papers Identified** |
| --- | --- |
| ACM Digital | 368 |
| IEEE Explore | 1284 |
| Scopus | 898 |
| Web of Science | 61 |
| **Total** | **2611** |

Based on the defined paper selection criteria, the selection procedure was executed as follows: first, data cleaning was conducted, then duplicates and papers containing fewer than five pages were removed, filtering by paper title and abstract was performed, and finally, filtering by reading the entire article was executed. Further, this section describes each of the filtering stages. Table 3 summarizes the data on the number of processed and filtered papers.

Table 3:The Results of the Selection Process

| **Filtering Stage** | **Number of Identified Papers** | **Total Number of Papers Left** |
| --- | --- | --- |
| *Primary Search Results* | 2611 |  |
| *Filtering by Paper Format* | 173 | 2438 |
| *Filtering out Duplicates* | 253 | 2185 |
| *Filtering by Paper Title and Abstract* | 1950 | 235 |
| *Filtering by Reading the Full Paper* | 130 | 105 |
| *After Backward Referencing* | 105+7 | 112 |

1. **Filtering by Paper Format.** At this stage, publications that are not available through the university's digital libraries or are not publicly available on the internet are omitted from the review. Publications that were not available in the English language or were published in non-peer-reviewed journals or other sources were also excluded. As a result, out of a total of 2611 papers, 173 papers were deleted, and 2438 articles advanced to the next level of screening.
2. **Filtering out duplicates.** Since there are four resources for paper search, some papers can inevitably occur in several resources, thus creating duplicates in the list of research papers for data extraction. Hence, the next step was to remove the duplicates from the list. 253 duplicates were identified and removed, leaving 2185 papers for the further filtering stage.
3. **Filtering by the paper title and abstract.** The rest of the papers are filtered by the title and abstract matching the research topic and question-driven by the selection criteria IC1. If it is evident from the title and the abstract that the paper does not relate to the research, it is removed from the list. If it is unclear, the paper is left for the next filtering stage. As a result of filtering the paper by title and abstract, 1950 papers were considered irrelevant for this research and removed from the list. 235 papers entered the next round of filtering which is filtering by reading the full paper.
4. **Filtering by reading the entire paper.** An additional 130 papers were filtered out from the list of relevant studies based on the selection criteria IC2, resulting in a list of 105 papers.

**Secondary Search (backward referencing).** We searched for references cited in the filtered list of primary papers, which could be relevant for the research, which resulted in 7 articles being included in the research. The final list of papers of this SLR comprised a total of 112 publications.

As a result of the filtering process, conducted based on determined inclusion/exclusion criteria, out of 2611 papers obtained from the primary search and 7 publications received from the secondary search, 112 articles were selected as eligible for this SLR.

## Overview of Publications

In this section, the overview of the papers included in the research will be presented. Based on the set inclusion and exclusion criteria, a total amount of 98 articles were considered eligible for the data extraction phase. The distribution of the papers over the years of publication is depicted in Figure 1.



Figure 1: Distribution of Papers per Publication Year

The complete list of 112 papers included in this SLR is presented in Table 4.

Table 4: Papers Included in the SLR

| **ID** | **Document Title** | **Authors** | **Publication Year** | **Citation Count** |
| --- | --- | --- | --- | --- |
| Aissaoui2022 | A BPMN-VSM based process analysis to improve the efficiency of multidisciplinary outpatient clinics | Aissaoui N.O., Ben Mbarek H., Layeb S.B., B. Hadj-Alouane A. | 2022 | 0 |
| Singh2021 | A collaborative method for simultaneous operations: case of an eye clinic | Singh S., Verma R., Koul S. | 2022 | 3 |
| Hompes2016 | A generic framework for context-aware process performance analysis | Hompes B.F.A., Buijs J.C.A.M., van der Aalst W.M.P. | 2016 | 38 |
| Khan2019 | A Generic Model for End State Prediction of Business Processes Towards Target Compliance | Khan N., Ali Z., Ali A., McClean S., Charles D., Taylor P., Nauck D. | 2019 | 3 |
| Drosouli2020 | A Process Mining Approach for Resource Allocation Management in a Bike Sharing System | Drosouli I,Theodoropoulou G,Miaoulis G,Voulodimos A | 2020 | 1 |
| Antunes2019 | A Solution Framework Based on Process Mining, Optimization, and Discrete-Event Simulation to Improve Queue Performance in an Emergency Department | Antunes, BBP; Manresa, A; Bastos, LSL; Marchesi, JF; Hamacher, S | 2019 | 13 |
| Dijkman2018 | Advanced queueing models for quantitative business process analysis | Dijkman R., Adan I., Peters S. | 2018 | 2 |
| Yampaka2016 | An application of process mining for queueing system in health service | T. Yampaka; P. Chongstitvatana | 2016 | 12 |
| Ganesha2017 | An approach to fuzzy process mining to reduce patient waiting time in a hospital | K. Ganesha; S. Dhanush; S. Raj S.M. | 2017 | 17 |
| Cho2019 | An Evidence-Based Decision Support Framework for Clinician Medical Scheduling | M. Cho; M. Song; S. Yoo; H. A. Reijers | 2019 | 24 |
| Gerhardt2018 | An Investigation to Identify Factors that Lead to Delay in Healthcare Reimbursement Process: A Brazilian case | Gerhardt R., Valiati J.F., Canto dos Santos J.V. | 2018 | 7 |
| ThomasVBP15 | An optimal process model for a real time process | Thomas L., Manoj Kumar M.V., Annappa B., Vishwanath K.P. | 2015 | 0 |
| Tridalestari2022 | Analysis of E-Commerce Process in the Downstream Section of Supply Chain Management Based on Process and Data Mining | Tridalestari F.A., Mustafid M., Warsito B., Wibowo A., Prasetyo H.N. | 2022 | 1 |
| Rojas2019 | Analysis of Emergency Room Episodes Duration Through Process Mining | Rojas E., Cifuentes A., Burattin A., Munoz-Gama J., Sepúlveda M., Capurro D. | 2019 | 12 |
| Ganesha2017 | Analyzing the waiting time of patients in hospital by applying heuristics process miner | K. Ganesha; K. V. Supriya; M. Soundarya | 2017 | 9 |
| Broderick2011 | Anomaly detection without a pre-existing formal model: Application to an industrial manufacturing system | J. A. Broderick; L. V. Allen; D. M. Tilbury | 2011 | 3 |
| Grabis2014 | Application of predictive simulation in development of adaptive workflows | J. Grabis | 2014 | 4 |
| Duong2021 | Assessing product quality from the production process logs | Duong L.T., Travé-Massuyès L., Subias A., Roa N.B. | 2021 | 2 |
| Pan2021 | Automated process discovery from event logs in BIM construction projects | Pan Y., Zhang L. | 2021 | 15 |
| Pufahl2014 | Batch Regions: Process Instance Synchronization Based on Data | L. Pufahl; A. Meyer; M. Weske | 2014 | 32 |
| Porouhan2018 | Behavioral Performance Evaluation and Emotion Analytics of a MOOC Course via Fuzzy Modeling | P. Porouhan; W. Premchaiswadi | 2018 | 4 |
| Satitcharoenmuang2017 | Benchmarking efficiency of children's garment production process using alpha and ILP replayer techniques | Satitcharoenmuang C., Porouhan P., Nammakhunt A., Saguansakiyotin N., Premchaiswadi W. | 2018 | 5 |
| Fitriansah2019 | Business Process Analysis of Academic Information System Application using Process Mining (Case Study: Final Project Module) | I. A. Fitriansah; R. Andreswari; M. A. Hasibuan | 2019 | 4 |
| Nguyen2016 | Business process performance mining with staged process flows | Nguyen H., Dumas M., Ter Hofstede A.H.M., La Rosa M., Maggi F.M. | 2016 | 28 |
| vanderAalst2015 | Change your history: Learning from event logs to improve processes | W. M. P. van der Aalst; W. Z. Low; M. T. Wynn; A. H. M. ter Hofstede | 2015 | 12 |
| Meincheim2017 | Combining Process Mining with Trace Clustering: Manufacturing Shop Floor Process - An Applied Case | A. Meincheim; C. d. S. Garcia; J. C. Nievola; E. E. Scalabrin | 2017 | 11 |
| Senderovich2019 | Context-aware temporal network representation of event logs: Model and methods for process performance analysis | Senderovich A., Weidlich M., Gal A. | 2019 | 7 |
| Rbigui2017 | Customer Oder Fulfillment Process Analysis with Process Mining: An Industrial Application in a Heavy Manufacturing Company | R'bigui H,Cho C | 2017 | 12 |
| Lashkevich2022 | Data-Driven Analysis of Batch Processing Inefficiencies in Business Processes | Lashkevich K., Milani F., Chapela-Campa D., Dumas M. | 2022 | 1 |
| Senderovich2015 | Data-driven performance analysis of scheduled processes | Senderovich A., Rogge-Solti A., Gal A., Mendling J., Mandelbaum A., Kadish S., Bunnell C.A. | 2015 | 23 |
| Fox2022 | Dental Extractions under General Anesthesia: New Insights from Process Mining | Fox F., Whelton H., Johnson O.A., Aggarwal V.R. | 2022 | 0 |
| deMan2019 | Detailed Performance Diagnosis Based on Production Timestamps: A Case Study | de Man J.C., Mannhardt F. | 2019 | 0 |
| Toosinezhad2020 | Detecting System-Level Behavior Leading To Dynamic Bottlenecks | Z. Toosinezhad; D. Fahland; Ö. Köroğlu; W. M. P. van der Aalst | 2020 | 12 |
| Raitubu2019 | Detection of Bottleneck and Social Network in Business Process of Agile Development | N. Raitubu; K. R. Sungkono; R. Sarno; C. S. Wahyuni | 2019 | 0 |
| Leemans2019 | Directly Follows-Based Process Mining: Exploration & a Case Study | S. J. J. Leemans; E. Poppe; M. T. Wynn | 2019 | 86 |
| PetitdemangeLFL20 | Enhancing emergency call centers’ performance through a data-driven simulation approach | Petitdemange E., Lamine E., Fontanili F., Lauras M. | 2020 | 0 |
| Fracca2022 | Estimating Activity Start Timestamps in the Presence of Waiting Times via Process Simulation | Fracca C., de Leoni M., Asnicar F., Turco A. | 2022 | 2 |
| Mannhardt2019 | Estimating the Impact of Incidents on Process Delay | F. Mannhardt; P. Arnesen; A. D. Landmark | 2019 | 6 |
| Nogayama2015 | Estimation of average latent waiting and service times of activities from event logs | Nogayama T., Takahashi H. | 2015 | 8 |
| Pika2016 | Evaluating and predicting overall process risk using event logs | Pika A., Van Der Aalst W.M.P., Wynn M.T., Fidge C.J., Ter Hofstede A.H.M. | 2016 | 45 |
| Zisimou2021 | Evaluation of Public Funding Processes by Mining Event Logs | A. Zisimou; I. Kalaitzoglou; G. Theodoropoulou; A. Bousdekis; G. Miaoulis | 2021 | 0 |
| Zaki2015 | Extracting accurate performance indicators from execution logs using process models | N. M. Zaki; A. Awad; E. Ezat | 2015 | 9 |
| Perimal14 | Health Intelligence: Discovering the Process Model Using Process Mining by Constructing Start-to-End Patient Journeys | Perimal-Lewis L,De Vries D,Thompson CH | 2014 | 29 |
| Leemans2018 | Hierarchical performance analysis for process mining | Leemans M., Van Der Aalst W.M.P., Van Den Brand M.G.J. | 2018 | 13 |
| Caesarita2017 | Identifying bottlenecks and fraud of business process using alpha ++ and heuristic miner algorithms (Case study: CV. Wicaksana Artha) | Y. Caesarita; R. Sarno; K. R. Sungkono | 2017 | 16 |
| SalimifardHM13 | Improving emergency department processes using Coloured Petri nets | Salimifard K., Hosseini S.Y., Moradi M.S. | 2013 | 10 |
| Leonardi2018 | Leveraging semantic labels for multi-level abstraction in medical process mining and trace comparison | Leonardi G., Striani M., Quaglini S., Cavallini A., Montani S. | 2018 | 23 |
| Ajmi2015 | Mapping patient path in the Pediatric Emergency Department: A workflow model driven approach | Ajmi I., Zgaya H., Gammoudi L., Hammadi S., Martinot A., Beuscart R., Renard J.-M. | 2015 | 30 |
| dosSantos2020 | Method to Reduce Lead-time of Business Process discovered | G. A. dos Santos; L. F. P. Southier; E. E. Scalabrin | 2020 | 1 |
| Mans2012 | Mining Processes in Dentistry | Mans R,Reijers H,van Genuchten M,Wismeijer D | 2012 | 58 |
| Mannhardt2019 | Mining railway traffic control logs | Mannhardt, F; Landmark, AD | 2019 | 6 |
| benSghaier2020 | Modeling the patient journey in a maternity unit of the UHC in Tunisia: An approach to overcrowding analysis | Ben Sghaier S., Mraihi R. | 2020 | 0 |
| Amissah2022 | Modelling Granular Process Flow Information to Reduce Bottlenecks in the Emergency Department | Amissah M., Lahiri S. | 2022 | 0 |
| Budai2019 | New approach for resource allocation indigital healthcare 4.0 | Kocsi, B; Pusztai, L; Budai, I | 2019 | 0 |
| Gupta2014 | Nirikshan: Mining Bug Report History for Discovering Process Maps, Inefficiencies and Inconsistencies | Gupta M,Sureka A | 2014 | 43 |
| JagadeeshChandraBose2015 | Opportunities for process improvement: A cross-clientele analysis of event data using process mining | Jagadeesh Chandra Bose R.P., Gupta A., Chander D., Ramanath A., Dasgupta K. | 2015 | 11 |
| Barbagallo2015 | Optimization and planning of operating theatre activities: An original definition of pathways and process modeling | Barbagallo S., Corradi L., De Ville De Goyet J., Iannucci M., Porro I., Rosso N., Tanfani E., Testi A. | 2015 | 96 |
| Senderovich2016 | P3-folder: Optimal model simplification for improving accuracy in process performance prediction | Senderovich A., Shleyfman A., Weidlich M., Gal A., Mandelbaum A. | 2016 | 14 |
| AboHamad2017 | Patient pathways discovery and analysis using process mining techniques: An emergency department case study | Abo-Hamad W. | 2017 | 18 |
| Stefanini2018 | Performance analysis in emergency departments: a data-driven approach | Stefanini A., Aloini D., Benevento E., Dulmin R., Mininno V. | 2018 | 34 |
| Rojas2019 | Performance analysis of emergency room episodes through process mining | Rojas E., Cifuentes A., Burattin A., Munoz-Gama J., Sepúlveda M., Capurro D. | 2019 | 29 |
| Rofiif2019 | Performance Analysis of Hierarchical Process Model | A. N. Rofiif; M. M. Wildan; K. R. Sungkono; R. Sarno; C. S. Wahyuni | 2019 | 0 |
| Klijn2019 | Performance Mining for Batch Processing Using the Performance Spectrum | Klijn E.L., Fahland D. | 2019 | 18 |
| Rahardianto2018 | Performance Time Evaluation of Domestic Container Terminal Using Process Mining and PERT | R. Rahardianto; R. Sarno; G. Intani Budiawati | 2018 | 6 |
| Low2014 | Perturbing event logs to identify cost reduction opportunities: A genetic algorithm-based approach | W. Z. Low; J. De Weerdt; M. T. Wynn; A. H. M. ter Hofstede; W. M. P. van der Aalst; S. vanden Broucke | 2014 | 16 |
| PlaGML11 | Petri net based agents for coordinating resources in a workflow management system | Plà A., Gay P., Meléndez J., López B. | 2011 | 5 |
| Pla2012 | Petri net-based process monitoring: A workflow management system for process modelling and monitoring | Pla A., Gay P., Meléndez J., López B. | 2014 | 59 |
| Park2020 | Predicting performances in business processes using deep neural networks | Park G., Song M. | 2020 | 32 |
| RoggeSolti2015 | Prediction of business process durations using non-Markovian stochastic Petri nets | Rogge-Solti A., Weske M. | 2015 | 113 |
| Mesabbah2018 | PRESENTING A HYBRID PROCESSING MINING FRAMEWORK FOR AUTOMATED SIMULATION MODEL GENERATION | M. Mesabbah; S. McKeever | 2018 | 0 |
| Sitova2020 | Process Data Analysis Using Visual Analytics and Process Mining Techniques | I. Sitova; J. Pecerska | 2020 | 2 |
| Zhou2014 | Process mining based modeling and analysis of workflows in clinical care - A case study in a chicago outpatient clinic | Z. Zhou; Y. Wang; L. Li | 2014 | 45 |
| Dogan2022 | Process mining based on patient waiting time: an application in health processes | Dogan O. | 2022 | 3 |
| Pang2021 | Process mining framework with time perspective for understanding acute care: a case study of AIS in hospitals | Pang J., Xu H., Ren J., Yang J., Li M., Lu D., Zhao D. | 2021 | 0 |
| Gupta2014 | Process Mining Multiple Repositories for Software Defect Resolution from Control and Organizational Perspective | Gupta M,Sureka A,Padmanabhuni S | 2014 | 47 |
| Premchaiswadi2015 | Process modeling and bottleneck mining in online peer-review systems | Premchaiswadi W., Porouhan P. | 2015 | 51 |
| Pika2013 | Profiling event logs to configure risk indicators for process delays | Pika A., Van Der Aalst W.M.P., Fidge C.J., Ter Hofstede A.H.M., Wynn M.T. | 2013 | 31 |
| Goel2022 | Quality-Informed Process Mining: A Case for Standardised Data Quality Annotations | Goel K,Leemans SJ,Martin N,Wynn MT | 2022 | 2 |
| Zeng2020 | Resource Conflict Checking and Resolution Controller Design for Cross-Organization Emergency Response Processes | Q. Zeng; C. Liu; H. Duan; M. Zhou | 2020 | 20 |
| Martin2016 | Retrieving Resource Availability Insights from Event Logs | N. Martin; F. Bax; B. Depaire; A. Caris | 2016 | 12 |
| Rudnitckaia2022 | Screening Process Mining and Value Stream Techniques on Industrial Manufacturing Processes: Process Modelling and Bottleneck Analysis | J. Rudnitckaia; H. S. Venkatachalam; R. Essmann; T. Hru&#x0161;ka; A. W. Colombo | 2022 | 0 |
| Andrews2017 | Shelf Time Analysis in CTP Insurance Claims Processing | Andrews, R; Wynn, M | 2017 | 5 |
| Agostinelli2020 | Supporting Governance in Healthcare Through Process Mining: A Case Study | S. Agostinelli; F. Covino; G. D'Agnese; C. De Crea; F. Leotta; A. Marrella | 2020 | 8 |
| SenderovichWG17 | Temporal network representation of event logs for improved performance modelling in business processes | Senderovich A., Weidlich M., Gal A. | 2017 | 0 |
| Jaisook2015 | Time performance analysis of medical treatment processes by using disco | P. Jaisook; W. Premchaiswadi | 2015 | 19 |
| CanturkC06 | Time-based workflow mining | Canturk D., Cicekli N.K. | 2006 | 0 |
| Denisov2018 | Unbiased, fine-grained description of processes performance from event data | Denisov V., Fahland D., van der Aalst W.M.P. | 2018 | 50 |
| Martin2016 | Using event logs to model interarrival times in business process simulation | Martin N., Depaire B., Caris A. | 2016 | 11 |
| Vasilyev2013 | Using Inductive Reasoning to Find the Cause of Process Delays | E. Vasilyev; D. R. Ferreira; J. Iijima | 2013 | 14 |
| Ferreira2015 | Using logical decision trees to discover the cause of process delays from event logs | Ferreira D.R., Vasilyev E. | 2015 | 33 |
| vanderAalst2020 | Visualizing Token Flows Using Interactive Performance Spectra | van der Aalst W.M.P., Tacke Genannt Unterberg D., Denisov V., Fahland D. | 2020 | 10 |
| **Literature Retrieved Through Backward Referencing** | | | | |
|
| Denisov2020 | Repairing event logs with missing events to support performance analysis of systems with shared resources | Denisov, Vadim and Fahland, Dirk and van der Aalst, Wil MP | 2020 | 15 |
| Senderovich2016 | Discovering queues from event logs with varying levels of information | Senderovich, Arik and Leemans, Sander JJ and Harel, Shahar and Gal, Avigdor and Mandelbaum, Avishai and van der Aalst, Wil MP | 2016 | 30 |
| RoggeSolti2014 | Temporal anomaly detection in business processes | Rogge-Solti, Andreas and Kasneci, Gjergji | 2014 | 64 |
| vanDongen2010 | Process mining: fuzzy clustering and performance visualization | van Dongen, Boudewijn F and Adriansyah, Arya | 2009 | 79 |
| DavidDumas | Modeling Extraneous Activity Delays in Business Process Simulation | David Chapela-Campa; Marlon Dumas | 2022 | 0 |
| Wombacher2013 | Start Time and Duration Distribution Estimation in Semi-Structured Processes | Wombacher, Andreas and lacob, Maria-Eugenia | 2013 | 10 |
| Wombacher2011 | Towards a Performance Estimate in Semi-Structured Processes | Wombacher, Andreas, Maria Iacob, and Martin Haitsma. | 2011 | 9 |

# References

Ali, Muhammad Awais. "Why Am I Waiting? Analyzing Waiting Times in Business Processes from Event Logs." (2021).

Toosinezhad, Zahra, Dirk Fahland, Özge Köroğlu, and Wil MP Van Der Aalst. "Detecting system-level behavior leading to dynamic bottlenecks." In *2020 2nd International Conference on Process Mining (ICPM)*, pp. 17-24. IEEE, 2020.

Andrews, Robert, and Moe Wynn. "Shelf time analysis in CTP insurance claims processing." In *Pacific-Asia Conference on Knowledge Discovery and Data Mining*, pp. 151-162. Springer, Cham, 2017.

Chapela-Campa, David, and Marlon Dumas. "Modeling Extraneous Activity Delays in Business Process Simulation." In *2022 4th International Conference on Process Mining (ICPM)*, pp. 72-79. IEEE, 2022.

Mannhardt, Felix, Petter Arnesen, and Andreas D. Landmark. "Estimating the impact of incidents on process delay." In *2019 International Conference on Process Mining (ICPM)*, pp. 49-56. IEEE, 2019.

Nogayama, Takahide, and Haruhisa Takahashi. "Estimation of average latent waiting and service times of activities from event logs." In *International Conference on Business Process Management*, pp. 172-179. Springer, Cham, 2016.

Fracca, Claudia, Massimiliano de Leoni, Fabio Asnicar, and Alessandro Turco. "Estimating Activity Start Timestamps in the Presence of Waiting Times via Process Simulation." In *International Conference on Advanced Information Systems Engineering*, pp. 287-303. Springer, Cham, 2022.

Brereton, Pearl, Barbara A. Kitchenham, David Budgen, Mark Turner, and Mohamed Khalil. "Lessons from applying the systematic literature review process within the software engineering domain." *Journal of systems and software* 80, no. 4 (2007): 571-583.

Fink, Arlene. *Conducting research literature reviews: From the internet to paper*. Sage publications, 2019.

Kitchenham, Barbara. "Procedures for performing systematic reviews." *Keele, UK, Keele University* 33, no. 2004 (2004): 1-26.

Keele, Staffs. *Guidelines for performing systematic literature reviews in software engineering*. Vol. 5. Technical report, ver. 2.3 ebse technical report. ebse, 2007.

Okoli, Chitu. "A guide to conducting a standalone systematic literature review. "*Communications of the Association for Information Systems* 37, no. 1 (2015): 43.

Okoli, C., and K. Schabram. "A Guide to Conducting a Systematic Literature Review of Information Systems Research. Ssrn, 10 (2010)." (2011).

Webster, Jane, and Richard T. Watson. "Analyzing the past to prepare for the future: Writing a literature review." *MIS quarterly* (2002): xiii-xxiii.

Kitchenham, Barbara, and Stuart Charters. "Guidelines for performing systematic literature reviews in software engineering." (2007).

Rowley, Jennifer, and Frances Slack. "Conducting a literature review." *Management research news* (2004).