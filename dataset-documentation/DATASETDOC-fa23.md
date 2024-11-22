***Project Information*** 

* What is the project name?  
  * Maple Bill Summarization  
* What is the link to your project’s GitHub repository?   
  * https://github.com/BU-Spark/ml-maple-bill-summarization  
* What is the link to your project’s Google Drive folder? \*\**This should be a Spark\! Owned Google Drive folder \- please contact your PM if you do not have access\*\**  
  * [https://drive.google.com/drive/u/3/folders/1kXyaCjKCsMnMZBj0NUshKvANSkaFtyvq](https://drive.google.com/drive/u/3/folders/1kXyaCjKCsMnMZBj0NUshKvANSkaFtyvq)   
* In your own words, what is this project about? What is the goal of this project?   
  * This project is about making Massachusetts bills more accessible and organized. Currently, bills on malegislature.gov are long, unorganized, and difficult to understand. Our goal was to summarize Massachusetts bills to make them simpler, more concise, and free of unnecessary technical jargon. Additionally, we add tags to each bill to make them more organized, i.e. “environmental”, “education”, “health care”.  
* Who is the client for the project?  
  * Massachusetts Platform for Legislative Engagement  
* Who are the client contacts for the project?  
  * Matt Victor matthewsteinvictor@gmail.com  
* What class was this project part of?  
  * DS549

***Dataset Information***

* What data sets did you use in your project? Please provide a link to the data sets, this could be a link to a folder in your GitHub Repo, Spark\! owned Google Drive Folder for this project, or a path on the SCC, etc.  
  * [https://github.com/BU-Spark/ml-maple-bill-summarization/tree/main/demoapp](https://github.com/BU-Spark/ml-maple-bill-summarization/tree/main/demoapp)   
* Please provide a link to any data dictionaries for the datasets in this project. If one does not exist, please create a data dictionary for the datasets used in this project. **(Example of data dictionary)**   
* What keywords or tags would you attach to the data set?  
  * Domain(s) of Application: Computer Vision, Object Detection, OCR, Image Classification, Image Segmentation, Facial Recognition, NLP, Topic Modeling, Sentiment Analysis, Named Entity Recognition, Text Classification, Summarization, Anomaly Detection, Other   
    * NLP  
    * Summarization  
  * Sustainability, Health, Civic Tech, Voting, Housing, Policing, Budget, Education, Transportation, etc.   
    * Civic Tech

*The following questions pertain to the datasets you used in your project.*   
*Motivation* 

* For what purpose was the dataset created? Was there a specific task in mind? Was there a specific gap that needed to be filled? Please provide a description.   
  * The main purpose for creating the dataset was to have access to the raw bill text. Using the malegislature API, we wrote a script to collect all of these bills to use for our project. We would continue to use this dataset for everything in our project, including EDA, summarization, and tagging. 

*Composition*

* What do the instances that comprise the dataset represent (e.g., documents, photos, people, countries)? Are there multiple types of instances (e.g., movies, users, and ratings; people and interactions between them; nodes and edges)? What is the format of the instances (e.g., image data, text data, tabular data, audio data, video data, time series, graph data, geospatial data, multimodal (please specify), etc.)? Please provide a description.   
  * The instances (rows) represent Massachusetts Bills.  
  * There is only one type of instance.  
  * Tabular data.  
* How many instances are there in total (of each type, if appropriate)?  
  * There are 6597 instances.  
* Does the dataset contain all possible instances or is it a sample (not necessarily random) of instances from a larger set? If the dataset is a sample, then what is the larger set? Is the sample representative of the larger set? If so, please describe how this representativeness was validated/verified. If it is not representative of the larger set, please describe why not (e.g., to cover a more diverse range of instances, because instances were withheld or unavailable).  
  * The dataset is a sample as it only contains bills from the current (193rd) General Court, which would mean our dataset contains bills from January 4, 2023 up to the date we collected them (\~ October 2023). The larger set would be a dataset containing every bill in all previous General Courts. I would say that our dataset is representative because we didn’t choose to include or omit any data ourselves.  
* What data does each instance represent? “Raw” data (e.g., unprocessed text or images) or features? In either case, please provide a description.   
  * Columns include: Title, BillNumber, DocketNumber, GeneralCourtNumber, PrimarySponsor, Cosponsors, JointSponsor, BillHistory, LegislationTypeName, Pinslip, DocumentText, EmergencyPreamble, RollCalls, Attachments, CommitteeRecommendations, Amendments  
* Is there any information missing from individual instances? If so, please provide a description, explaining why this information is missing (e.g., because it was unavailable). This does not include intentionally removed information, but might include redacted text.   
  * No information missing.  
* Are there recommended data splits (e.g., training, development/validation, testing)? If so, please provide a description of these splits, explaining the rationale behind them  
  * No traditional data splits. But we did reach out to our client for bills that they were particularly familiar/concerned with, so that we could summarize and tag these bills and give it back to them to evaluate.  
* Are there any errors, sources of noise, or redundancies in the dataset? If so, please provide a description.   
  * None.  
* Is the dataset self-contained, or does it link to or otherwise rely on external resources (e.g., websites, tweets, other datasets)? If it links to or relies on external resources,   
  * I think the data that the API endpoints return is self-contained because there are no references to or dependencies on external websites or resources. But the bills themselves could become outdated as the General Court ends and new ones start.  
  * Are there guarantees that they will exist, and remain constant, over time;  
    * As far as I know, the malegislature API should exist and remain accessible over time.  
  * Are there official archival versions of the complete dataset (i.e., including the external resources as they existed at the time the dataset was created)?  
    * There are no official versions of the data that come pre-collected in say a CSV file, but using the API you can go back to any general court number and collect the same data.  
  * Are there any restrictions (e.g., licenses, fees) associated with any of the external resources that might apply to a dataset consumer? Please provide descriptions of all external resources and any restrictions associated with them, as well as links or other access points as appropriate.   
    * No restrictions.  
* Does the dataset contain data that might be considered confidential (e.g., data that is protected by legal privilege or by doctor-patient confidentiality, data that includes the content of individuals’ non-public communications)? If so, please provide a description.   
  * No, all the data is sourced from a publicly available API. https://malegislature.gov/api/swagger/index.html?url=/api/swagger/v1/swagger.json\#/  
* Does the dataset contain data that, if viewed directly, might be offensive, insulting, threatening, or might otherwise cause anxiety? If so, please describe why.   
  * I guess it could, if a bill was addressing something of this nature. But I personally have not seen any.  
* Is it possible to identify individuals (i.e., one or more natural persons), either directly or indirectly (i.e., in combination with other data) from the dataset? If so, please describe how.   
  * The dataset does include the primary and co-sponsor of each bill, which is the individual who is pushing for a bill to be passed.  
* Dataset Snapshot, if there are multiple datasets please include multiple tables for each dataset. 


| Size of dataset | 44 MB |
| :---- | :---- |
| Number of instances | 6597 |
| Number of fields  | 16 |
| Labeled classes (for classification tasks) | N/A |
| Number of labels (for classification tasks) | N/A |


  
*Collection Process*

* What mechanisms or procedures were used to collect the data (e.g., API, artificially generated, crowdsourced \- paid, crowdsourced \- volunteer, scraped or crawled, survey, forms, or polls, taken from other existing datasets, provided by the client, etc)? How were these mechanisms or procedures validated?  
  * We used the official MALegislature API.  
* If the dataset is a sample from a larger set, what was the sampling strategy (e.g., deterministic, probabilistic with specific sampling probabilities)?  
  * Our dataset contains bills from the current General Court, covering the period from January 4, 2023, to January 7, 2025\. However, as our data collection happened in October 2023, the dataset only contains records up to that date. This doesn’t exactly fit into a sampling strategy, it’s more like we collected data available up to a certain date just due to the timing of things.  
* Over what timeframe was the data collected? Does this timeframe match the creation timeframe of the data associated with the instances (e.g., recent crawl of old news articles)? If not, please describe the timeframe in which the data associated with the instances was created.   
  * This data was collected in October 2023\. This timeframe does match the creation timeframe of the data, it was collected in 2023 and the actual data was created in 2023\.

*Preprocessing/cleaning/labeling* 

* Was any preprocessing/cleaning/labeling of the data done (e.g., discretization or bucketing, tokenization, part-of-speech tagging, SIFT feature extraction, removal of instances, processing of missing values)? If so, please provide a description. If not, you may skip the remaining questions in this section.   
  * No preprocessing/cleaning/labeling or altering of the dataset of bills. But to do retrieval augmented generation for summarization, we had to process some other data. This included using regex to find instances of references to laws inside the bill, making an API call to get the contents of the law, and storing it in a txt file (for [example](https://github.com/BU-Spark/ml-maple-bill-summarization/blob/main/demoapp/extracted_mgl.txt)).   
* Were any transformations applied to the data (e.g., cleaning mismatched values, cleaning missing values, converting data types, data aggregation, dimensionality reduction, joining input sources, redaction or anonymization, etc.)? If so, please provide a description.   
  * There were no transformations to the data itself.  
* Was the “raw” data saved in addition to the preprocessed/cleaned/labeled data (e.g., to support unanticipated future uses)? If so, please provide a link or other access point to the “raw” data, this could be a link to a folder in your GitHub Repo, Spark\! owned Google Drive Folder for this project, or a path on the SCC, etc.  
  * Yes the raw data is still the same. In this folder, [https://github.com/BU-Spark/ml-maple-bill-summarization/tree/main/demoapp](https://github.com/BU-Spark/ml-maple-bill-summarization/tree/main/demoapp), the raw data is ‘all\_bills.csv’.  
* Is the code that was used to preprocess/clean the data available? If so, please provide a link to it (e.g., EDA notebook/EDA script in the GitHub repository).   
  * [https://github.com/BU-Spark/ml-maple-bill-summarization/blob/main/demoapp/MGL\_extract.ipynb](https://github.com/BU-Spark/ml-maple-bill-summarization/blob/main/demoapp/MGL_extract.ipynb) 

*Uses* 

* What tasks has the dataset been used for so far? Please provide a description.   
  * The dataset has been used to summarize and tag bills, and packaged into a webapp using streamlit.  
* What (other) tasks or applications could the dataset be used for? Wh  
  * The dataset could be used to improve the summaries and tags.  
* Is there anything about the composition of the dataset or the way it was collected and preprocessed/cleaned/labeled that might impact future uses?   
  * We used the /documents endpoint to list all the bills in the current general court, then the /documents/{billNumber} endpoint to get the details of individual bills  
* Are there tasks for which the dataset should not be used? If so, please provide a description.  
  * None.

*Distribution*

* Based on discussions with the client, what access type should this dataset be given (eg., Internal (Restricted), External Open Access, Other)?  
  * Open Access.

*Maintenance* 

* If others want to extend/augment/build on/contribute to the dataset, is there a mechanism for them to do so? If so, please provide a description or a link to the code.  
  * Yes, there is a jupyter notebook that runs the code to generate the dataset. Link: https://github.com/BU-Spark/ml-maple-bill-summarization/blob/main/EDA/eda.ipynb

*Other*

* Is there any other additional information that you would like to provide that has not already been covered in other sections?  
  * None.

