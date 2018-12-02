<body>

<h1>
Neural Information Retrieval
</h1>

Daniel Keller

<h3>Introduction</h3>

Neural Information Retrieval is an exciting space that is currently developing.
Please use these curated resources as a way to start reading about the field.

<h3>Surveys</h3>

Here is collected variety of surveys.  Depending on which form of survey you prefer,
the surveys are organized into reports and slides.

***
<h4>Reports</h4>

<b>Neural information retrieval: at the end of the early years</b> (2018, IR) <a href="https://link.springer.com/article/10.1007/s10791-017-9321-y">[paper]</a><br/>
Kezban Dilek, Ye Zhang, Ismail Sengor Altingovde, Md Mustafizur Rahman, Pinar Karagoz, Alex Braylan, Brandon Dang, Heng-Lu Chang, Henna Kim, Quinten McNamara, Aaron Angert, Edward Banner, Vivek Khetan, Tyler McDonnell, An Thanh Nguyen, Dan Xu, Byron C. Wallace, Maarten de Rijke, Matthew Lease


<b>An Introduction to Neural Information Retrieval</b> (2017, FnTIR) <a href="https://www.microsoft.com/en-us/research/publication/introduction-neural-information-retrieval/">[paper]</a></br>
Bhaskar Mitra, Nick Craswell


<b>Neural Models for Information Retrieval</b> (2017, arXiv) <a href="https://arxiv.org/pdf/1705.01509.pdf">[paper]</a></br>
Bhaskar Mitra, Nick Craswell


***
<h4>Slides</h4>

<b>Neural Networks for Information Retrieval</b> (2018) <a href="http://nn4ir.com/">[slides]</a></br>
Tom Kenter, Alexey Borisov, Christophe Van Gysel, Mostafa Dehghani,and Maarten de Rijke, and Bhaskar Mitra

<b>Neural Text Embeddings for Information Retrieval</b> (2017, WSDM) <a href="https://www.slideshare.net/BhaskarMitra3/neural-text-embeddings-for-information-retrieval-wsdm-2017">[slides]</a></br>
Bhaskar Mitra, Nick Craswell


<h3>Papers of Note</h3>

Papers are annotated with brief synopsis of the main lessons learned when I read them.

***

<b>Distributed Representations of Sentences and Documents</b> (2014, ICML) <a href="https://arxiv.org/abs/1405.4053">[paper]</a><br/>
Quoc V. Le, Tomas Mikolov

Synopsis:  Aims to improve upon bag-of-word embeddings by building new fixed
length representations that can be formed from variable-length pieces of text.  
Additionally, these new embeddings, called Paragraph Vectors, learn on the entire
document at once, leading them to learn the ordering and semantics of words.  These
vectors are then used by the authors on several text classification and sentiment
analysis tasks, and they are able to achieve state of the art.

***

<b>Embedding-based Query Language Models</b> (2016a, ICTIR) <a href="https://ciir-publications.cs.umass.edu/getpdf.php?id=1225">[paper]</a><br/>
Hamed Zamani and W. Bruce Croft

Synopsis:  This paper applies word embeddings to the task of ad-hoc retrieval.
A major problem in ad-hoc retrieval is vocabulary mismatch, wherein the words
used in a query to describe an idea do not match the words used in a document
to describe the same idea.  This makes it difficult to find relevant documents
purely based on what words an author chooses to use.  The authors of this paper
circumvent this problem by using word embeddings to find the cosine similarity between
query terms and the terms used in documents, avoiding the vocabulary mismatch problem.
They then construct several models that use embeddings, and these models significantly
outperform competitive baselines in many tasks.

***

<b>A Deep Relevance Matching Model for Ad-hoc Retrieval</b> (2016, CIKM) <a href="https://arxiv.org/pdf/1711.08611.pdf">[paper]</a><br/>
Jiafeng Guo, Yixing Fan, Qingyao Ai, W. Bruce Croft

Synopsis:  In this paper, the authors propose a new model, DRMM, for ad-hoc retrieval.  
While other papers tried to model ad-hoc retrieval as a semantic matching problem
(wherein documents are scored based solely on their semantic similarity to a query),
this paper proposes that it is better to describe it as a relevance matching problem
(wherein documents are scored on their semantic similarity to a query and a variety
of other features, such as query term importance).  They then construct a deep
learning model that tries to address ad-hoc retrieval as a relevance matching problem
by using matching histogram mapping, a feed forward matching network, and a term gating network,
and this model outperforms competitive baselines for almost all tasks tested.

***

<b>Analysis of the Paragraph Vector Model for Information Retrieval</b> (2016, ICTIR) <a href="https://dl.acm.org/citation.cfm?id=2970409">[paper]</a><br/>
Qingyao Ai, Liu Yang, Jiafeng Guo, W. Bruce Croft

Synopsis:  Due to the popularity of the paragraph vector embeddings proposed by
the paper above, this paper tries to analyze the effectiveness of PV embeddings
across a variety of IR tasks by adding them to many traditional IR models.  
Unfortunately, PV embeddings underperform in many tasks and lead to unstable performance.
The paper then goes on to identify why this is: specifically, PV embeddings suffer
from over-fitting to short documents, overly suppress the importance of frequent words,
and are unable to capture word-substitution relationships.  They propose several improvements
on the PV model, and then show how these improvements lead to improved performance
on the tasks they previously tested.

***

<b>DeepRank: A New Deep Architecture for Relevance Ranking in Information Retrieval</b> (2017, CIKM) <a href="https://arxiv.org/pdf/1710.05649.pdf">[paper]</a><br/>
Liang Pang, Yanyan Lan, Jiafeng Guo, Jun Xu, Jingfang Xu, Xueqi Cheng

Synopsis:  This paper proposes a new model, DeepRank, that builds off of the previously
developed DRMM and DSSM.  DeepRank attempts to model how humans themselves would
undertake an information retrieval process.  To do this, they build a detection
strategy that finds relevant contexts from a document.  They then construct a
matching network that learns proximity data from the gathered relevant contexts,
and then finally feeds into an aggregation network.  Clearly, trying to model
human behavior paid off in some ways, as this model outperforms all other baselines.

***

<b>MatchZoo: A Toolkit for Deep Text</b> (2017, SIGIR Workshop on Neural IR) <a href="https://arxiv.org/pdf/1707.07270.pdf">[paper]</a><br/>
Yixing Fan, Liang Pang, JianPeng Hou, Jiafeng Guo, Yanyan Lan, Xueqi Cheng

Synopsis:  This paper proposes a toolkit for building deep learning text matching
systems.  They construct a system to uniformly process data, a layer based
model building process, and a suite of tools that can be used to evaluate models.

***

<b>Neural Ranking Models with Weak Supervision</b> (2017, SIGIR) <a href="https://arxiv.org/pdf/1704.08803.pdf">[paper]</a><br/>
Mostafa Dehghani, Hamed Zamani, Aliaksei Severyn, Jaap Kamps, W. Bruce Croft

Synopsis:  This paper proposes using weak supervision for information retrieval.
While unsupervised learning is challenging in IR due to the complexity of relevance
matching, this paper attempts to simplify the problem by using a basic unsupervised
IR model BM25 as a weak supervision signal.  They then train a simple model based
on feed forward networks to learn from the weakly supervised data, and find that
the model outperforms the BM25 baseline.  Additionally, they find that they
can generate performance gains by pre-training supervised models on weakly supervised data.

***

<b>Neural Ranking Models with Multiple Document Fields</b> (2017, WSDM) <a href="https://arxiv.org/pdf/1711.09174.pdf">[paper]</a><br/>
Hamed Zamani, Bhaskar Mitra, Xia Song, Nick Craswell, Saurabh Tiwary

Synopsis:  This paper proposes a model that uses neural nets to do relevance
matching using every field of a document.  The primary contribution of this paper
is a complex hyper-parameter based system that can structured to learn from
multiple document fields of varying length, occurrence, and importance.  Additionally,
their model has several clever additions that allow it to learn from all fields
of a document in case certain high predictability fields are left empty during prediction.
These techniques significantly improve the performance of the ranker, and ideally
should be used in future neural IR models moving forward, as using multiple document
fields has been shown in both feature based IR models and neural models to be helpful.

***

Neural Vector Spaces for Unsupervised Information Retrieval (2018, TOIS) <a href="https://arxiv.org/pdf/1708.02702.pdf">[paper]</a><br/>

Synopsis:  This paper proposes a method for ranking documents in an unsupervised manner.
Using gradient descent, the model the paper proposes is able to build low-dimensional
representations of documents and queries from scratch and rank documents by their
similarity with queries.  They then add these vector spaces to a variety of baselines,
and they find that adding these vector spaces improve the performance of many baselines.
After additional testing, they determine that neural vector spaces seem to learn the notion
of term specificity.  They also learn regularities related to Luhn Significance,
meaning that neural vector spaces learn which terms are important for document ranking.




</body>
