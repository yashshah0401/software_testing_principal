# Project Documentation

## AI Training Data Categorization

### Description
The AI training data must be categorized with separate sections for questions and answers. This ensures developers can work on self-affirmation tasks without confusion.

### Acceptance Criteria
- Questions are stored in a separate file/table from answers.
- Data format follows a predefined structure (e.g., JSON, CSV, SQL).
- There is a script available to organize unstructured data.

### Assumptions
- The data to be categorized is available and accessible.
- Developers have the necessary tools and permissions to access and modify the data.
- The predefined structure for data format is agreed upon and documented.

### Validation Plan
1. **Data Separation Check**: Verify that questions and answers are stored in separate files/tables.
2. **Format Compliance**: Ensure the data format adheres to the predefined structure (e.g., JSON, CSV, SQL).
3. **Script Functionality**: Test the script to confirm it correctly organizes unstructured data into the required format.

### Tasks
1. **Define Data Structure**:
   - Document the predefined structure for storing questions and answers.
   - Review and approve the structure with the team.

2. **Develop Separation Script**:
   - Write a script to separate questions and answers from unstructured data.
   - Test the script with sample data to ensure accuracy.

3. **Data Migration**:
   - Migrate existing data into the new structure.
   - Validate the migrated data to ensure it meets the acceptance criteria.

4. **Review and Validation**:
   - Conduct a peer review of the data separation and migration process.
   - Perform validation checks as outlined in the Validation Plan.

## Bias Detection in AI Training Data

### Description
To ensure a balanced AI model, we need a process to analyze and flag biased data.

### Acceptance Criteria
- Algorithm detects and reports biased data.
- Provides a log file or UI dashboard showing flagged issues.
- Allows manual review and correction of flagged data.

### Assumptions
- The dataset to be analyzed is accessible and representative of the training data.
- The Machine Learning Engineer has the necessary tools and permissions to implement and test the algorithm.
- There is a predefined definition of what constitutes biased data.

### Validation Plan
1. **Bias Detection Accuracy**: Test the algorithm with known biased and unbiased data to ensure it correctly identifies biased data.
2. **Logging and Reporting**: Verify that the log file or UI dashboard accurately displays flagged issues.
3. **Manual Review Process**: Ensure there is a clear process for manual review and correction of flagged data.

### Tasks
1. **Define Bias Criteria**:
   - Document the criteria for what constitutes biased data.
   - Review and approve the criteria with the team.

2. **Develop Detection Algorithm**:
   - Write and test the algorithm to detect biased data.
   - Validate the algorithm with sample datasets.

3. **Implement Logging/Reporting**:
   - Develop a log file or UI dashboard to report flagged issues.
   - Test the logging/reporting system to ensure accuracy and usability.

4. **Manual Review Process**:
   - Establish a process for manual review and correction of flagged data.
   - Train team members on the review process.

5. **Review and Validation**:
   - Conduct a peer review of the bias detection and reporting process.
   - Perform validation checks as outlined in the Validation Plan.
