<!-- anchor tag for back-to-top links -->
<a name="readme-top"></a>

<!-- PROJECT LOGO -->
<div align="center">
  <a href="https://github.com/JensBender/chatgpt-cover-letter-generator">
    <img src="images/logo.png" width=80%>
  </a>
  <p>
    <br />
    Create your cover letter with ChatGPT.
    <br />
  </p>
</div> 

---

## Table of Contents
<ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#usage">Usage</a>
    </li>
    <ul>
        <li><a href="#enter-information">Enter Information</a></li>
        <li><a href="#create-cover-letter">Create Cover Letter</a></li>
    </ul>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
</ol>

<!-- ABOUT THE PROJECT -->
## About The Project
Utilize AI to write your cover letter. 

How it works:
+ Enter the URL of the job posting you want to apply for and information about yourself. 
+ The ChatGPT cover letter generator will extract information about the employer, the position, the tasks, the requirements, the contact person and the company address from the job posting. 
+ Then, it will match the education, work experience, skills, and motivation that you provided to the tasks and requirements of the job posting. 
+ Finally, it will add your salary expectations and possible start date and create three cover letter suggestions that you can fine-tune to apply for the job.

### Built With
* [![ChatGPT][ChatGPT-badge]][ChatGPT-url]
* [![Python][Python-badge]][Python-url]
* [![Jupyter Notebook][JupyterNotebook-badge]][JupyterNotebook-url]

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- USAGE -->
## Usage
### Enter Information
+ Enter the URL of the job posting and your motivation to apply for the job in `your_target_job.py`. 
    ```
    job_description_url = "https://openai.com/careers/research-scientist"
    
    motivation = """
    Active and highly satisfied ChatGPT user.
    Fascination for data and all things AI.
    Use my machine learning skills to contribute to the advancement of AI technology.
    """
    ```
+ Enter your OpenAI API key, name, address, phone number, email, education, work experience, skills, salary expectations and possible start date in `your_secrets.py`.
    ```
    # OpenAI API
    OPENAI_API_KEY = "Your_OPENAI_API_key_here"
    
    # Cover letter input
    name = "John Doe"
    address = "123 Main Street, Anytown, USA"
    phone = "+1 (555) 123-4567"
    email = "john.doe@email.com"

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

    salary_expectations = "$100,000 - $120,000 per year"
    possible_start_date = "2023-10-01"
    ```

### Create Cover Letter
+ Run `cover_letter_generator.ipynb` to create three cover letter suggestions.
+ Pick the best cover letter, fine-tune it to your needs and use it to apply for the job.
+ To create a cover letter in German language, run `cover_letter_generator_de.ipynb`.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- GETTING STARTED -->
## Getting Started

Follow these steps to get the program running on your local machine.

### Prerequisites

This is a list of things you need to use this program.
<ul>
  <li>Python packages</li>
  <ul>
    <li>Openai</li>
    <li>Requests</li>
    <li>Beautiful soup</li>
  </ul>
  <li>OpenAI account</li>
</ul>

### Installation

1. Install the following packages: Openai, Requests, and Beautiful soup.
2. Create an OpenAI account, create an API key and paste it in `your_secrets.py`.
    ```
    OPENAI_API_KEY = "Your_OPENAI_API_key_here"
    ```

<!-- MARKDOWN LINKS -->
[ChatGPT-badge]: https://img.shields.io/badge/chatGPT-74aa9c?style=for-the-badge&logo=openai&logoColor=white
[ChatGPT-url]: https://openai.com/blog/chatgpt
[Python-badge]: https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54
[Python-url]: https://www.python.org/
[JupyterNotebook-badge]: https://img.shields.io/badge/jupyter-%23FA0F00.svg?style=for-the-badge&logo=jupyter&logoColor=white
[JupyterNotebook-url]: https://jupyter.org/
