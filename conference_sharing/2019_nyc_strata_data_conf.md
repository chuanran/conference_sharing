# Strata data Conference 2019 - New York City
I got a chance to attend [O’Reilly Strata data Conference 2019 - NYC, New York](https://conferences.oreilly.com/strata/strata-ny), here are some talks I feel worth sharing. Please be mindful that this is a small selection. There are multiple parallel sessions happening and I can only attend one at a time. You can find all the useful https://conferences.oreilly.com/strata/strata-ny/public/schedule/proceedings


### The road to an enterprise cloud (keynote)

Hillery, the CTO of IBM Cloud gave an introduction of IBM Hybrid cloud strategy and CloudPak for Data. Hillery explained that IBM Cloud Pak for Data is a native cloud solution that enables you to put your data to work quickly and efficiently, especially enabling you connect to your data, govern it, find it, and use it for analysis. It's also ready for AI and includes an enterprise data catalog that helps you create a cohesive information architecture. It's also a private cloud solution by nature, and you have complete control of your data, and even if you do have data in the public cloud, you can also connect to your public cloud data sources from Cloud Pak for Data.

### AI isn't magic. It’s computer science. (keynote)

Rob Thomas, General manager of IBM Data and AI had a talk on IBM's AI strategy with O'Reily's CEO Tim Reily. There are some impressive QAs I want to highlight here:

* Tim Reily asked Rob what skills/capabilities a company typically lacking on AI, Rob mentioned that latest survey reveals that there is shortage of 250000 data scientists in the market, also mentioned that AI-builds-AI model such as feature engineering automation inside watson, automation of machine learning algorithm selection to narrow the skill gaps; 
* Tim also asked if there's anything that need to be done for infrastructure part to support AI well. Rob stated that though there's still reluctancy from customers to move their sensitive data to public cloud, the redhat private cloud and the hybrid cloud strategy could definitely give confidence to customers for their transition, and IBM cloud infrastructure can fulfill the challenges of AI. 
* Tim asked Rob how will he explain to a customer who has not used AI for their business yet, Rob said he would explain to customer that AI will not replace managers, but those managers who use AI will gonna replace those who are not using, and the best time to use AI in the business is right now, otherwise may be too late.


### Data sonification: Making music from the yield curve (keynote)
Based on a critical evaluation of the iconic yield curve chart, Alan Smith argues that combining visualization (data to pixels) with sonification (data to pitch) offers potential to improve not only aesthetic multimedia experiences but also an opportunity to take the presentation of data into the rapidly expanding universe of screenless devices and products.

IMO this is meaningful work since this can cover people with visual impairment, who wants to subjectively understand the trend of data changes as well.


### The future of Google cloud data processing (Keynote)
Open source has always been a core pillar of Google Cloud’s data and analytics strategy. James Malone gives out a prospect of future of opensource data processing, and examines how, as the community continues to set industry standards, the company continues to integrate those standards into its services so organizations around the world can unlock the value of data faster.

* At the very beginning of his speech, James brought up 2 challenges for running cloud dataproc(a managed spark & hadoop distribution) : portability and resource profile flexibility, which can be resolved by kubernetes such as: kubernetes operator for Apache Spark (released on Jan. 2019), cloud dataproc on kubernetes (Alpha, run both Yarn and kubernetes cluster) and kubernetes operator for Apache Flink (Sep. 2019)
* What it means to data scientists/data engineers? cross-cloud and hybrid cloud support, better OSS component isolation, support for vender-supported components on cloud Dataproc, faster development of cluster/ task management than Apache YARN. What it means to Cloud Dataproc is a uniformed control plane that offers mgmt, security, logging, monitoring across the YARN and kubernetes cluster 
* Then James gave a recorded demo on how to leverage YARN to trigger a pySpark job and how to do the similar thing in kubernetes world. In kubernetes world, it's using an existing kubernetes cluster (which has network settings there and other stuff running on it etc) and corresponding "helm install" can allow the cluster to plugin to cloud Dataproc APIs. The container for kubernetes world matches the YARN Based images, and don't need to worry about jogging between the two. After specifying the container we want to use, the notebook we want to run, Submit the spark job to the kubernetes cluster, which you don't need open ssh window to check the log output or care about the network settings, etc


### Everything is connected and the clock is ticking: AI and big ag data for food security (keynote)

Sara Menker and Nemo Semret come from Gro Intelligence, which targets on AI for agricuture.  Gro’s platform automatically harvests vast amounts of disparate global agricultural data, transforms it into knowledge, and generates predictions for volatile markets.
* Sara started the talk with an example that how the trade war between US and China could impact the agriculture (mostly focus on shortage of soybean) in  China, and she listed lots of contributors like: US is the biggest exporter for the soybean in China, so the duration of trade war is one contributor; how other substitutions of soybean can help make up for the shortage of the soybean; how other exporters can help on the shortage of soybean; the weather condition, disaster prediction , etc. Based on this example, Sara stated that there are lots of data need to be gathered for agriculture AI,outline the complex and interconnected factors that shape the agriculture industry, and everything is connected. Then Sara gave some basic introduction about what Gro Intelligence is doing and how it can help on establishing model for this kind of agriculture issues.

* Nemo, the CTO of Gro Intelligence gave out more details about the agriculture data/ontology challenges  Gro Intelligence faces such as following:
  * data volume is huge: every pixel on the earth, every day for 40 years; 100k weather stations, etc
  * data formats: satellite projections, PDF of scanned tables of data
  * different human languages since it's reported by all over the world
  * coverage/lags: human error, satellite can be covered by cloud, etc
  * Time: need to understand
  * Entities: lots of different entities such as there could be 50+ varieties for wheat (winter, spring, hard, soft, etc), protein content of wheat, sugar content of cane, etc

* When back to how Gro intelligence do the modeling about the agriculture data, Sara gave an example on Gro's unified model of agriculture applied to China and Swine fever, actually it's  modeling interplay between supply, demand, trade, price, for evey combination, every commodity, over and over again, then have to multiply that by each country that's connected to China. 

### Executive Briefing: Top 10 big data blunders
Michael Stonebraker is a computer scientist specializing in database research, and he's the CEO of Tamr (database company) as well. In this talk, he gave out top 10 big data blunders based on his academic and industry experiences. The ones that impressed me a lot include:
* Michael stated that data scientists only put 5%-%10 time/efforts on data science itself, and they have to put most of time on data engineering work such as data gathering, data cleaning, etc, which is not correct. Data engineers and data scientists should work together on the big data project and should make the scope more clear
* Belief that Hadoop/Spark will solve all your problems: Michael argued that Hadoop/Spark is not very good at anything,i.e. Spark/SQL is not particularly competitive, Spark/Streaming is not particularly competitive; Use "best of breed" not "lowest common denominator", and this is a universal blunder to use only one vendor
* Outsourcing your new stuff to other companies: Michael thinks it's not wise for enterprises to make the "shiny new stuff" get outsourced, and not wise as well for IT companies to have the best people maintain the legacy buggy stuff.
* Hire ordinary people to the company: As a CEO, Michael also stated that the company should always try to hire the most talent/strange people (he has a theory that a person who looks more strange/odd means that he may be a talent person at the same time), and should pay more to hire the correct people, i.e. hire the best people on data science and AI
* Lastly Michael did an advertisement for Tamr as well, and he stated that it's not wise to work for a company that is not trying to do something about the "Sins of the past". 


### Introducing a new anomaly detection algorithm(SR-CNN) inspired by computer vision
In this session, Microsoft's Qiyang Li, and Wenyi Yang introduce the pipeline and algorithm of Microsoft’s anomaly-detection service, which is designed to be accurate, efficient, and general. The pipeline consists of three major modules—data ingestion, experimentation platform, and online compute. They developed a novel algorithm based on SR and CNN, which is the first attempt to borrow the SR model from the visual saliency-detection domain and apply it to time series anomaly detection. Moreover, SR and CNN are innovatively combined to improve the performance of the SR model, achieving superior experimental results compared with state-of-the-art baselines on both public datasets and Microsoft production data.  Some key points include:
* The algorithm borrows the SR (Spectral Residual) model from visual saliency detection field, and apply CNN on the saliency   map produced by SR and train it with faked data;
* SR is unsupervised, accurate, simple, efficient, and with good generality. Unlikely to train CNN from the original time-series because lack of lables. However it's feasible to train CNN on the saliency map using fully synthetic data.
* Opensource code & KDD paper
  * SR in Python: https://github.com/microsoft/anomalydector
  * KDD 2019: https://www.kdd.org/kdd2019/accepted-papers/view/time-series-anomaly-detection-service-at-microsoft



### Automating ML model training and deployments via metadata-driven data, infrastructure,feature engineering, and model management

### spark on kubernetes for data science
Spark on Kubernetes is a winning combination for data science that stitches together a flexible platform harnessing the best of both worlds. Jordan Volz coming from Dataiku gives a brief overview of Spark and Kubernetes, the Spark on Kubernetes project, and explained why it’s an ideal fit for data scientists who may have been dissatisfied with other iterations of Spark in the past, and some applications.
He explained that spark as a bridge to "big data" and a distributed data processing framework, have flexible programming paradigm, and have been widely adopted by the industry. Specifically, there are several aspects that makes data scientist loves spark:  
* Targeted for handling large datasets
* strong support for Python/R APIs, and even provider higher-level APIs for non-experts
* the nature of parallel processing that can support hyperparameter tunning and large datasets scoring very well
* provides built-in distributed algorithms

However there are some drawbacks of spark that data scientist do NOT like, specifically as following:
* Managing a hadoop cluster
* Have to resolve dependencies for libaries
* Using GPUs. it cannot provide flexible resource profile like GPU
* Performance tunning and debugging

Based on above, spark on kubernetes project becomes necessary to make data scientist's life much easier. Kuberntes as the container orchestration platform can make the above drawbacks of spark better because: Docker container can help resolve the libararies/dependencies well; relatively easy and flexible resource profile (i.e. GPUs); the cloud nature can ensure the compute on demand, etc. However, this does NOT mean spark on kubernetes is perfect, the complexity of kubernetes add to the cost of potential operation tasks for data scientist, i.e. building docker images, troubleshooting when things don't work, Lacking some key features of Spark on Yarn, such as no kerberos, no External Shuffle Service, etc. 

Jordan then explained the gist of spark on k8s is to make Yarn kubernetes-rized, and containerizing executor and driver, and spark just works more or less as normal.He mentioned that starting from `spark 2.4` it becomes more user-friendly for data scientist, as docker images for pyspark/sparkR are ready for use. To elaborate how the overall process of spark on kubernetes works, he gives an overview as following:
* Get access to k8s cluster. BYO or vendor-managed (Notice that most of cloud vendor has its own kubernetes services, for IBM, such as openshift, IKS, for Amazon is EKS, etc). 
* Download spark binary onto client host
* Build base spark image with customization if needed
* Push spark docker images to a specific registry
* Run spark jobs

Jordan at last shared some best practice on configuration/tips for  spark on K8s

### Some other popular sessions that I did not get a chance to attend

* Deep	Learning	Methods	for	Natural	Language	Processing (Garrett	Hoffman, materials see: https://github.com/GarrettHoffman/talks-and-tutorials/tree/master/strata-2019-dl-for-nlp)
* An	in-depth	look	at	the	data	science	career:	Defining	roles,	assessing	skills	(Usama	Fayyad, Hamit	Hamutcu): Usama Fayyad and Hamit Hamutcu launched the Initiative for Analytics and Data Science Standards (IADSS) to support the development of standards regarding analytics role definitions, required skills, and career advancement paths
* Handling data gaps in time series using imputation Presentation (Alfred Whitehead, Clare Jeon): Alfred Whitehead and Clare Jeon explore a number of methods for handling data gaps and advise you on which to consider and when. You’ll see how to perform tests to determine which method suits your problem the best. 

### some other popular topics in expo Hall including: 
* data lake ecosystems
* database systems: graph DB, etc
* ML Ops (ops for machine learning),etc









