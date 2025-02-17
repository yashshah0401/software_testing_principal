# Assignment #2: AI Training Data System

---

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

---

### **System Requirements**
*Technical specifications to support functionality.*

1. **Web Scraping Integration**
	- **Requirement:** The system must scrape all the data from the multiple public websites and domain that we can use for the configurable tools.
	- **Justification:** Flexibility in the data collection which will ensures the diverse and relevant training datasets for the AI model.	
	- **Example:** Integration with the *Scrapy* to extract Q&A pairs from forums like Stack Overflow and other website.

2. **Bias Detection Module**
	- **Requirement:** The system shall compute bias metrics (e.g., demographic, topic distribution) within 10 minutes of data ingestion.
	- **Justification:** Rapid analysis that allows the developers to iterate quickly on all the dataset adjustments.
	- **Example:** A Python-based module with using Pandas and NumPy to calculate statistical distributions for the Bias module.
