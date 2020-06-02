# HTML Report Generation

This code combines the individual xml files obtained from robot framework and combines it in the parent.xml file provided with only positive test cases. After that the combined parent.xml file is converted to HTML report through the xmltohtmlReport xsl file. The final input is HTML while which needs to be printed as pdf to obtain the PDF report.

# Description

Filename.py consist the main python code which takes input path and module name as input from the user then finds all the passed test cases through function passing and then adds it's to the parent.xml file through the fuction extends. After the combined xml file is generated it uses the xslt transformer to read the xsl file and convert the xml report to HTML.

XmltohtmlReport is written in xslt language to convert xml to html. It consist of table and image source gathered through the xpath search in the combine xml file generated.

Parent.xml file is a static xml file which consist the static header and footer of the combined xml file where the passed test results are added.

Logo.png consist of the logo which is to be copied to the input location for the header in report.

# Running the Code and Generating PDF Report

Steps:

1) Open command prompt navigate to library folder of uiautomation, run following command. 

python filename.py

2) Enter the name of module (eg Equipment Management)

3) Give the path of input folder containing individual xml files and screenshots . (Make sure they have only the .xml to be combined)

4) Run the command and you should get a message “Great Job! Your Report is Ready!!” in command line.

5) Navigate to the input path which you specified it must contain the HTML file with the same as the module name input you specified. (eg Equipment Management.html)

6) Open the html file and go to print and select save as pdf. (Make sure it is in portrait and uncheck header and footer from More settings)

You can also refer to : https://ambarkaar.atlassian.net/wiki/spaces/SQE/pages/886309230?src=jira

7) PDF report should be ready on the location that you saved the file.
