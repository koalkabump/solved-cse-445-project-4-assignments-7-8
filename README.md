Download Link: https://assignmentchef.com/product/solved-cse-445-project-4-assignments-7-8
<br>
<h1>Introduction</h1>

The aim of this assignment is to make sure that you understand and are familiar with the concepts covered in the lectures, including XML elements, attributes, statements, XML schema, XML validation, XML transformation (XSL), and their classes in .Net FCL. By the end of the assignment, you should have applied these concepts and techniques in creating an XML file, its schema, its style sheet, and have written Web services and an SOA application to process these files.

This is an individual assignment. Each student must complete and submit independent work. No cooperation is allowed. You can use WebStrar to host your files and services. You can also use your ASU personal Web site space to host your XML, XSD, and XSL files.

<h1>Section I Practice Exercises (No submission required)</h1>

No submission is required for this part of exercises. However, doing these exercises can help you better understand the concepts and thus help you in quizzes or exams.

<ol>

 <li>Reading: Textbook Chapter 4.</li>

 <li>Answer the multiple choice questions 1.1 through 1.16 of the Text Section 4.8. Study the material covered in these questions can help you to prepare for the class exercises, quizzes, and the exam.</li>

 <li>Study for the questions 2 through 8 in text Section 4.8. Make sure that you understand these questions and can briefly answer these questions. Studying the material covered in these questions can help you to prepare for the exam and understand the homework assignment.</li>

 <li>In this assignment, you can use WebStrar to host your XML files and services. You can also use your ASU personal Web hosting site to host the files. If you have not activated your file service and personal Web hosting site at ASU, you can activate them at: <a href="http://www.asu.edu/selfsub">asu.edu/selfsub</a><a href="http://www.asu.edu/selfsub">.</a> Choose “Subscribe to additional computing access/services”, and then chose “Personal Webpage Hosting”. To access your personal Web site, you need to have SSH or PuTTY software to connect to general.asu.edu. You can also search for “Uploading Your Personal Web page” within the ASU search page to find the steps for uploading your files. Notice that the ASU Personal Web site space hosts files only. You can use it to host your .xml, .xsd, and .xsl files. It does not host programs such as Web services and Web applications. IIS are not installed. In order for your files to be accessible from the Web, you must put the files into the WWW directory, it its sub-directories.</li>

</ol>

5          You can access the sample XML and XSD files at: http://neptune.fulton.ad.asu.edu/WSRepository/xml/Courses.xml http://neptune.fulton.ad.asu.edu/WSRepository/xml/Courses.xsd




<h1>Section II Project Questions (Submission Required)</h1>

Assignment 7

<ol>

 <li>In this question, you will create a directory of persons, which can be represented as an XML tree. The diagram below shows the required structure of the directory of persons in XML tree notation that you will create in this assignment. All the “Person” elements have the same structure. Notice that different shapes of boxes have different meanings. They represent elements, attributes, and text contents/values, respectively. The structure of elements and attributes given in the diagram below are required to implement, while the given text contents/values in the diagram are examples. The Category element can take three content values: Family, Friend, or Work. You can define it as of enumeration type or simply as of string type. The solid arrows show parent-child element relations, and the dotted arrows show the element-content relations. Notice that the optional attribute “Provider” means that the XML instance can have the attribute or not have the attribute, without causing a verification error against its schema. However, it is still required to define the optional attribute in the XML Scheme file.

  <ul>

   <li>Write the xsd file that defines the XML schema allowing the structure shown in the diagram above. You can use any tool to create/edit the file. [10 points]</li>

   <li>Create an XML file xml as an instance of your schema file. Define at least five (5) persons in each category: (1) Family, (2) Friend, and (3) Work. Enter the person information into the Persons.xml file. You can use any tool to edit the file. If an element has a Required Attribute, you must provide the attribute for each of the elements. If an element has an Implied (Optional) Attribute, you will provide this attribute for some elements, but not for all elements. [10 points]</li>

   <li>Write a xsl file for defining the HTML style for displaying the persons stored in Persons.xml in a formatted table. You can choose your own format to present the data in a table, which must include all elements, attributes, and their values. You can use any tool to edit the XSL file. [10 points]</li>

   <li>As a test page (TryIt page), create an ASPX Web site application (not a Web service) which takes the URL of an XML file as input (via textbox) and displays the element (tag) names, text contents, attribute names, and attribute values in the GUI page. You can define the order of data to be displayed.</li>

  </ul></li>

</ol>

Make your Persons.xml as the default input.                [20 points]

Assignment 8

<ol start="2">

 <li>Develop a Web service (.svc) with <strong>two</strong> of the Web operations listed below. The node mentioned in the sub questions below includes every component (element, content, and attribute) shown in the XML tree above. You need to choose two operations to implement. If you implement more than two operations, we will grade the first two operations only. If you have implemented and submitted a service listed below in your assignment 3 as an elective service, you cannot choose the same service here. However, in your Project 5, you can use the services developed in this project in addition to your elective services for the application that you have outlined in project 3. A complete application will be implemented in Project 5.

  <ul>

   <li>Web operation “verification” takes the URL of an XML (.xml) file and the URL of the corresponding XMLS (.xsd) file as inputs and validates the XML file against the corresponding XMLS (XSD) file. The Web method returns “No Error” or an error message showing the available information at the error point. You must use files that you created in the previous questions, with and without fault injection, as the test cases. However, your service operation should work for other test cases too.</li>

  </ul></li>

</ol>

[10 points]

<ul>

 <li>Web operation “transformation” takes the URL of an XML (.xml) file and the URL of the XSL file as inputs and generates the HTML file based on the XML and XSL files. The generated HTML file should be returned as the return value of the operation. In the TryIt GUI (question 3), you can store the returned file in a text file or in an .htm (or .html) file. You can also display the file in the GUI of your Web application. You must use files that you create in the previous questions as the test cases.</li>

</ul>

However, your service operation should work for other test cases too.                                                          [10 points]

<ul>

 <li>Web operation “search” takes the URL of an XML (.xml) file and a key (name) as input. It returns the node’s content information related to the key: Name, Password, Phone and Provider, and Category. Your program must read the attribute Encryption of the Password element to determine if decryption is necessary. [10 points]</li>

 <li>Web operation “XPathSearch” takes the URL of an XML (.xml) file and a path expression as input. It returns the path expression value of the given path. It could be a list of nodes, the content value, etc., depending on the path given. [10 points]</li>

 <li>Web operation “addPerson” modifies the XML by adding a new person into the XML file. You can use multiple parameters or one parameter that contains all the information required for adding a new person into the tree. Your program must determine if encryption is necessary. [10 points]</li>

</ul>

<em>Notice that, for all the questions above, do not place the XSD file as a namespace in your XML file. </em>

<em>It may cause an exception to some library classes. The absence of the XSD namespace will not cause </em>




<em>a problem with the schema validation, as your validation method will take two parameters as input: </em>

<em>the XML file and the schema file. </em>

<ol start="3">

 <li>Create a Web application, and add the project into the same “solution” that hosts your web service. The Web application must provide a GUI (TryIt Page), which allows entering the required inputs, such as URLs and keyword, path, or contents, based on the questions that you select. The GUI must have the buttons required to invoke the service operations, depending on the methods that you implement in the previous question, for example,

  <ul>

   <li>The button validates the XML file against the schema file.</li>

   <li>The button generates the HTML file.</li>

   <li>The button searches by keyword or by path in the XML file.</li>

   <li>The button adds a new person.</li>

  </ul></li>

</ol>

The Web application must use the Web services created in question 2 to perform the required processing, and display the return messages in the GUI. You can use a textbox, a list box, or a label to display the html file, or display it in a separate page. This assignment will be implemented on localhost (IIS Express) or WebStrar.

[20 points]

<ol start="4">

 <li>Testing: Based on your selection of the sub questions in question 2, provide test inputs and test results. For example, if you chose questions 2.1 and 2.2, you can place the three files: xml, Persons.xsd, and Persons.xsl, into a Web site and use them to test your program on your .Net development server. Inject an error in your XML file and make sure the validation service can detect the error. For this question, you must submit the test results (inputs and outputs) in screenshots. For example       [10 points]

  <ul>

   <li>Screenshots of the GUI, including the output of the XML validation displayed in the GUI, with no error and with an error message;</li>

   <li>A screenshot of the GUI, including the input and output for keyword search;</li>

   <li>The htm file (or Persons.html) file generated.</li>

  </ul></li>

</ol>

These three files above are not programs and can be deployed to any web location, such as the personal web space provided by ASU. See exercise 4 in Part 0. Do not use the server for assignment 3 in this assignment.

Deployment: In this assignment, you can choose to use localhost or use WebStrar. In both cases, you must submit the entire project in a single zip file into the Canvas submission site.

The entire project must include all project files of the service and the application, so that the project can be tested by the TA. You also need to submit the files used in the services, such as Persons.xml, Persons.xsd, Persons.xsl, and generated by the services, such as Persons.htm (or Persons.html), and the screenshot of the testing results in a Word or PDF file. Zip all these files in Assignments 7 and 8 into a zip file for submission.

<h1>Submission Requirement</h1>

All submissions must be electronically submitted to the assignment folder where you downloaded the assignment paper. All files must be zipped into a single file.




Canvas submission notice: The assignment consists of multiple distributed projects and components. They may be stored in different locations on your computer when you create them. You must copy these projects into a single folder for Canvas submission. To make sure that you have all the files included in the zip file and they work together, you must test them before submission. You must also download your own submission from the Canvas. Unzip the file on a different location or machine, and test your assignment and see if you can run the solution in a different location, because the TA will test your application on a different machine.

<h1>Grading and Rubrics</h1>

Each sub-question (component) has been assigned certain points. We will grade your programs following these steps:

<ul>

 <li>Compile the code. If it does not compile, 50% of the points given for the code under compilation will be deducted. Then, we will read the code and give points between 50% and 0, as shown in right part of the rubric table.</li>

 <li>If the code passes the compilation, we will execute and test the code using test cases. We will assign points based on the left part of the rubric table.</li>

</ul>

In both cases (passing compilation and failed compilation), we will read your program and give points based on the points allocated to each component (sub-question), the readability of your code (organization of the code and comments), logic, inclusion of the required functions, and correctness of the implementations of each function.

Please notice that we will not debug your program to figure out how big or how small the error is. You may lose 50% of your points for a small error such missing a comma or a space!

We will apply the following rubrics to <strong>each sub-question</strong> listed in the assignment. Assume that points assigned to a sub-question is <em>pts</em>:

<ul>

 <li></li>

</ul>