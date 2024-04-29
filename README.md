# Minimal Resume Template for Quarto 💼

Minimal Resume is a Quarto template that uses a YAML header (YAML Ain’t Markup Language) to define the contents for a minimal resume. The template uses a minimal file structure, consisting of only two files:

- `resume.qmd`: the Quarto Markdown file configuring the contents of the resume. It uses YAML metadata to define variables such as first and last names, contact information, as well as populate resume sections such as education, skills, projects, and experience.

- `template.tex`: the LaTeX file used to structure the YAML content into the final PDF output. It defines custom LaTeX commands for structuring the resume layout, styling headers, defining resume items, etc.

## How to Use

1. **Edit Resume Information**: open the `resume.qmd` file in a text editor and edit the YAML metadata to include your personal information, education, skills, projects, and job experience.

2. **Define the Output File Options**: modify the last section of the YAML header to define options such as paper size, margins, line spacing, font size, etc.

3. **Generate PDF Output**: use Quarto Markdown to render the `resume.qmd` file into a PDF. You can use the following command in the terminal:

   ```
   quarto render resume.qmd
   ```

    This command will generate a PDF file named `resume.pdf` based on the content and formatting defined in the `resume.qmd` file.

## YAML Header
The YAML header in the `resume.qmd` file is used to define the contents and formatting of the resume. Each parameter in the YAML header specifies different elements of the resume, such as personal information, education, skills, projects, experience, formatting options, and output format. 

Below is a list of all parameters used in this template and how to use them. A few notes on usage:
- Make sure you format the YAML elements as described below.
- Use dashes as specified below, only to define resume items within YAML arrays (eductional degrees, job experiences, skills), not each element in the YAML.
### Resume Header
- **first-name** and **last-name**: splits your name and bolds you last name.
```{yaml}
first-name: John
last-name: Doe
```
- **homepage**: your personal website URL (use only your domain for a cleaner look).

```{yaml}
homepage: domain.com
```
- **email**: your email address.
```{yaml}
email: your@email.com
```
- **linkedin**: your LinkedIn header.
```{yaml}
linkedin: linkedin_header
```

### Sections
- **summary**: a brief professional summary describing your professional background, skills, and career goals.
```{yaml}
summary: Lorem ipsum dolor sit amet, officia excepteur ex fugiat reprehenderit enim labore culpa sint ad nisi Lorem pariatur mollit ex esse exercitation amet. Nisi anim cupidatat excepteur officia.
```
- **education**: a list of education milestones, each item consisting of the following elements:
    * degree: {degree} of {type} in {program}
    * institution: name of institution
    * location: city and country abbreviation
    * gpa: "{system}: {points}" (surrounded by quotes)
    * dates: starting date — end date
```{yaml}
education:
  - degree: Bachelor of Science in Computer Science
    institution: University of Fictional City
    location: Fictional City, FC
    gpa: "GPA: 3.78"
    dates: September 2015 — May 2019
  - degree: Master of Engineering in Natural Language Processing
    institution: Fictional Institute of Technology
    location: Fictional City, FC
    dates: Aug. 2013 — Dec. 2014
```
- **skills**: a list of skills by category, each item contains the following elements:
    * type: skill category (bolded)
    * skills: comma-separated list of skills within the category.
```{yaml}
skills:
  - type: Programming Languages
    skills: Python, R, TensorFlow, PyTorch
  - type: Technologies
    skills: NLTK, spaCy, Gensim, scikit-learn, AWS SageMaker
  - type: Languages
    skills: English, Spanish, Chinese, Arabic, Japanese, Korean, Hindi, Bengali
```
- projects: a list of projects, each containing the following elements:
    * project: title or name of the project.
    * skills: comma-separated list of skills used in the project.
    * dates: duration or timeline of the project.
    * description: a list of project descriptions, each containing the following elements:
        - keyword: a keyword to highlight the description (optional).
        - text: a description text.
```{yaml}
projects:
  - project: "NLP Research: Sentiment Analysis"
    skills: Python, NLTK, TensorFlow, PyTorch
    dates: March 2022 ‐ August 2022
    description:
      - keyword: Sentiment Analysis
        text: Conducted research on sentiment analysis techniques for social media data, achieving 85% accuracy on a test dataset.
      - text: Developed deep learning models for sentiment analysis using both TensorFlow and PyTorch frameworks.
```
- experience: a list of job experiences, each containing the following elements:
    * company: name of the company or organization.
    * position: job title or position held.
    * location: location of the company or organization.
    * dates: duration of employment.
    * description: a list of job descriptions, each containing the following elements:
        - keyword: keyword or label for the description (optional).
        - text: description text.
```{yaml}
experience:
  - company: Fictional Tech Solutions
    position: NLP Engineer
    location: Fictional City, FC
    dates: Oct 2019 - Present
    description:
      - keyword: Natural Language Processing
        text: Developed NLP algorithms for text classification and named entity recognition, contributing to a 30% improvement in document processing efficiency.
      - text: Collaborated with cross-functional teams to deploy NLP solutions in production environments, ensuring scalability and performance.

```
### Ouput Options
The last section of the YAML heading contains standard Quarto parameters to modify the output document, such as papersize, margins (geometry), mainfont, fontsize, and line spacing (linestrech).

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
