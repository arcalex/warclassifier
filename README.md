# warclassifier

While the role of web archiving in preserving our digital heritage is undeniable, unlocking its full potential continues to call for ongoing enhancements. Given the huge number of records that we find in a web archive, we can expect that the ability to organize content into categories will enhance usability. We approached web archive content classification using advanced machine learning techniques, specifically, zero-shot learning. Our goal is to offer a tool for classification of web archive content, so that this information can eventually be useful in making web archives a more navigable digital landscape for information retrieval as well as research.

We developed WARClassifier, a tool for classifying content in WARC files. The user supplies an arbitrary list of target categories. The tool makes use of a zero-shot classifier provided by Facebook’s BART model pretrained on the Multi-NLI dataset to attempt to associate HTML documents in the set of WARC files with the user-supplied candidate labels. The output is produced in the form of CSV data.

Data preprocessing is performed as the first step to ensure that the data is cleaned and formatted appropriately for analysis. WARClassifier depends on another tool, WARChtml, to iterate through WARC records and extract HTML elements that contain text into JSON format.

Zero-shot learning enables the model to generalize its understanding across previously unseen content types by leveraging semantic relationships and attributes associated with them. This is advantageous when it comes to classification of large data such as web archive data, since training models to recognize a predefined set of categories is no longer required.

For evaluation, we carried out lightweight human validation of model predictions. We also  experimented with inputting similarly labeled data to assess prediction correctness.

Looking ahead, our plan is to continue to work on evaluation and tuning of the classification, and to eventually use the categorization information to enhance access to web archives by developing improved search, content recommendation, and categorized research dataset extraction.

Keywords: web archiving, content classification, machine learning, zero-shot learning
