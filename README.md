<!-- anchor tag for back-to-top links -->
<a name="readme-top"></a>

<!-- HEADER IMAGE  -->
<img src="images/header_image.png">

<!-- SHORT SUMMARY  -->
AI-powered assistant that extracts key information from job postings to generate and refine customized cover letters that align personal qualifications with job requirements, leveraging web scraping and the OpenAI API. 

---

## 📋 Table of Contents
<ol>
  <li>
    <a href="#-about-the-project">About The Project</a>
    <ul>
      <li><a href="#️-built-with">Built With</a></li>
    </ul>
  </li>
  <li>
    <a href="#-usage">Usage</a>
    <ul>
      <li><a href="#️-enter-information">Enter Information</a></li>
      <li><a href="#-create-cover-letter">Create Cover Letter</a></li>
    </ul>
  </li>
  <li>
    <a href="#-getting-started">Getting Started</a>
    <ul>
      <li><a href="#️-prerequisites">Prerequisites</a></li>
      <li><a href="#-install-python-packages">Install Python Packages</a></li>
      <li><a href="#-set-up-openai-api">Set Up OpenAI API</a></li>
    </ul>
  </li>
  <li>
    <a href="#️-license">License</a>
  </li>
  <li>
    <a href="#-credits">Credits</a>
  </li>
</ol>


<!-- ABOUT THE PROJECT -->
## 💡 About The Project
This AI-powered tool streamlines the cover letter writing process, transforming job postings into compelling, personalized applications. Simply provide a job posting URL and your personal background information to generate tailored cover letters.

Project Highlights:
- **Web Scraping**: Retrieves the job description text directly from the job posting URL using `Requests` and `BeautifulSoup`, with automatic language detection using `langdetect`.
- **Intelligent Information Extraction**: Analyzes job descriptions to identify and extract crucial information, including the job requirements, tasks, job title, and employer details using `OpenAI's chat completions API` with `structured outputs`. Leverages `Pydantic` to validate the JSON output.
- **Automated Cover Letter Generation**: Creates three unique cover letter suggestions by matching personal qualifications with job requirements using `chat completions API`.
- **Refinement and Consolidation**: Reviews and refines each cover letter, then consolidates them into a final, optimized cover letter, providing you with ready-to-edit drafts.
- **Multilingual and Personalization Support**: Provides cover letters in both English and German and allows customization for personal background, motivation, salary expectations, and start date.

Streamline your job application process and increase your chances of landing interviews with professionally crafted cover letters that effectively showcase your qualifications.

### 🛠️ Built With
- [![ChatGPT][ChatGPT-badge]][ChatGPT-url]
- [![Python][Python-badge]][Python-url]
- [![Requests][Requests-badge]][Requests-url]
- [![Beautiful Soup][BeautifulSoup-badge]][BeautifulSoup-url]
- [![Jupyter Notebook][JupyterNotebook-badge]][JupyterNotebook-url]

<p align="right">(<a href="#readme-top">back to top</a>)</p>


<!-- USAGE -->
## 💻 Usage
### 🖊️ Enter Information
To get started, input your API key, job posting URL, professional background, personal information, and motivation in `your_information.py`. 

```
# OpenAI API key
OPENAI_API_KEY = "Your_OPENAI_API_key_here"

# Job posting URL
job_posting_url = "https://openai.com/careers/research-scientist"

# Professional background
education = """
Bachelor of Science in Computer Science, XYZ University, Anytown, USA (2015-2019).
Master of Science in Machine Learning, ABC University, Somewhere City, USA (2020-2022)                                                  
"""

work_experience = """
Machine Learning Engineer, ABC Tech Solutions, Somewhere City, USA (2022-Present)
- Designed and implemented machine learning algorithms to improve product recommendations.
- Developed and deployed scalable machine learning pipelines using cloud-based platforms.
- Conducted model evaluation and performance tuning to optimize accuracy and efficiency. 
"""

skills = """
Programming Languages: Python, R
Machine Learning Frameworks: TensorFlow, PyTorch, scikit-learn
Data Manipulation and Analysis: Pandas, NumPy
Big Data Processing: Apache Spark
Data Visualization: Matplotlib, Seaborn
Version Control: Git
Cloud Platforms: AWS, Google Cloud Platform
"""

# Personal information
name = "John Doe"
address = "123 Main Street, Anytown, USA"
phone = "+1 (555) 123-4567"
email = "john.doe@email.com"
salary_expectations = "$100,000 - $120,000 per year"
possible_start_date = "2024-10-01"

# Motivation for the job
motivation = """
Active and highly satisfied ChatGPT user.
Fascination for data and all things AI.
Use my machine learning skills to contribute to the advancement of AI technology.
"""
```

<p align="right">(<a href="#readme-top">back to top</a>)</p>


### 📝 Create Cover Letter
Run `cover_letter_generator.ipynb` to automate each stage of creating a personalized cover letter:

1. **Web Scraping**: Extracts job description text directly from the job posting URL using `Requests` and `BeautifulSoup`. Automatically detects the language of the job description using `langdetect`.
2. **Information Extraction**: Uses `OpenAI's chat completions API (beta)` with `structured outputs` to extract the relevant information from the job description in JSON format. Leverages `Pydantic` to validate the JSON format against a defined schema.
    ```
    {
      "employer": "OpenAI",
      "job_title": "Research Scientist",
      "requirements": [
        "Track record of coming up with new ideas or improving 
        upon existing ideas in machine learning",
        "Ability to own and pursue a research agenda",
        "Excitement about OpenAI's approach to research",
        "Nice to have: Interested in and thoughtful about the 
        impacts of AI technology",
        "Nice to have: Past experience in creating high-performance 
        implementations of deep learning algorithms"
      ],
      "tasks": [
        "Develop innovative machine learning techniques",
        "Advance the research agenda of the team",
        "Collaborate with peers across the organization"
      ],
      "contact_person": "unknown",
      "address": "San Francisco, California, United States"
    }
    ```

3. **Cover Letter Generation**: Produces three unique cover letter suggestions by aligning your education, work experience, skills, and motivation to the tasks and requirements outlined in the job description using `chat completions API` and language-specific prompts in both English and German. 
4. **Cover Letter Refinement**: Reviews and refines each cover letter leveraging `chat completions API` with specific refinement prompts. 
5. **Cover Letter Consolidation**: Combines the best parts of each refined cover letter into a single, cohesive cover letter using `chat completions API` with dedicated consolidation prompts. 
6. **Save Cover Letters as Text File**: Exports the consolidated cover letter and the three refined cover letters to a `.txt` file for easy access and final editing.

**Example Cover Letter**:
```
John Doe
123 Main Street
Anytown, USA
+1 (555) 123-4567
john.doe@email.com

June 28, 2024

OpenAI
San Francisco, California, United States

Dear Hiring Manager,

I am writing to apply for the Research Scientist position at OpenAI. 
With a strong educational background in computer science and machine 
learning, along with relevant work experience and a passion for AI 
technology, I believe I possess the necessary qualifications and 
motivation to excel in this role.

In terms of requirements, I have a track record of coming up with new 
ideas and improving upon existing ideas in machine learning. My Master of 
Science in Machine Learning from ABC University, along with my work as a 
Machine Learning Engineer at ABC Tech Solutions, have provided me with 
hands-on experience in designing and implementing machine learning 
algorithms. I have also utilized various frameworks such as TensorFlow, 
PyTorch, and scikit-learn to develop and deploy scalable machine learning 
pipelines. Additionally, I possess strong programming skills in Python 
and R, and I am proficient in data manipulation and analysis using Pandas 
and NumPy.

Furthermore, I am excited about OpenAI's approach to research and its 
impact on the field of AI. As an active and highly satisfied user of 
ChatGPT, I have witnessed firsthand the capabilities and potential of 
OpenAI's technology. I am also thoughtful about the impacts of AI and its 
ethical considerations, making me an ideal candidate for the role.

In terms of tasks, I am confident in my ability to develop innovative 
machine learning techniques and advance the research agenda of the team. 
I have a collaborative mindset and have successfully collaborated with 
peers across organizations in the past. Additionally, my experience in 
creating high-performance implementations of deep learning algorithms 
aligns with the nice-to-have requirement of the position.

Regarding my education, I hold a Bachelor of Science in Computer Science 
from XYZ University and a Master of Science in Machine Learning from ABC 
University. My educational background, coupled with my practical 
experience, has equipped me with a strong foundation in both theoretical 
concepts and practical applications of machine learning.

In terms of salary expectations, I am seeking a range of $100,000 - 
$120,000 per year. My possible start date would be October 1, 2024.

Thank you for considering my application. I am excited about the 
opportunity to contribute to OpenAI's research efforts and advance the 
field of AI. I have attached my resume for your review. I look forward to 
the possibility of discussing my qualifications further.

Sincerely,

John Doe
```

Review the cover letter drafts, select the version that best fits your style, make any necessary adjustments, and submit your personalized cover letter.

<p align="right">(<a href="#readme-top">back to top</a>)</p>


<!-- GETTING STARTED -->
## 🚀 Getting Started

Follow these steps to set up the ChatGPT Cover Letter Generator on your local machine.

### ✔️ Prerequisites
Ensure you have the following in place before proceeding.
- **Python 3.10 or higher**: Installed on your local machine.
- **Python Packages**: These will be installed using `requirements.txt` in the next step.
  - **OpenAI**: To interact with OpenAI's chat completions API.
  - **Requests**: To make HTTP requests to get job postings from the web.
  - **BeautifulSoup**: To parse HTML content to extract job descriptions.
  - **langdetect**: To automatically detect the language of job descriptions.
  - **Pydantic**: To validate the job information JSON output.
- **OpenAI Account**: To generate an API key for accessing the OpenAI API.

### 📦 Install Python Packages
Ensure you have **pip** installed. Then, install the required dependencies listed in `requirements.txt`:
```
pip install -r requirements.txt
```

### 🔑 Set Up OpenAI API
- Log in to your OpenAI account or create one if you haven't already.
- Create a new project:
  - Navigate to your account **Dashboard** and click **Create project**.
  - Name your project (e.g., chatgpt-cover-letter-generator).
- Create an API key:
  - In the **Dashboard**, navigate to **API keys**.
  - Name the key (e.g., chatgpt-cover-letter-generator) and click **Create new secret key**.
  - Under **Permissions**, select **Restricted** and allow only **Write** permissions for **Model capabilities** for better security.
- Save your API key in `your_information.py`:
  ```
  OPENAI_API_KEY = "Your_OPENAI_API_key_here"
  ```

<p align="right">(<a href="#readme-top">back to top</a>)</p>


<!-- LICENSE -->
## ©️ License
This project is licensed under the [MIT License](LICENSE).

<p align="right">(<a href="#readme-top">back to top</a>)</p>


<!-- CREDITS -->
## 👏 Credits
This project was made possible with the help of the following resources and tutorials:
- **Project Logo**: Created using [LOGO.com](https://logo.com/).
- **OpenAI API**: Short courses by Andrew Ng and Isa Fulford on DeepLearning.AI. 
  - [ChatGPT Prompt Engineering for Developers](https://www.deeplearning.ai/short-courses/chatgpt-prompt-engineering-for-developers/).
  - [Building Systems with the ChatGPT API](https://www.deeplearning.ai/short-courses/building-systems-with-chatgpt/).

<p align="right">(<a href="#readme-top">back to top</a>)</p>


<!-- MARKDOWN LINKS -->
[ChatGPT-badge]: https://img.shields.io/badge/chatGPT-74aa9c?style=for-the-badge&logo=openai&logoColor=white
[ChatGPT-url]: https://chatgpt.com/
[Python-badge]: https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54
[Python-url]: https://www.python.org/
[Requests-badge]: https://img.shields.io/badge/Requests-black?style=for-the-badge
[Requests-url]: https://requests.readthedocs.io/
[BeautifulSoup-badge]: https://img.shields.io/badge/Beautiful%20Soup-4B8BBE?style=for-the-badge
[BeautifulSoup-url]: https://www.crummy.com/software/BeautifulSoup/
[JupyterNotebook-badge]: https://img.shields.io/badge/Jupyter-F37626.svg?style=for-the-badge&logo=Jupyter&logoColor=white
[JupyterNotebook-url]: https://jupyter.org/
