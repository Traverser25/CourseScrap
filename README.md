# CourseScrap
A selenium based webscrapper for scrapping courses of different colleges 

# College Course Scraper

## Overview

This project is a web scraper designed to extract course details from colleges listed on the Collegedunia website. Due to the varying structures of course pages on different college websites, scraping capabilities are limited. Therefore, we focused on a website that provides a comprehensive list of colleges, **Collegedunia**, which covers approximately 80% of the colleges.

## Features

1. **Dynamic Page Handling**: 
   - Many college websites have different structures for their course pages, which can limit scraping capabilities. This script is designed to handle the dynamic nature of the pages on Collegedunia.

2. **Comprehensive Coverage**:
   - The script scrapes data from Collegedunia, which lists a large number of colleges. By focusing on this site, we aim to cover a significant portion of available colleges and their course details.

3. **Dynamic Content Handling**:
   - We use Selenium to handle dynamic content and interactions, such as clicking buttons and waiting for elements to load. This allows us to navigate through pages and extract the necessary information effectively.

4. **Performance**:
   - On average, scraping details for each college takes approximately 2 minutes. The script can be run for a list of colleges to gather comprehensive data.

## Advantages

1. **Wide Coverage**:
   - Collegedunia provides access to a vast number of colleges, making it a valuable resource for gathering educational data on a broad scale.

2. **Dynamic Interaction**:
   - Selenium handles dynamic content and user interactions, which allows the script to deal with modern, JavaScript-heavy web pages effectively.

3. **Customizable**:
   - The script can be customized to fit different requirements or to adapt to changes in the websiteâ€™s structure.

4. **Unique Entries**:
   - The script ensures that only unique courses are included in the output, avoiding duplicate entries.

## Limitations

1. **Website Dependency**:
   - The scraper is dependent on the structure of Collegeduniaâ€™s website. If the website layout changes, the script may require updates to handle the new structure.

2. **Dynamic Content Handling**:
   - While Selenium is effective for dynamic content, it may struggle with very complex or frequently changing pages, potentially leading to longer scraping times or missed data.

3. **Performance**:
   - Average scraping time is about 2 minutes per college. For a large list of colleges, this may result in long total execution times.

4. **Error Handling**:
   - The script includes basic error handling, but unexpected issues with the website or connectivity problems may require manual intervention.

## How It Works

1. **Scraping College Details**:
   - The script first retrieves the URL for each college's course details page from Collegedunia.

2. **Extracting Course Information**:
   - Using Selenium, it navigates through the course details page, handling dynamic elements and interactions to extract the list of courses available.

3. **Writing Results**:
   - The scraped data is written to a text file, with each college's name and course details formatted appropriately.

## Requirements

- **Python 3.x**
- **Selenium**: For interacting with web pages
- **ChromeDriver**: To control Chrome browser
- **BeautifulSoup** (optional): For parsing HTML (if needed for additional parsing)

## Setup

1. **Install Dependencies**:
   - Install the required Python packages using pip:
     ```bash
     pip install selenium beautifulsoup4
     ```

2. **Download ChromeDriver**:
   - Download the ChromeDriver executable that matches your version of Chrome from [ChromeDriver Download](https://sites.google.com/chromium.org/driver/).

3. **Place ChromeDriver**:
   - Ensure that the `chromedriver` executable is in your system's PATH or specify its location in the script.

## Usage

1. **Set Up College List**:
   - Define the list of colleges you want to scrape in the script.

2. **Run the Script**:
   - Execute the script to start scraping. The script will output results in text files named based on the college names.

   ```python
   college_name = "Example College"
   link = get_courses_link(college_name)
   if link:
       results = get_course(link)
       write_to_file(results, college_name)
   else:
       print("Could not retrieve courses link.")


3. **Check Output:
The results will be saved in a text file named according to the college name (e.g., Example_College_courses.txt).


