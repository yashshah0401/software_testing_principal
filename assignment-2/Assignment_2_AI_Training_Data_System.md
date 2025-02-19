# Assignment #2: AI Training Data System

# Shah, Yash Ketanbhai
# 8990493
# Software Engineering Principles
# SENG8091 - Winter 2025 - Section 1

---

## Purpose
This document outlines the functional and system requirements for the AI developer's project, focusing on improving the categorization and balance of training data.

## Scenario
The client is an AI developer who is using the publicly available data for AI training through web scraping. After several discussions, the key challenges identified are:
- Developers require categorized training questions separated from answers for better self-affirmation.
- Developers need balanced training data to prevent biases in AI models.

## 1. Requirements
*What the system must do to meet the user needs.*

1. **Categorized Training Questions**
	- **Requirement:** The system shall allow the developers to store the questions and answers in the distinct, labeled of the datasets.
	- **Justification:** Separating the questions from the answers which will help to enables developers to review and validate them independently, supporting self-affirmation during the AI training model.	
	- **Example:** A question can be asked like "What is the reinforcement learning?" which is tagged under the "Machine Learning branch," while its answer is stored in a separate "Answers" repository/branch.

2. **Balanced Training Data**
	- **Requirement:** The system shall analyze the datasets for the biases and generate balance reports accordingly.
	- **Justification:** Balanced data improves the AI model fairness and it's accuracy by avoiding overrepresentation of any specific groups or the topics.
	- **Example:** A report showing that the 80% of the healthcare-related data focuses on "pediatrics," which is flagging it as a potential imbalance.

3.  **Data Verification and Modification**
	- **Requirement:** The system shall provide a user interface where developers can verify and modify training data categorization.
	- **Justification:** Ensures accuracy and flexibility in training data management.
	- **Example:** A review panel that allows manual adjustments to categorized data before finalization.

4. **Data Format Support**
	- **Requirement:** The system shall enable exporting categorized data in multiple formats (e.g., JSON, CSV).
	- **Justification:** Different AI training tools require varied input formats for compatibility.
	- **Example:** A feature that allows developers to download structured training data in user-specified formats.

---

### **System Requirements**
*Technical specifications to support functionality.*

1. **Web Scraping Integration**
	- **Requirement:** The system must scrape all the data from the multiple public websites and domain that we can use for the configurable tools.
	- **Justification:** Flexibility in the data collection which will ensures the diverse and relevant training datasets for the AI model.	
	- **Example:** Integration with the **Scrapy** to extract Q&A pairs from forums like Stack Overflow and other website.

2. **Bias Detection Module**
	- **Requirement:** The system shall compute bias metrics (e.g., demographic, topic distribution) within 10 minutes of data ingestion.
	- **Justification:** Rapid analysis that allows the developers to iterate quickly on all the dataset adjustments.
	- **Example:** A Python-based module with using **Pandas** and **NumPy** to calculate statistical distributions for the Bias module.

3. **API Integration**
	- **Requirement:** The system shall provide an API for integrating with other AI training tools.
	- **Justification:** API support enables seamless interoperability with external AI development platforms.
	- **Example:** A RESTful API that allows querying and retrieving categorized training data.

4. **Security and Access Control**
	- **Requirement:** The system shall provide access control mechanisms to ensure data security and integrity.
	- **Justification:** Prevents unauthorized modifications and data breaches.
	- **Example:** Role-based access control (RBAC) limiting editing privileges to authorized users.

## 2. Assumptions & Validation
### **Assumptions**

## 1. Assumptions

- **Categorized Training Questions**
	- Assumes that the developers will correctly label all the questions and answers for proper categorization.
	- Assumes that the stored questions and answers will be used for AI training models with minimal human intervention.
	- Assumes that the developers need a structured approach to review and validate categorized data.

- **Balanced Training Data**
	- Assumes that the system can be analyze datasets for bias with predefined metrics.
	- Assumes that the AI fairness and accuracy are impacted by imbalanced training data.
	- Assumes that the bias detection reports will guide dataset improvements.

- **Data Verification and Modification**
	- Assumes that the developers will need a user interface to manually adjust categorization.
	- Assumes that the dataset modification improves model accuracy.
	- Assumes that the real-time modifications will be reflected in the final dataset.

- **Data Format Support**
	- Assumes that the different AI models require multiple data formats (JSON, CSV, etc.).
	- Assumes the that system should be enable seamless export and conversion options.
	- Assumes that the developers require structured data formats for model compatibility.

- **Web Scraping Integration**
	- Assumes that the publicly available data can be legally scraped for training purposes.
	- Assumes that the developers require flexibility in configurable data sources.
	- Assumes that the third-party tools like **Scrapy** can facilitate data extraction.

- **Bias Detection Module**
	- Assumes that the bias computation must be completed within 10 minutes.
	- Assumes that the developers require real-time feedback on dataset distribution.
	- Assumes that the statistical libraries (Pandas, NumPy) will be effective for bias analysis.

- **API Integration**
	- Assumes that the other AI training tools will integrate with the provided API.
	- Assumes that the a RESTful API will be sufficient for querying categorized data.
	- Assumes that the seamless data retrieval is essential for interoperability.

- **Security and Access Control**
	- Assumes that the role-based access control (RBAC) will ensure data integrity.
	- Assumes that the different user roles require varying access permissions.
	- Assumes that the unauthorized modifications must be prevented.

## 2. Validation Plan

| Requirement | Validation Method |
1. | Categorized Training Questions | Review the labeled datasets for the consistency & correctness of the question.|
2. | Balanced Training Data | Generate and analyze the bias reports using AI models.|
3. | Data Verification and Modification | Test the UI functionality for the manual categorization updates.|
4. | Data Format Support | Export the datasets in JSON and CSV, test compatibility.|
5. | Web Scraping Integration | Scrape public data sources, validate dataset integrity.|
6. | Bias Detection Module | Run the statistical bias checks within time constraints.|
7. | API Integration | Test API endpoints for data retrieval and format accuracy.|
8. | Security and Access Control | Conduct the access control tests with the test cases for the authorized user roles.|
