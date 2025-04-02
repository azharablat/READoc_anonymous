An Explainable & Secure Artificial Intelligence platform for the manufacturing industry – Applications & lessons learnt

Konstantinos Perakis*1*, Silvia Rodriguez *2* and Fenareti Lampathaki*3*

1 UBITECH, Thessalias 8, 15231, Athens, Greece

3 Asociación de Empresas Tecnológicas Innovalia, Calle Rodriguez Arias, 6 Dto. 605, 48008 Bilbao, Spain.

4 Suite5 Data Intelligence Solutions, Alexandreias 2, Limassol, Cyprus

Abstract (UBI)

Abstract text.

Keywords (UBI)[1]

XMANAI, explainable,

# Introduction (UBI)

Despite the fact that AI undeniably plays a crucial role in the ongoing transformation of the manufacturing industry, its accomplishments are being scrutinized due to the escalating complexity of black-box AI models that lack transparency [1]. AI-driven systems often provide limited visibility and understanding of decision-making processes and predictions, as many algorithms used cannot be scrutinized in a manner that humans can comprehend the specifics of how and why a decision was reached. Consequently, despite AI being a driving force for smart factories, manufacturing sites exhibit strong reluctance to adopt it, primarily due to the lack of trust in decisions and uncertainty about where and how it should be integrated into the manufacturing pipeline [2]. In response to this challenge, Explainable Artificial Intelligence (XAI), enabling end-users to understand both the algorithmic decisions and the data that influenced those decisions [3], has been proposed as a solution to eliminate the black-box effect and move towards more transparent AI solutions. XAI holds the potential of enhancing the comprehensibility of results, and thereby increasing their trustworthiness, fostering their increased adoption in critical domains such as the manufacturing industry [4].

This paper introduces the innovative XMANAI Explainable AI platform [5], which relies on explainable AI models to instill trust, enhance human understanding, and address concrete manufacturing challenges through value-based explanations. The platform leverages the latest advancements in AI and breakthroughs in XAI to construct "glass box" AI models that are explainable to a "human-in-the-loop," without significantly sacrificing AI performance, thus addressing significant challenges faced by data scientists, such as lifecycle management, security, and trusted sharing of complex AI assets. It aims at overcoming critical barriers to AI adoption in the manufacturing industry and at enabling the design and execution of AI pipelines by manufacturing industry stakeholders. The current paper also introduces the validation of the XMANAI platform. The validation of the platform was realized across four discrete real-life manufacturing domains, including automotive, white goods, machinery, and metrology, spanning across discrete and diversified use cases, which were supported by a set of innovative manufacturing applications and services. The current paper discusses the problems faced by the stakeholders involved in these application scenarios, the uptake of the XMANAI platform towards addressing these challenges and problems and the impact of this uptake in daily operations, and also discusses the lessons learnt from the scientific, technical and business perspective.

# The XMANAI Platform (1.5 page) (UBI)

The primary goal of the XMANAI platform is to present a pioneering Explainable AI platform. This platform allows manufacturing stakeholders to utilize explainable AI models to address specific manufacturing challenges in a trustworthy manner. The platform achieves this by offering value-based explanations that are easily understandable and effective for humans. At its core, the platform comprises a catalog of hybrid and graph AI models. These models are developed, fine-tuned, and validated to serve as either baseline AI models applicable to various manufacturing problems or trained AI models specifically fine-tuned for different issues.

The XMANAI platform efficiently manages the entire lifecycle of AI assets. This encompasses steps such as data uploading, exploration, preparation, and sharing, leading to data analysis. The platform also facilitates the design and execution of AI pipelines, incorporating value-based explanations and meaningful visualizationson- throughout the process.

The XMANAI Platform is structured as a collection of service bundles arranged into various tiers. These tiers are crafted and executed using cutting-edge data handling, data manipulation, and AI technologies and tools. The XMANAI Platform architecture comprises of three core tiers, namely: a) the XMANAI Cloud infrastructure which constitutes the core part of the platform and represents the centralized cloud instance of the XMANAI Platform, b) the XMANAI On Premise Environments which represent the parts of the XMANAI Platform that can be hosted and executed in a private cloud instance of a stakeholder and c) the XMANAI Manufacturing Apps Portfolio which is composed of AI manufacturing intelligence solutions that are effectively solving specific manufacturing problems. The XMANAI Cloud infrastructure comprises of a) the Core AI Management Platform that provides all the offerings and functionalities of the platform and is responsible for the design of the data and / or AI pipelines and the orchestration of their execution; and b) the Secure Execution Clusters (SEC) which constitute the isolated per stakeholder organization spaces which are triggered/spawn on demand by the Core AI Management Platform, for executing data and / or AI pipelines. The XMANAI On Premise Environments facilitate the execution of the platform’s functionalities on the stakeholders’ environments based on the instructions that are provided by the XMANAI Cloud infrastructure in accordance with the preferences of the stakeholder.

**Figure 1**: The XMANAI Platform Architecture

The XMANAI platform's services are developed and integrated into eight distinct bundles, ensuring seamless integration through well-defined interfaces. These bundles facilitate intercommunication among the services and contribute to the overall functionality of the XMANAI platform, and include the:

1. **Data Collection & Governance Services bundle**: Itensures consistent and well-managed data collection by configuring and executing appropriate data handling processes. It securely and reliably collects data assets and incorporates a provenance mechanism to track their lifecycle.
2. **Scalable Storage Services bundle**: It facilitates the persistence of platform assets based on their types and storage locations, and provides metadata indexing to optimize query performance and enhance data discoverability.
3. **Data Manipulation Services bundle**: Its core functionalities include data explainability and feature engineering. It enables the derivation and harmonization of knowledge from available data based on the XMANAI data model, and prepares the data for ML/DL applications, allowing its usage in training XAI models and executing XAI pipelines.
4. **XAI Execution Services bundle**: It is responsible for executing XAI model/pipeline experiments during the experimentation phase and deploying XAI pipelines in the production phase based on user-defined schedules. It monitors and tracks the execution status in the Secure Execution Clusters and/or the On-Premise Environments, ensuring the storage of model/pipeline results and associated metrics.
5. **XAI Insight Services bundle**: It facilitates collaboration between business experts and data scientists and supports gaining insights throughout different phases of extracting manufacturing intelligence. It incorporates the XAI Visualization Engine, which offers novel dashboards and diagrams to visually represent data, XAI model results, explanations, and insights, thereby supporting the entire experimentation process.
6. **XAI Lifecycle Management Services bundle**: It manages XAI pipelines, encompassing collaborative design, validation, and handling of the pipelines. It integrates various functionalities such as data preparation, model engineering, and explainability, as well as training, explanation generation, management, tracking, and evaluation of XAI models, considering performance and security aspects.
7. **Secure Asset Sharing Services bundle**: It enables cataloging and trusted sharing of data and AI models across various manufacturing organizations and/or users. These functionalities are provided through the XAI Marketplace.
8. **Platform Management Services bundle**: Its responsibilities include access control functionalities for data assets based on providers' preferences, centralized user management, and authentication mechanisms for the platform.

With the exception of the XAI Lifecycle Management Services bundle, the Secure Asset Sharing Services bundle and the Platform Management Services bundle which reside only in the XMANAI Cloud Infrastructure, all other service bundles can reside on both the XMANAI Cloud infrastructure and the XMANAI On-Premise Environments.

# The XMANAI Platform Application in Real-Life Scenarios

The previously described XMANAI services and bundles will provide the 4 manufacturing demonstrators of the XMANAI project with a clear path to obtain explanations of the processes behind artificial intelligence-assisted applications.

Retrieving explainability requirements from the 4 demonstrators has been the unavoidable step that contributed to the definition of an implementation process of the platform in real life scenarios. Data ingestion, processing and analytics is another of the main pillars of the process, that must seamlessly address the data governance.

Finally, the XMANAI platform has taken into account the relevance of offering a strong, reliable and agile tool for selecting and training strong ML models and algorithms to solve the specific needs of each organization.

## Demonstrator #1 - FORD

### Business problem statement (0.25 page) (INNOV)

The Ford demonstrator takes place at the Valencia engine plant (Spain-Valencia) and is focusing on managing the complexity of manufacturing in terms of variability. The plant is working with weekly batches, managed manually using the expertise of MP&L (Material Planning & Logistics) and production staff. Currently, the assembly line is manufacturing 25 different derivatives (i.e., engine types) depending on the vehicle in which they will be installed.

Currently, the performance of the entire plant depends on the correct planning of the batches and the "MIX" that the planning engineer has scheduled based on customer demand and his experience. Furthermore, line production depends on the shift foreman's decision to minimize planned stoppages and failures during the shift.

In this scenario, FORD needs to improve the plant performance and both the availability of the production line and its efficiency by providing smart capabilities to operators and engineers in order to choose the best operation decision at any given moment [6].

### XMANAI Explainability and Platform Uptake

Thanks to the XMANAI platform, Ford wants to offer to its manufacturing engineers a holistic overview of the production lines, identifying specific parts of the line that may affect the global availability of the line, during the period of time comprising the current shift and the one immediately after it.

In the Ford Demonstrator, Random forest has been identified as the ML model that better fits the needs of the company for the overview and management of the production line, and it will be combined with LIME as the explainability tool. On the other hand, and to better adapt to the manufacturing use case, the XMANAI platform provides the option to also implement Graph ML models for explainability, and so, GAT has been used in the Ford demonstrator. These models have been trained in the XMANAI platform with Ford real production data to offer accurate predictions on the performance of the production lines.

### XMANAI Platform Added Value & Impact Assessment

In the FORD demonstrator, the XMANAI platform is helping ingest, manage and analyze the data by Ford’s corporate systems, as well as programmed data contained in the MP&L, maintenance and tooling systems, to obtain recommendations for optimizing line performance through different scenarios and to deeply understand which factors have a bigger influence in the results of the predictions and why.

During the evaluation of the Ford demonstrator, both the efficiency and the availability of the production lines have been measured while helping end users to visually identify the main culprits or responsible elements influencing the manufacturing process. The first results are promising and improve the trust and confidence in the predictions of the platform that will finally positively impact in the quality of the decisions that the manufacturing engineers do on a daily basis.

## Demonstrator #2 - WHIRLPOOL

### Business problem statement

WHIRLPOOL demonstrator is focused on the demand forecasting for a D2C (Direct To Customer) business case. Direct to Consumer is a business channel only recently activated by Whirlpool in European markets. It consists in the direct sale of Whirlpool products, within a defined range and brand portfolio active for that specific country, to a final consumer through a web portal.

Due to the novelty of this business channel and due to the complexity induced by Whirlpool demand-driven production planning process, the capability to effectively forecast the D2C demand and to acquire a deep knowledge of the business dynamics are crucial for the success in this innovative and challenging market sector.

The reliable demand predictability is not the only result expected from the demonstrator: the knowledge of demand dynamic and of the explanation of some forecasting effects, is very important in order to empower business stakeholders in driving and developing the business itself. [7]

### XMANAI Explainability and Platform Uptake

One of the main tasks related to the XMANAI platform uptake has been the implementation of an appropriate predictive model for the sales forecasting along with a suitable explainability model. During the experimentation phase, the focus was given to the development of various forecasting models for individual products and product categories with the most sales. The models were evaluated using appropriate evaluation metrics and the most promising results were obtained by boosting models and specifically XGBoost.

Regarding the explainability aspect of the task, descriptive visualizations depicting features’ correlations and their influence on the target value were employed to provide initial explainability insights. After developing the predictive models, a range of explainability tools were utilized, including SHAP, permutation importance, counterfactuals and what-if scenarios, to generate additional explanation results

The Whirlpool use case has leveraged all available components of the XMANAI platform in order to properly ingest the sales data, share them with the technical support partners, design and configure XAI pipelines and schedule their execution on a weekly basis.

### XMANAI Platform Added Value & Impact Assessment

The XMANAI platform, along with the accompanying manufacturing app (that is custom for the Whirlpool demand forecasting problem) offers to Whirlpool the possibility to deeply understand the business dynamic through further investigating the correlations among the various identified factors, the visualization of hidden phenomena and the experimentation on the forecasted effect of some control variables.

Even if in the Whirlpool use case, the evaluation of the XMANAI solution is not easy as the comparison of DFE for the D2C market only is not available, it has been done manually and the users highlighted a meaningful improvement between the XMANAI weekly DFE results in comparison to the average DFE baseline values, demonstrating the potential benefit driven by the usage of this system to support enrichment forecast decisions making for D2C.

## Demonstrator #3 - CNH

### Business problem statement

Within CNHi's production plant, the needs of the operators who face downtime issues every day lie in restoring the machinery, the beating heart of the plant, in such a quick timeframe that it does not cause major production losses.

Even if the plant is well-represented in plant layout and logistic warehouse is tracked on daily bases, during a normal shift of drivelines, the production lines are suffering unplanned and planned stoppages, due to machine stop or unexpected maintenance operation, that are affecting their availability; such stoppages are typically requiring to replace worn components (i.e. tooling), to maintain manufacturing conditions, such as cleaning the machine of the chips produced during the process, or are caused by components malfunction (i.e. broken tools, inductive switches, electro valve). Another important issue is the performance loss and the bad quality of the product, which is caused by faulty components (not perfectly in line with 3D-2D models), poor lubrication, bad machine setup, etc. and results in an increased machine cycle time, affecting the entire line as lines are configured for mass production (one operation feeds the next operation). [8]

### XMANAI Explainability and Platform Uptake

Thanks to the XMANAI platform, CNHi wants to retrieve quality data automatically from the Heller 400, the machine in the production plant selected for the use case, and from this obtain suggestions from the XAI algorithms to identify which component to replace or maintain to ensure optimum machine performance.

To do so, Isolation Forest has been selected as the proper ML model to be trained thanks to the XMANAI platform as it has good performance with multiple irregular time series of different length. The trained ML models are then exploited to generate the needed explanations using a combination of custom tools and standard graphs, taken from the SHAP library and keeping into account the explainability requirements provided by the end users.

All but 2 of the components of the XMANAI platform have been utilized to implement the CNHi demonstrator.

### XMANAI Platform Added Value & Impact Assessment

The CNHi demonstrator thanks to the XMANAI platform is able to provide to the end-user quality information about the operating condition of the machine being monitored and assist him/her in understanding of where and why a failure occurred on the machine.

The main focus of this demonstrator was on the human-machine collaboration by exploiting the XAI suggestions offered by the XMANAI platform and use them to boost the diagnosis phases during stoppage in plant. Even with simulated sessions that reproduced the occurrence of failures, a high ratio of relevant information shared between the XAI and blue-collar workers in collaborative troubleshooting during the evaluation session has been detected and therefore, the trust of the production managers in the explainable predictions has been considered as medium from a starting point that was not implementing any AI solution.

## Demonstrator #1 - UNIMETRIK

### Business problem statement

UNIMETRIK is a technological developer in the field of dimensional metrology services that provides solutions to the manufacturing industry in terms of calibration, parts measurement and metrological engineering. Companies dedicated to manufacturing parts for the automotive, aeronautical, and similar sectors are receiving dimensional quality requirements and tolerances from large companies. Compliance with these requirements leads to the use of optical technology for the realization of dimensional quality controls.

Currently, the optical measurement system used by UNIMETRIK, has its information processing software parameterizable associated with it. However, depending on the experience of the metrologist that is operating the software, one result or another will be obtained which the developers design as a “black box”, making it difficult to verify how they can process this information. This affects directly the accuracy of the measurement that may vary. More errors and so, more iterations of the measurement process may be necessary for a good output, and as a result, the amount of time dedicated to the process as a hole increases. [9]

### XMANAI Explainability and Platform Uptake

Firstly, the formulated regression task of predicting point measurement errors with respect to the surface of convex objects, has been broken down in three axes (X, Y, Z) in order to study the parameters that mostly affect the scanning instrument’s response in each direction. Based on that, datasets for experimentation have been generated that have led to the identification of AI components of Hybrid XAI models such as Artificial Neural Network (NN) and Support Vector Machine (SVM) regressors as the most suitable ones to provide more detailed prediction per axis and further enhance the metrologist's understanding via individual explainability results for each axis. The selected NN and SVM models have been trained and fine-tuned on partitions of the available data on the XMANAI platform.

As for the explainability components to the Hybrid XAI models, SHAP and Permutation Importance are the tools selected to explain the predictions of NN and SVM models respectively. Consequently, unique explanations for each axis can be delivered, enabling an elevated degree of comprehensibility regarding the laser scanning performance along each of the three axes. Both methods assign feature attributions, explaining the importance of input features to the model’s outcome.

All but 2 of the components of the XMANAI platform have been utilized to implement the UNIMETRIK demonstrator.

### XMANAI Platform Added Value & Impact Assessment

The current UNIMETRIK demonstrator thanks to the XMANAI platforms allows metrologists to better understand the level of uncertainty that the captured points ‘positions have in different parts of the object under analysis based on a certain key parameters configuration.

It is highly remarkable that even if the geometrical properties of the object under metrological study of course cannot change, thanks to the results and explanation offered by the platform, the operator can change the laser orientation to adjust the geometric setup of the scanning device, in order to better capture areas of the object with large predicted errors in the current setup. In addition, during the first evaluation of the demonstrator, experience metrologists have perceived a clear reduction of the most frequent errors.

# Conclusions & Discussion

Implementing the XMANAI platform in the 4 manufacturing demonstrators has led to the identification of relevant lessons that will help the growth of the adoption of explainable AI solutions in the industry. As a general overview and from the business perspective, it is relevant to involve in the process as many different profiles as possible to align the explainability solutions to the actual needs of the organization. Moreover, it is mandatory to establish data quality controls and validate the consistency and coherence of the available data no avoid inaccuracy in the results provided by the platform and lack of reliability in the explanations and conclusions. Furthermore, the support of a structured change management, which includes communication and focused training actions towards data scientists and data engineers, seems to be the key success factor for the successful introduction of XMANAI platform into a business organization.

From the technical perspective, it is really important to adequately assess the quantity and quality of data that could be used in the experimentation phase is critical when establishing the model training processes. Moreover, it is important to realistically manage the expectations when working on explainable AI solutions to solve the organization's problems/needs. Having a process that helps to reformulate the scope is necessary to avoid losing end user confidence in the platform.

# Acknowledgements

The research leading to this work has received funding from the European Union’s Horizon 2020 research and innovation programme under Grant Agreement No: 957362

# References

1. W. Saeed and C. Omlin, “Explainable AI (XAI): A systematic meta-survey of current challenges and future opportunities,” *Knowledge-Based Systems*, vol. 263, p. 110273, 2023.
2. S. W. Kim, J. H. Kong, S. W. Lee, and S. Lee, “Recent advances of artificial intelligence in manufacturing industrial sectors: A Review,” International Journal of Precision Engineering and Manufacturing, vol. 23, no. 1, pp. 111–129, 2021.
3. A. Krajna, M. Kovac, M. Brcic, and A. Sarcevic, “Explainable artificial intelligence: An updated perspective,” 2022 45th Jubilee International Convention on Information, Communication and Electronic Technology (MIPRO), 2022.
4. XMANAI. [Online]. Available: <https://ai4manufacturing.eu/>. [Accessed: 14-Mar-2023]
5. A novel Explainable Artificial Intelligence and secure Artificial Intelligence asset sharing platform for the manufacturing industry for the manufacturing industry. Accepted for publication at 29th ICE IEEE/ITMC Conference (ICE 2023).
6. Perez-Castanos, S., Prieto-Roig, A., Monzo, D., Colomer-Barbera, J. (2024). Holistic Production Overview: Using XAI for Production Optimization. In: Soldatos, J. (eds) Artificial Intelligence in Manufacturing. Springer, Cham. <https://doi.org/10.1007/978-3-031-46452-2_24>
7. Lampathaki, F. et al. (2024). XAI for Product Demand Planning: Models, Experiences, and Lessons Learnt. In: Soldatos, J. (eds) Artificial Intelligence in Manufacturing. Springer, Cham. <https://doi.org/10.1007/978-3-031-46452-2_25>
8. Sesana, M. et al. (2024). Process and Product Quality Optimization with Explainable Artificial Intelligence. In: Soldatos, J. (eds) Artificial Intelligence in Manufacturing. Springer, Cham. <https://doi.org/10.1007/978-3-031-46452-2_26>
9. Lavasa, E. et al. (2024). Toward Explainable Metrology 4.0: Utilizing Explainable AI to Predict the Pointwise Accuracy of Laser Scanning Devices in Industrial Manufacturing. In: Soldatos, J. (eds) Artificial Intelligence in Manufacturing. Springer, Cham. <https://doi.org/10.1007/978-3-031-46452-2_27>

# List of Figures

**Figure 1**: The XMANAI Platform Architecture

1. Proceedings Name, Month XX–XX, YYYY, City, Country

   EMAIL: email1@mail.com (A. 1); email2@mail.com (A. 2); email3@mail.com (A. 3)

   ORCID: XXXX-XXXX-XXXX-XXXX (A. 1); XXXX-XXXX-XXXX-XXXX (A. 2); XXXX-XXXX-XXXX-XXXX (A. 3)

   |  | ©️  2020 Copyright for this paper by its authors.Use permitted under Creative Commons License Attribution 4.0 International (CC BY 4.0). |
   | --- | --- |
   |  | CEUR Workshop Proceedings (CEUR-WS.org) |

   ↑