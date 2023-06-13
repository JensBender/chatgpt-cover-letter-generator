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
+ Enter the URL of the job posting and your motivation to apply for the job in your_target_job.py. 
+ Enter your OpenAI API key, name, address, phone number, email, education, work experience, skills, salary expectations and possible start date in your_secrets.py.

### Create Cover Letter
+ Run cover_letter_generator.ipynb to create three cover letter suggestions.
+ Pick the best cover letter, fine-tune it to your needs and use it to apply for the job.
+ To create a cover letter in German language, run cover_letter_generator_de.ipynb.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- MARKDOWN LINKS -->
[ChatGPT-badge]: https://img.shields.io/badge/chatGPT-74aa9c?style=for-the-badge&logo=openai&logoColor=white
[ChatGPT-url]: https://openai.com/blog/chatgpt
[Python-badge]: https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54
[Python-url]: https://www.python.org/
[JupyterNotebook-badge]: https://img.shields.io/badge/jupyter-%23FA0F00.svg?style=for-the-badge&logo=jupyter&logoColor=white
[JupyterNotebook-url]: https://jupyter.org/
