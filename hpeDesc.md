## Template Extraction & Anomaly Detection of Log Messages 

##### Hewlett Packard Enterprise | Data Science Intern 
**Business Problem:** When customers have system failures support engineers would have to spend hours of time looking through log messages to troubleshoot any error or failure. My work was to find a solution to identify these harmful messages and save time.

**Solution Highlights:** 
  * Developed a full model pipeline that took unstructured log messages and leveraged Hierarchical  Clustering based template extraction to transform 4 million unique log messages into 84 templates.  
  * Increased efficiency of support engineers identifying harmful log messages by over 30% in weekly ticket completions.  
  * Implemented an Unsupervised anomaly detection algorithm to identify harmful log messages based on auto-embeddings of extracted templates. 


**Write-up:** 


This work was done as a Data Science Intern at Hewlett Packard Enterprise. I worked on the Primary Storage Customer Engineering Team.

The first step of this process was to perform template extraction on all log messages. Template Extraction works by vectorizing log messages and using hierarchal clustering to find common patterns between log messages. Using the template extraction model I created, we were able to turn a dataset of 3 million different log messages into 84 templates.

By having our log messages in template format makes our dataset much more compatible for log sequence anomaly detection. Along with the pattern template, we can also use the unique attributes of the original log message as additional features.

When running anomaly detection on sequences of log messages, we are able to easily identify rare log messages that may appear.


###### All Intellectual Property of this work belongs to Hewlett Packard Enterprise and therefore I cannot show any code.


