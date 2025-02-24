# GPCNKB_data
The datasets  used in the GPCNKB paper include the following components:

(1) CVE, CWE, and CAPEC Data: These three datasets are sourced from the official websites of CVE and NVD. The relationships between them are obtained by crawling the NVD website.

(2) **Role of the Three Datasets**: These datasets provide the model with multi-dimensional information, thereby enhancing its comprehensive capabilities. For these datasets, we primarily utilize their description fields.  

 **CVE (Common Vulnerabilities and Exposures)**: The description field of CVE provides detailed information about each known vulnerability, including the vulnerability name, affected systems or software versions, specific manifestations, attack methods, potential impacts, and available fixes or mitigation measures.  It focuses on the technical details of vulnerabilities, offering characteristics of vulnerabilities and possible attack paths, providing a foundation for attack behavior recognition and classification.  

**CWE (Common Weakness Enumeration)**: The description field of CWE includes the name of the weakness, its detailed description, the scope of its impact, and the root causes that may lead to the weakness. It reveals the underlying causes of vulnerabilities, such as coding defects, design errors, or system configuration issues. This information helps the model understand the nature and origin of vulnerabilities at a deeper level. When incorporated as feature words into the feature matrix, the model can classify vulnerabilities more accurately based on their root causes, as it can identify the type and impact of vulnerabilities by combining these technical details. Furthermore, if this information is transformed into embedding vectors, the model can capture the potential relationships between vulnerabilities and attack behaviors, uncovering the logical patterns behind attacks. This deeper understanding enables the model to infer possible attack methods triggered by vulnerabilities more accurately, thereby improving the overall precision and reliability of reasoning.

**CAPEC (Common Attack Pattern Enumeration and Classification)**: The description field of CAPEC provides specific information about attack patterns, including the attacker's methods, tools, techniques, attack processes, targets, and potential defense measures. CAPEC may also include details on the complexity of attack patterns, required conditions, and their potential impacts.

 By associating the data from CVE, CWE, and CAPEC through their relationships, the accuracy and depth of attack classification and defense analysis can be significantly enhanced. This association allows the model not only to identify individual vulnerabilities but also to understand their root causes and how they might be exploited by attackers, thereby revealing the intrinsic connections between vulnerabilities, weaknesses, and attack behaviors. This multi-dimensional information fusion enables the model to make more accurate predictions and classifications, ultimately improving the precision of attack identification. 

(3)** **GPCN File** ：**

The 'data' directory contains the 'cora11' dataset, which includes the constructed feature matrix and the relationship matrix. The 'cora11.content' file contains the feature matrix data, while the 'cora11.cites' file contains the relationship matrix.


**GPCNKB File：**

In the 'data8' directory, 'traindata.txt' serve as the training datasets. The remaining files in this directory are used as test datasets. For the test sets, we randomly replace either the head entity, the tail entity, or the relationship between them.



