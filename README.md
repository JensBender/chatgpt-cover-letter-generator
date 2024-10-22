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
      <li><a href="#prerequisites">Prerequisites</a></li>
      <li><a href="#install-python-packages">Install Python Packages</a></li>
      <li><a href="#set-up-openai-api">Set Up OpenAI API</a></li>
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
Utilize AI to write your cover letter. 

How it works:
- Enter the URL of the job posting you want to apply for and information about yourself. 
- The ChatGPT cover letter generator will extract information about the employer, the job title, the requirements, the tasks, the contact person and the company address from the job posting. 
- Then, it will match the education, work experience, skills, and motivation that you provided to the tasks and requirements of the job posting. 
- Finally, it will add your salary expectations and possible start date and create three cover letter suggestions that you can fine-tune to apply for the job.

### 🛠️ Built With
- [![ChatGPT][ChatGPT-badge]][ChatGPT-url]
- [![Python][Python-badge]][Python-url]
- [![Jupyter Notebook][JupyterNotebook-badge]][JupyterNotebook-url]

<p align="right">(<a href="#readme-top">back to top</a>)</p>


<!-- USAGE -->
## 💻 Usage
### 🖊️ Enter Information
Enter the URL of the job posting and your motivation to apply for the job in `your_information.py`. 
```
job_description_url = "https://openai.com/careers/research-scientist"

motivation = """
Active and highly satisfied ChatGPT user.
Fascination for data and all things AI.
Use my machine learning skills to contribute to the advancement of AI technology.
"""
```

Enter your OpenAI API key, name, address, phone number, email, education, work experience, skills, salary expectations and possible start date in `your_information.py`.
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

<p align="right">(<a href="#readme-top">back to top</a>)</p>


### 📝 Create Cover Letter
Run `cover_letter_generator.ipynb`. This will extract the relevant information from the job description in json format.
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
    "Nice to have: Past experience in creating high-performance 
    implementations of deep learning algorithms"
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

Next, the `cover_letter_generator.ipynb` will create three cover letter suggestions. Pick the best cover letter, fine-tune it to your needs and use it to apply for the job.
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
$120,000 per year. My possible start date would be October 1, 2023.

Thank you for considering my application. I am excited about the 
opportunity to contribute to OpenAI's research efforts and advance the 
field of AI. I have attached my resume for your review. I look forward to 
the possibility of discussing my qualifications further.

Sincerely,

John Doe
```

To create a cover letter in German language, run `cover_letter_generator_de.ipynb`.

<p align="right">(<a href="#readme-top">back to top</a>)</p>


<!-- GETTING STARTED -->
## 🚀 Getting Started

Follow these steps to set up the ChatGPT Cover Letter Generator on your local machine.

### Prerequisites
Ensure you have the following in place before proceeding.
- **Python 3.10 or higher**: Installed on your local machine.
- **Python Packages**: These will be installed using `requirements.txt` in the next step.
  - **OpenAI**: To interact with OpenAI's chat completions API.
  - **Requests**: To make HTTP requests to get job postings from the web.
  - **BeautifulSoup**: To parse HTML content to extract job descriptions.
- **OpenAI Account**: To generate an API key for accessing the OpenAI API.

### Install Python Packages
Ensure you have **pip** installed. Then, install the required dependencies listed in `requirements.txt`:
```
pip install -r requirements.txt
```

### Set Up OpenAI API
- Log in to your OpenAI account or create one if you haven't already.
- Create a new project:
  - Navigate to your account **Dashboard** and click **Create project**.
  - Name your project `chatgpt-cover-letter-generator` (or choose another name).
- Create an API key:
  - In the **Dashboard**, navigate to **API keys**.
  - Name the key (e.g., chatgpt-cover-letter-generator) and and click **Create new secret key**.
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
- **Project Logo**: Designed using [LOGO.com](https://logo.com/).
- **OpenAI API**: The following short courses by Andrew Ng and Isa Fulford. 
  - [ChatGPT Prompt Engineering for Developers](https://www.deeplearning.ai/short-courses/chatgpt-prompt-engineering-for-developers/).
  - [Building Systems with the ChatGPT API](https://www.deeplearning.ai/short-courses/building-systems-with-chatgpt/).

<p align="right">(<a href="#readme-top">back to top</a>)</p>


<!-- MARKDOWN LINKS -->
[ChatGPT-badge]: https://img.shields.io/badge/chatGPT-74aa9c?style=for-the-badge&logo=openai&logoColor=white
[ChatGPT-url]: https://openai.com/blog/chatgpt
[Python-badge]: https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54
[Python-url]: https://www.python.org/
[JupyterNotebook-badge]: https://img.shields.io/badge/jupyter-%23FA0F00.svg?style=for-the-badge&logo=jupyter&logoColor=white
[JupyterNotebook-url]: https://jupyter.org/
