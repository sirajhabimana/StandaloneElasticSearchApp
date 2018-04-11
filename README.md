# StandaloneElasticSearchApp
This is an elastic search that demonstrates how an xml file can be formatted into json and then indexed into elastic search. The data can then viewed using elastic search as json objects queried by ID
To use this application, install elastic search (I used 5.0.0). Once it is up and running, clone this project and import it into Intellij IDE. Run the file ElasticSearchSpringBootApplication.
Once it has successfully run, go to your favorite brower and enter the address http://localhost:8080/rest/products/bulk. This will index the file's contents into elastic search. The output is a string in the browser which consists of the IDs with which the contents were saved in elastic search.
To view the contents, enter the following address in your browser http://localhost:8080/rest/products/view/{id} or http://localhost:9200/product/id/{id}, where by {id} is one of the IDs in the output of 4 above.
Note: I am using the default ports 8080, 9200 and 9300 so ensure that they are free before running the application
Note also that the above indexing method uses the bulk API to index the records. To insert the records one by one, enter the following address in your browser: http://localhost:8080/rest/products/insertXML, and then to view the results, enter either of the addresses; http://localhost:8080/rest/products/view/{id} or http://localhost:9200/product/id/{id}, where {id} is 1, 2 or 3.
