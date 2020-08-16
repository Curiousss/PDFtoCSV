# PDFtoCSV

## Extract table from canopy_technical_test_input.pdf into newcsv.csv

### First approach
First I tried to use Poppler: https://poppler.freedesktop.org/. It gives an html file with the location of the tables and contents. 
My approach was to find a range of xmin, xmax, ymin, ymax values for each cell and extract values and convert to table. It was time consuming to get the right range to be able to generically extract values in each column and row.
I shall contiue this, since eventually I can build a package that can extract any kind of table from a PDF.

### Current approach:
The files uploaded here show this approach where I used the https://pdftables.com/ to extract table from a pdf file and convert to csv. It was pretty neat except for few mistakes. I used their webapp for the same. Next time I want to use their API so that the I can convert as many files as needed from the program itself instead of using the webapp.
Find that generated file here: [canopy_technical_test_output.csv](https://github.com/Curiousss/PDFtoCSV/blob/master/canopy_technical_test_input.csv)
The notebook uploaded here is the program for cleaning up these mistakes to get the expected table in csv format. The notebook reads the csv into a Pandas datafram which make the manipulation of the table very easy. 
### The resulting table, the final CSV can be found here [newcsv.csv](https://github.com/Curiousss/PDFtoCSV/blob/master/newcsv.csv)
For now the notebook shows the idea behind the cleanup process. I used the notebook to be able to explain the steps. I have also avoided the python comprehensions and coded the loops in multiple lines to be able to grasp the steps.

### Next steps...:
- I want make this as generic as posible so that it can be made into a python package to extract tables in pdf into csv.
- Implementing it as an object oriented approach to make it more modularized and extendable into more functionalities.
- Implement comprehensions to make the processing efficient.



