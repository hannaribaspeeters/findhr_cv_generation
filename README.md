# Synthetic CV Generation Process for the Tourism Sector

## Overview

This document outlines the process followed to generate synthetic CVs across the **Tourism**, **Arts & Crafts**, and **Teaching** sectors. The objective was to create **100 synthetic CVs** for each sector, ensuring a **realistic distribution** based on gender, nationality, and age group. The generation of these CVs involved scraping data from relevant websites, processing the information, and applying a structured methodology to generate the content for the CVs. After generation, the CVs were manually reviewed for quality assurance.

---

## Process Overview

The key steps involved in generating synthetic CVs are as follows:

1. **Data Collection and Preparation**:
   - **Scraping Data**: Collect information on courses, institutions, and professions relevant to the sector.
   - **Data Structuring**: Organize the scraped data into tables, adding additional relevant columns such as study level, profession locations, required skills, and languages.
   - **CV Generation**: Use a custom code to generate the CVs based on predefined rules and randomization techniques.

2. **Distribution**:
   - Ensure that the distribution of the CVs across gender, nationality, and age group mirrors the distribution in the real-world dataset of donated CVs.

3. **Manual Review**:
   - After generating the CVs, a manual review process was applied to ensure that they appear realistic and credible. Only CVs that meet certain criteria for realism were retained.

---

## Detailed Process Breakdown

### Step 1: Data Collection

#### 1.1. **Generate Courses and Institutions Table**

To generate the **courses and institutions table**, the following steps were taken:

1. **Scraping Data**:  
   Scraped the **Educaweb website** for tourism-related studies in Spain from this URL:  
   [Educaweb Tourism Studies](https://www.educaweb.com/estudios/hosteleria-turismo-ocio/).

2. **Filtering and Structuring**:  
   - The scraped data contains information on various studies and the institutions offering them.
   - Sorted the studies into three categories based on the degree type:
     - **Level 0**: Professional Training (e.g., non-degree programs).
     - **Level 1**: Bachelor’s Degree.
     - **Level 2**: Master’s Degree.
   - This categorization was determined by checking for keywords in the course names such as "degree," "bachelor," "master," etc.

3. **Table Structure**:  
   The final table includes:
   - Course Title
   - Institution Name(s)
   - Level (0: Professional Training, 1: Bachelor’s Degree, 2: Master’s Degree)

#### 1.2. **Generate Professions Table**

To generate the **professions table**, the following steps were taken:

1. **Collect Data**:  
   Scraped the **Educaweb website** for information on professions related to tourism in Spain from this URL:  
   [Educaweb Tourism Professions](https://www.educaweb.com/profesiones/hosteleria-turismo-ocio/).

2. **LinkedIn Research**:  
   Gathered additional data by analyzing **LinkedIn profiles** of professionals in the tourism sector. This helped identify real-world roles and career progression.

3. **Data Structuring**:  
   - Merged the scraped data and LinkedIn insights into a final list of **professions**.
   - The list includes job titles commonly found in the tourism sector.

4. **Use of ChatGPT for Enrichment**:  
   Used **ChatGPT** to add three columns to the professions table:
   - **Places**: A list of locations where these roles are typically developed (e.g., hotels, travel agencies).
   - **Skills**: A list of skills required for each role (e.g., customer service, communication).
   - **Languages**: The number of languages typically needed for each role (e.g., Spanish, English, French).

5. **Table Structure**:  
   The final professions table includes:
   - Profession Name
   - Companies where the role can be developed
   - Required skills
   - Languages typically needed

### Step 2: CV Generation

#### 2.1. **Age Group and Demographic Distribution**

To create a representative set of **100 CVs per sector**, I ensured the following demographic distribution:

- **Gender**: 50% Female, 50% Male
- **Nationality**: 85% EU, 15% Non-EU
- **Age Group**:  
  - 25% Group 1 (Under 25)
  - 50% Group 2 (25-40 years)
  - 25% Group 3 (Over 40 years)

These distributions were based on the **real donated CV dataset** used as a reference.

#### 2.2. **Generating CVs**

For each demographic combination (e.g., female, EU, Group 1), I generated CVs using predefined code, which uses **randomization techniques** based on the available courses and professions data.

1. **Educational Background**:  
   - The educational background is created by randomly selecting a degree (professional training, bachelor’s, or master’s) from the courses table.
   - The degrees are assigned realistic start and end dates, with some randomization to make the timeline plausible.

2. **Professional Background**:  
   - For each CV, job roles are randomly assigned based on the profession table.
   - A realistic career progression is simulated, with entry-level roles followed by mid-level and senior roles (if applicable).
   - The roles come with associated skills, companies, and language requirements.

3. **Manual Review**:  
   After generating the synthetic CVs, I manually reviewed them to ensure their **realism**. The following criteria were considered:
   - CVs should have realistic job progression and educational timelines.
   - The content should be logically consistent with the age group, gender, and nationality distribution.

**Note**: This step introduces potential **bias**, as CVs were selected based on personal judgment.

### Step 3: Final Output

The final output consists of **100 CVs for each sector** (Tourism, Arts & Crafts, Teaching) with the following information:

- **Personal Information**: Gender, Nationality, Age Group (grouped by demographics)
- **Educational Background**: List of degrees, institutions, and durations.
- **Professional Background**: List of job roles, companies, start/end dates, and required skills.
- **Languages**: A list of languages spoken by the individual.

---

## Reproducibility Instructions

To reproduce this process, follow these steps:

1. **Scrape Data**:
   - Use web scraping techniques (e.g., BeautifulSoup, Scrapy) to gather course and institution data from **Educaweb** for tourism studies.
   - Similarly, scrape profession-related data from **Educaweb** for tourism jobs.

2. **Process Data**:
   - Categorize the courses by level (Professional Training, Bachelor’s, Master’s).
   - Merge the scraped profession data with insights from LinkedIn and ChatGPT for role descriptions, companies, skills, and languages.

3. **Generate CVs**:
   - Use the provided code to generate synthetic CVs based on age, gender, and nationality distribution.
   - Review the generated CVs to ensure they are realistic.

4. **Review and Filter**:
   - Manually review and filter the generated CVs to remove any unrealistic or biased results.

5. **Adjust Demographic Distribution**:
   - Ensure the distribution across age groups, gender, and nationality matches the real-world dataset.

---

## Conclusion

This README provides a comprehensive overview of the process followed to generate synthetic CVs for the tourism sector (and by extension, other sectors like arts & crafts and teaching). By following this process, it is possible to reproduce realistic and diverse CVs based on publicly available data and structured randomization techniques.

