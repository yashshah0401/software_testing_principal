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

---

# User Stories & Tasks

## 1. Categorized Training Questions
**User Story:** As a developer, I should be able to categorize training questions and answers separately so that I can validate them independently.

### Tasks:
- Develop a database schema to separate questions and answers.
- Implement tagging functionality for categorization.
- Build an interface to allow manual question validation.

### Solution:
- Use relational database structure with separate tables for questions and answers.
- Implement a tagging with metadata labels.
- Develop a UI for manual categorization and validation.

## 2. Balanced Training Data
**User Story:** As a data scientist, I should be able to generate balance reports to detect biases so that I can improve dataset fairness.

### Tasks:
- Implement statistical analysis for dataset distribution.
- Generate bias reports with visual indicators.
- Provide suggestions for balancing dataset.

### Solution:
- Use Pandas and NumPy for statistical analysis.
- Create dashboard visualizations for bias reporting.
- Implement automated rebalancing suggestions based on thresholds.

## 3. Data Verification and Modification
**User Story:** As a developer, I should be able to verify and modify training data so that I can ensure accuracy before model training.

### Tasks:
- Design a UI for developers to review data categorization.
- Implement real-time modification options.
- Enable version control for data changes.

### Solution:
- Create a React-based UI for reviewing categorized data.
- Use database transactions to store modifications.
- Implement Git-based version tracking for historical changes.

## 4. Data Format Support
**User Story:** As a machine learning engineer, I should be able to export categorized data in multiple formats so that I can integrate it with AI models.

### Tasks:
- Develop export functions for JSON and CSV.
- Provide UI options to choose export format.
- Validate exported files for format accuracy.

### Solution:
- Use Python’s Pandas library to generate structured exports.
- Provide dropdown selection for format choice in UI.
- Implement automated validation scripts to check file integrity.

## 5. Web Scraping Integration
**User Story:** As a researcher, I should be able to scrape public domain data so that I can gather diverse training examples.

### Tasks:
- Configure Scrapy to extract relevant Q&A pairs.
- Implement pipeline for processing scraped data.
- Ensure scraped data adheres to categorization standards.

### Solution:
- Use Scrapy spiders to collect Q&A pairs.
- Process data with NLP filtering to remove irrelevant content.
- Store cleaned data in pre-defined categories.

## 6. Bias Detection Module
**User Story:** As an AI analyst, I should be able to detect biases in my training data so that I can adjust the dataset accordingly.

### Tasks:
- Develop bias detection algorithms.
- Automate report generation within time constraints.
- Provide visual indicators for bias distribution.

### Solution:
- Use Pandas and NumPy for bias computation.
- Automate report generation with scheduled batch processing.
- Implement data visualizations in Matplotlib.

## 7. API Integration
**User Story:** As a developer, I should be able to access categorized training data via API so that I can integrate it with my AI models.

### Tasks:
- Develop RESTful API endpoints.
- Implement authentication for API access.
- Test API response times and data accuracy.

### Solution:
- Use Flask/Django REST framework to develop API endpoints.
- Implement OAuth2 for secure access.
- Optimize queries for fast API responses.

## 8. Security and Access Control
**User Story:** As a security administrator, I should be able to control access to training data so that unauthorized modifications are prevented.

### Tasks:
- Implement role-based access control (RBAC).
- Develop logging for access tracking.
- Encrypt sensitive training data.

### Solution:
- Use JWT-based authentication for role enforcement.
- Implement logging with ELK stack (Elasticsearch, Logstash, Kibana).
- Encrypt stored data using AES-256.


# References

1. Bishop, C. M. (2006). Pattern Recognition and Machine Learning. Springer.
   - [https://www.microsoft.com/en-us/research/publication/pattern-recognition-machine-learning/](https://www.microsoft.com/en-us/research/publication/pattern-recognition-machine-learning/)

2. Russell, S. J., & Norvig, P. (2021). Artificial Intelligence: A Modern Approach (4th ed.). Pearson.
   - [https://lib.ysu.am/disciplines_bk/efdd4d1d4c2087fe1cbe03d9ced67f34.pdf](https://lib.ysu.am/disciplines_bk/efdd4d1d4c2087fe1cbe03d9ced67f34.pdf)
