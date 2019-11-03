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


### Everything is connected and the clock is ticking: AI and big ag data for food security (keynote)

Sara Menker and Nemo Semret Come from  outline the complex and interconnected factors that shape the agriculture industry.



### Executive Briefing: Top 10 big data blunders: Michael Stonebraker is a computer scientist specializing in database research, CEO of Tamr. 

### From raw data to informed Intelligence: Democratizing data science and ML at Uber

### Introducing a new anomaly detection algorithm(SR-CNN) inspired by computer vision

### Devops in the cloud: Deploy, monitor, manage and automate



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








