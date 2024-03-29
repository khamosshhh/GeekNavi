# GeekNavi :mortar_board:
Building a Simple Course Recommendation System for Online Courses

## About the Project
With the use of a data-driven approach, GeekNavi is a minimalist system designed to assist students in navigating through the courses on Coursera. Currently, GeekNavi only identifies courses that are most similar to and most different from a selected course, which is picked by the learner from a pool of courses relevant to the skills the learner is interested in.
  
*NOTE: This is a personal project that the author started because they needed an end-to-end data science project that could teach them how to deploy a web app using [Streamlit](https://www.streamlit.io/), create a dataset using web scraping, and learn the fundamentals of content-based recommendation systems. Although this program currently provides reliable recommendations, it is hardly "smart." However, you may pull this repo, work on it, make it "smarter" and thus, make relevant contributions!* :smile: 
 
## Dataset Used
For the purpose of building GeekNavi, data from Coursera was scraped using the requests and beautifulsoup4 libraries. The ```scraper.py``` file contains code for scraping data from [https://www.coursera.org/courses](https://www.coursera.org/courses) and generates [coursera-courses-overview.csv](https://github.com/khamosshhh/GeekNavi/blob/main/coursera-courses-overview.csv). The ```course_scraper.py``` file contains code to scrape details of each individual course and the output is [coursera-individual-courses.csv](https://github.com/khamosshhh/GeekNavi/blob/main/coursera-individual-courses.csv).  

Both these above datasets have been combined to give [coursera-courses.csv](https://github.com/khamosshhh/GeekNavi/blob/main/coursera-courses.csv). This file consists of 1000 instances and 14 features and has a size of 1.41 MB.

### Features in the Dataset
The following features have been extracted for the dataset created above:  
  
**course_url:** The URL to the course homepage  
**course_name:** The name of the course  
**learning_product:** The type of product that the instance is. It can be a course, professional certificate or a specialization. *(While all instances of the dataset are referred to as courses , this is not be confused with the learning_product of a particular instance)*  
**course_provided_by:** The organization/partner that is providing the course  
**course_rating:** Overall rating of the course  
**course_rated_by:** The number of students who have rated the course  
**enrolled_student_count:** The number of learners who have enrolled into this course  
**course_difficulty:** The difficulty level of the course. It can take values of beginner, intermeditae, advanced and mixed  
**skills:** The main skills that the course works at developing in a learner  
**description:** About the course  
**percentage_of_new_career_starts:** Percentage of learners who have had a new career start after completing this course  
**percentage_of_pay_increase_or_promotion:** Percentage of learners who have had a pay increment or received a promotion after completing this course  
**estimated_time_to_complete:** The estimated tome to complete the course  
**instructors:** The instructors taking the course  

## Usage
The instructions to run GeekNavi on your local system are as follows:

1. Create a virtual environment on your local system to install this project's dependencied and run it
2. Download or clone this repository into your virtual environment
3. Run the following command to install necessary libraries for GeekNavi to run
  ```
  pip install -r requirements.txt
  ```
4. Run the streamlit app with
  ```
  streamlit run recommender.py
  ```
5. The app should open at http://localhost:8501

<!-- ## Screenshots
![](https://github.com/ry05/GeekNavi/blob/master/img/GeekNavi-init.JPG)  
Fig.1. The GeekNavi Interface
![](https://github.com/ry05/GeekNavi/blob/master/img/GeekNavi-skill-filter.JPG)  
Fig.2. Applying the Skill Filter
![](https://github.com/ry05/GeekNavi/blob/master/img/GeekNavi-recommend.JPG)  
Fig.3. Recommendations Generated -->

## What can GeekNavi do?
In a nutshell GeekNavi can perform the following tasks:
* Select courses for you based on the skills you want to learn
* Recommend courses that are most similar and most different to the course you select

## References
If you liked the concept and implementation of GeekNavi, do check out the following resources that provided me with some much needed help while working on this:
* [The Streamlit Official Guide](https://www.streamlit.io/)
* [The Real Python Guide to using Beautiful Soup](https://realpython.com/beautiful-soup-web-scraper-python/)
* [An article about web scraping Coursera](https://medium.com/analytics-vidhya/web-scraping-and-coursera-8db6af45d83f)
* [An article on building a content-based movie recommender with NLP](https://towardsdatascience.com/how-to-build-from-scratch-a-content-based-movie-recommender-with-natural-language-processing-25ad400eb243)
