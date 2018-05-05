# 412-house-search

The 412 House Seach is an Pittsburgh based aggregator service aimed to create an enriched house search experience for incoming CMU students. Our service designed entirely in Python which makes it very nimble and fast, which means that you can now search for house of your choice without having to be overwhelmed by multiple rental websites and advertizements. You can now stop at 412-house-search.com as your one stop shop for all the rental solutions.


# Program Modules

Our service has been designed primarily using the Model-View-Controller(MVC) framework in Python enables us to keep our code clean and modular. This also makes our code extensible in the future which means addditional value add-ons can be built on top of our core service. Our code consists of the following modules based on the nature of the operation.

1. Data Collection Module : In this module it connects with two websites Apartments.com and Hotpads.com and scrapes its data from these sites. Then it uses its third source that contains the property feedback that was manually collected. These three datasets are subjected to a lot of cleaning and the final data set is kept in a file called processed.xlsx.

2. Display Module : This module contains code that will guide the user in interacting with this console based application. 

3. Rent Analysis Module: This module helps in processing the user's preferences and then recommending the properties to the user.


# Project Folder Description

1. src folder - Given below is a section that shows what files are kept and why are they important.
  
      i. apartments_urls.csv - This file contains all the URL links of Apartment.com along with the maximum and minimum rent for the properties that appear on the link. Without these files the program will not be able to source data from the main rental website and as a result, either this program will fail or it will try to read from the cached files, apartments_raw.xlsx.
      
     ii. hotpads_urls.csv - This file contains all the URL links of Apartment.com along with the maximum and minimum rent for the properties that appear on the link. Without these files the program will not be able to source data from the main rental website and as a result, either this program will fail or it will try to read from the cached files, hotpads_raw.xlsx.
     
    iii. final_data_workbook.xlsx - This file contains a compilation of all the source data raw and in cleaned format and also the datasets merged together and its cleaned version.
   
     iv. prop_review_raw.xlsx - This file contains all the properties and thier tennat feedback. This file is necessary for the program to run or lese it can cause the program to crash.
   
      v. processed.xlsx - This file is the final dataset from which the program will read and recommend property suggestions. When the websites have blocked access, this file is necessary in the project folder and can act as an alternate source, prevent for the program to crash.


2. code 

     i. Search.ipynb - the main code in Jupyter Python Notebook
    ii. requriements.txt-  Before running all the code, please install all the packages in the requirments.txt and only then continue to run the progran.
 

# Important steps before running the code

1. Ensure that all the src files are downloaded into the project code.

2. Ensure that are judicisous when connecting to online websites, repeated attempts might block you.

3. Ensure that all the pacakges mentioned in the requirements.txt file has been installed and there are not failtures while installing them.

4. The webistes have a per day usage limit, so after making 300 requests, the server will automatically block you. To overcome this hurdle, we cached all the online data into offline apartments_raw.xlsx files, when the website doesnt let you connect then the program automatically reads the data from the files that are kept in the src folder.
        
5. The Google Web API that is being used to get the distance and duration to CMU alos has a 100 requests per day limit. Rerunning this code multiple times can result in a failure.
        
6. All the files kept under the src folder is necessary to run the program





















