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

1. The client has access to all the publicly available data that complies with ethical and legal regulations.
2. Bias detection can be improved using existing open-source AI fairness tools.
3. Developers require a UI/UX interface for categorization and validation.
4. The AI developer's primary focus is on improving training data quality rather than model tuning.
5. The client’s team has expertise in using cloud storage solutions.

### **Validation Plan**
1. Regular feedback sessions with the client to confirm requirement alignment.
2. Prototype demonstrations to validate user interactions.
3. Testing against real-world datasets to ensure bias detection accuracy.
4. Performance benchmarks to confirm system scalability and efficiency.
5. Review a sample of 500 scraped entries with the client to confirm accurate Q&A separation.
6. Demonstrate scraping from 3+ websites (e.g., Reddit, Wikipedia) during a client demo.
