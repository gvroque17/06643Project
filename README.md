%%writefile 06643Project/README.md

## 06-643-Project

#### Description:
This project lists the citations for a given paper OpenAlex ID (OAID). First it groups the references by first author and then lists them in descending order from the most cited paper to the least cited paper. This can help the user highlight relevant authors and/or fundamental papers for the subject matter of the inputted paper.

#### Instructions: 
Location of GITHUB repository: [https://github.com/gvroque17/06643Project.git](https://github.com/gvroque17/06643Project.git)

1. Clone the GitHUB repository in desired directory: `git clone https://github.com/gvroque17/06643Project.git` 

2. Pip install package in desired directory: 
`cd <location of cloned repo> && pip install .`

3. Import our package: 
`import RefWorkSortPkg`

4. Once the package is installed, run using following command: `<variableName> = RefWorkSortPkg.referenced_work_sort('\<insert OAID for paper of interest>\')` 


![resPic.jpeg](attachment:aeeffd33-328e-4d3c-9942-b1a1ef23a23d.jpeg)


**Note: Running the command without assigning it to a variable name will output 2 versions of the results as seen in the below image. Both results contain the same information. The first portion is formatted in a nice to view format as a result of the print() statement within our function. The second portion is the result of our function return. Assigning the output to a variable simply suppresses the output of the returned values of the function. Suggest `<variableName> == _`**

#### Dependencies:
Environment: 
* Python 3.9.x or later

Python Libraries: 
*  requests
*  pytest
*  time
*  setuptools
*  sys


#### Planned improvements:

*  Expand code to be able to find most cited papers grouped by authors when searching for keywords in a search instead of just one paper.
*  Figure out how to test the retrieval of the information sans the cited by count so that if cited by count changes, it does not interfere with test validity for ref_work_test.py
