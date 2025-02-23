## Python: How to scrape data from SSP website.

For this project, Selenium was chosen for scraping information from SSP dynamic pages.

A brief description:

For full documentation visit [Github project](https://github.com/Igorps023/Web-Scraping-SSP).

#### Tools and technologies involved.

*    `Python`
*    `Selenium`
*    `VS Code`

Website data is available at [Secretaria de Seguranca Publica do Estado de Sao Paulo](https://www.ssp.sp.gov.br/estatistica/dados-mensais)


*All the scripts, logs, virtual enviroment variables and packages are separate by folder.*

#### Final Result - Script in execution - Dynamic extraction of data
[![Script](https://s9.gifyu.com/images/SF56c.gif "Script")](https://s9.gifyu.com/images/SF56c.gif "Script")

#### Main objective: 
- Developing a solution to extract data dynamically, without the requirement of a user to select fields.

Automation developed in Python for selecting each Year, Region, District and Police Department:


#### FAQ about the project
Q: For what reason did you choose **Selenium** instead of  **Beautiful Soup**?

A: The elements generated by the web page were developed using Java Script, a few elements cannot be processed properly using libraries such as Beatiful Soup, that is the main reason that it was chose to use Selenium (note: a valid alternative would be using Selenium only to load and interact with the dynamic content of the page, afterwards, collecting the data with Beautiful Soup).

#### Main challenges during the development:
- Creating a logic for selecting each filter in a dependent logic. 
Example below:

1. Script selects 1 region (Grande SP, por exemplo)
2. Selects 1 district (Diadema, por exemplo)
3. Selects 1 police department (DP01 Diadema)
4. Data is shown in a table

The logic for solving this problem:
- Creating a nested for loop logic which selects each possible option after selecting the previous filter.
- Finally the data is collected and saved locally in format .csv

On the example below, the table data is presented after choosing at least one item.
[![Lista de rolagem dependente](https://s9.gifyu.com/images/SF5uE.gif "Lista de rolagem dependente")]("Lista de rolagem dependente")
