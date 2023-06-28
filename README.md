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
+ The ChatGPT cover letter generator will extract information about the employer, the job title, the requirements, the tasks, the contact person and the company address from the job posting. 
  ```
  {
    "employer": "OpenAI",
    "job title": "Research Scientist",
    "requirements": [
      "Track record of coming up with new ideas or improving 
      upon existing ideas in machine learning",
      "Ability to own and pursue a research agenda",
      "Excitement about OpenAI's approach to research",
      "Nice to have: Interested in and thoughtful about the 
      impacts of AI technology",
      "Nice to have: Past experience in creating high-
      performance implementations of deep learning algorithms"
    ],
    "tasks": [
      "Develop innovative machine learning techniques",
      "Advance the research agenda of the team",
      "Collaborate with peers across the organization"
    ],
    "contact person": "unknown",
    "address": "San Francisco, California, United States"
  }
  ```
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
```
John Doe
123 Main Street
Anytown, USA
+1 (555) 123-4567
john.doe@email.com

June 28, 2023

OpenAI
San Francisco, California, United States

Dear Hiring Manager,

I am writing to apply for the Research Scientist position at OpenAI. With a strong educational background in computer science and machine learning, along with relevant work experience and a passion for AI technology, I believe I possess the necessary qualifications and motivation to excel in this role.

In terms of requirements, I have a track record of coming up with new ideas and improving upon existing ideas in machine learning. My Master of Science in Machine Learning from ABC University, along with my work as a Machine Learning Engineer at ABC Tech Solutions, have provided me with hands-on experience in designing and implementing machine learning algorithms. I have also utilized various frameworks such as TensorFlow, PyTorch, and scikit-learn to develop and deploy scalable machine learning pipelines. Additionally, I possess strong programming skills in Python and R, and I am proficient in data manipulation and analysis using Pandas and NumPy.

Furthermore, I am excited about OpenAI's approach to research and its impact on the field of AI. As an active and highly satisfied user of ChatGPT, I have witnessed firsthand the capabilities and potential of OpenAI's technology. I am also thoughtful about the impacts of AI and its ethical considerations, making me an ideal candidate for the role.

In terms of tasks, I am confident in my ability to develop innovative machine learning techniques and advance the research agenda of the team. I have a collaborative mindset and have successfully collaborated with peers across organizations in the past. Additionally, my experience in creating high-performance implementations of deep learning algorithms aligns with the nice-to-have requirement of the position.

Regarding my education, I hold a Bachelor of Science in Computer Science from XYZ University and a Master of Science in Machine Learning from ABC University. My educational background, coupled with my practical experience, has equipped me with a strong foundation in both theoretical concepts and practical applications of machine learning.

In terms of salary expectations, I am seeking a range of $100,000 - $120,000 per year. My possible start date would be October 1, 2023.

Thank you for considering my application. I am excited about the opportunity to contribute to OpenAI's research efforts and advance the field of AI. I have attached my resume for your review. I look forward to the possibility of discussing my qualifications further.

Sincerely,

John Doe
```

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
