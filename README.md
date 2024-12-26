# Resume Generator

#### Video Demo: <https://youtu.be/MZETIFwZfBM?si=0kKUiCs6A4fpT79X>

#### Description:

The **Resume Generator** is a Python-based command-line application designed to automate the process of creating personalized resumes. It prompts the user for their personal details, educational background, work experience, skills, projects, and certifications, and then generates a professional-looking resume in PDF format. The application is built using the `FPDF` library, which allows for the creation of highly customizable PDF documents.

The primary objective of this project is to help individuals, especially students and professionals, quickly create a neat and readable resume by simply inputting their details. The project was designed with simplicity and usability in mind, allowing users to generate a well-structured resume without the need for complex templates or design software.

This README will explain the project in detail, including its functionality, design choices, file structure, and how to run the application. It also outlines the testing methods used to ensure the application functions as intended.

### Features:
- **User Input**: The application asks the user for various details, such as their name, email, phone number, career objective, education, work experience, skills, projects, and certifications.
- **PDF Generation**: Once the user provides all the required details, the program generates a PDF document containing the user's resume. The resume is organized into clear sections, including Objective, Education, Work Experience, Skills, Projects, and Certifications.
- **Customizable Layout**: The resume features a professional layout with color-coded sections and neatly formatted text to ensure that the resume is visually appealing and easy to read.
- **Interactive Command-Line Interface**: The application uses the command-line interface (CLI) for easy interaction. Users can enter their details through prompts, and the program handles the rest.
- **Simple Setup**: The program is easy to set up and run. Users can clone the project, install the required dependencies, and generate their resume with minimal effort.

### Files and Functionality:
This project consists of several key files:

1. **project.py**: The main file of the application. This file contains the code responsible for:
   - Collecting user input for the resume.
   - Generating the PDF resume using the `FPDF` library.
   - Formatting the content (such as project descriptions and work experience).
   - Saving the resume as `resume.pdf` in the current directory.

   The user input is gathered through a series of prompts in the terminal, and the information is stored in a dictionary. This dictionary is then used to populate the PDF fields, ensuring that the generated resume is customized to the user's inputs.

2. **test_project.py**: This file contains unit tests written using the `pytest` framework. The tests ensure that the functions in the application work as expected. 
   - `test_format_project_description()`: This test checks that the project descriptions are formatted correctly.
   - `test_clean_text()`: This test ensures that the text cleaning function works as expected, removing unnecessary spaces.
   - `test_generate_resume()`: This test verifies that the resume is generated correctly and saved as a PDF file.

   These tests help ensure that each function behaves correctly, making the application more reliable and easier to maintain.

3. **requirements.txt**: This file lists the Python libraries required to run the project. It includes:
   - `fpdf`: The library used to generate the PDF document.
   - `pytest`: The testing framework used to verify the correctness of the application.

4. **README.md**: This file, which documents the project in detail. It includes an explanation of the project, the features, how to use the application, and how to run the tests.

### Design Choices:
The **Resume Generator** was designed with the following goals in mind:
- **Simplicity**: The application should be easy to use for anyone, even those with little technical experience. The CLI interface ensures that users can simply follow the prompts to provide their details.
- **Customization**: Although the layout is fixed, the information in the resume is completely customizable based on user input. The ability to include details such as work experience, skills, and certifications makes the resume versatile for various professions.
- **Modularity**: The code is structured in a modular way, with functions dedicated to specific tasks such as gathering user input, generating the PDF, and formatting the data. This makes the code easy to maintain and extend.
- **Error Handling**: The program doesn't handle all edge cases explicitly, but it assumes that the user provides valid input. Future versions of the program could improve error handling, for example, by validating email addresses or phone numbers.

### How the Application Works:
1. **Input Gathering**: When you run the program (`python project.py`), it will prompt you for the following information:
   - Full name
   - Email address
   - Phone number
   - Career objective
   - Education details (degree, institution, year)
   - Work experience (job titles, companies, durations, descriptions)
   - Skills (comma-separated list)
   - Projects (titles, descriptions, years)
   - Certifications (titles, years)

2. **Resume Generation**: After the input is collected, the `generate_resume()` function is called, which creates a PDF file using the `FPDF` library. The content is laid out in a structured format, with each section of the resume styled with different fonts and colors for readability.

3. **PDF Output**: The generated resume is saved as `resume.pdf` in the current working directory. This file can be opened with any PDF viewer and is ready to be shared or printed.

4. **Customize and Share**: You can open the `resume.pdf` file and customize it further if needed before sharing it with potential employers or networking contacts.

### Tests-test_project.py:

The tests will verify that key functions are working correctly, such as formatting project descriptions, cleaning input text, and generating the resume PDF.
Execute pytest test_project.py

### How to Use:

Execute python project.py
Input all the Details
resume.pdf will be saved in the same directory of the project.

### Future Improvements:
While this project meets the basic requirements of generating a resume, there are several potential improvements and features that could be added in the future:
- **Error Handling**: Implementing input validation (e.g., checking for valid email or phone number formats).
- **Web Interface**: Creating a web-based version of the Resume Generator, which could provide a more user-friendly experience with form inputs.
- **Template Customization**: Allowing users to select from multiple resume templates to give them more control over the layout and design.
- **Advanced Features**: Adding the ability to import data from LinkedIn or other professional profiles to automate the resume-building process further.

### Conclusion:
The Resume Generator is a simple yet powerful tool that automates the process of generating a personalized resume. It is an ideal solution for anyone looking to quickly create a professional-looking resume without needing to use complex word processing software or resume templates. By using Python and the `FPDF` library, this project offers a flexible, command-line-based approach to resume creation, and the modular design ensures that it can be easily expanded and customized in the future.

This project also serves as a great example of how to build real-world applications with Python and demonstrates how to apply programming concepts like file handling, input processing, and PDF generation in a practical context.

