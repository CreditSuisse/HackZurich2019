# HackZurich 2019

##  Welcome to the Credit Suisse HackZurich challenge!  

Within this repo you will find instructions and documentation on how to 
gain access to the to the IS&P Research articles 
produced by our team of analysts in Zurich for public consumption.  The code 
and data store however are all maintained and built by Credit Suisse Labs based in 
San Francisco CA.  

The first step you will have to do is to clone the repo.  When you 
clone it you will download a certificate file (client.cer) that will be used to gain access 
to the data store if you intend to access it via an API or REST library.  

The data is housed on a rather robust Elastic Search (7.1) cluster that is hosted 
on Google Cloud (GCP) with a Kubernetes cluster.    

If you are unfamiliar with ElasticSearch (ES), it is essentially an indexed database 
used for primarily documents and text based data.  The ES engine, tokenizes the documents' text to 
make searching very fast and "language aware".  The primary interface for ES is a REST API
meaning that you can simply send a curl request to the clusters with the proper password
and auth token and receive results back.  

Within this repo you will also find a simply python notebook (3.7) with further instructions and 
sample code to access the cluster.  The python code requires both the password and the cert file
however the basic curl command as below only requires the password.

```curl -u "hack_zurich:PASSWORD" -k "https://data.schnitzel.tech:9200/_cat/indices?v"```

To view the code within the notebook and run it you will need to install Jupyter Notebooks (see links 
below).

You can get the password by asking one of the Credit Suisse staff here at the event. 

Good Luck!

Useful Links:
1.  Jupyter Notebooks:  https://jupyter.org/install
2.  ES Overview:  https://www.elastic.co/guide/en/elasticsearch/reference/7.1/index.html
3.  ES Query Language Docs:  https://www.elastic.co/guide/en/elasticsearch/reference/7.1/query-dsl.html
4.  Python ES Library (used in the notebook):  https://elasticsearch-py.readthedocs.io/en/master/

