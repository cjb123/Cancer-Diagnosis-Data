<p style="font-size:36px;text-align:center"> <h1> 1. <b>Personalized Medicine: Redefining Cancer Treatment</b> </h1> </p>

<h2>1.1. Description of Task</h2>

<p> Source: https://www.kaggle.com/c/msk-redefining-cancer-treatment/ </p>
<p> Data: Memorial Sloan Kettering Cancer Center (MSKCC)</p>
<p> Downloaded training_variants.zip and training_text.zip from Kaggle.</p> 

<h6> Context:</h6>
<p> Source: https://www.kaggle.com/c/msk-redefining-cancer-treatment/discussion/35336#198462</p>

<h2> 1.2 Problem Statement : </h2>
<p> Classify the given genetic variations/mutations based on evidence from text-based clinical literature. </p>

<h2> 1.3 Other Important Links </h2>
1. https://www.forbes.com/sites/matthewherper/2017/06/03/a-new-cancer-drug-helped-almost-everyone-who-took-it-almost-heres-what-it-teaches-us/#2a44ee2f6b25
2. https://www.youtube.com/watch?v=UwbuW7oK8rk 
3. https://www.youtube.com/watch?v=qxXRKVompI8

<h2> 1.4 Business objectives and constraints : </h2>
* No low-latency requirement.
* Interpretability is important.
* Errors can be very costly.
* Probability of a data-point belonging to each class is needed.

<h2> 1.5 Data Overview </h2>
- Source: https://www.kaggle.com/c/msk-redefining-cancer-treatment/data
- We have two data files: one contains the information about the genetic mutations and the other contains the clinical evidence (text) that  human experts/pathologists use to classify the genetic mutations. 
- Both these data files are have a common column called ID
- <p> 
    Data file's information:
    <ul> 
        <li>
        training_variants (ID , Gene, Variations, Class)
        </li>
        <li>
        training_text (ID, Text)
        </li>
    </ul>
</p>

<h2> 1.6 Machine Learning Problem mapping : </h2>
<p> For a unique Gene and Variation pair, taking the text we need to classify which of the given classes it belongs to </p>
<p> There are nine different classes a genetic mutation can be classified into.Therefore it is a Multi class classification problem  </p>

<h2> 1.7 Performance Matrix </h2>
Source: https://www.kaggle.com/c/msk-redefining-cancer-treatment#evaluation
Metric(s): 
* Multi class log-loss 
* Confusion matrix 



<h2> Objective: </h2>
<p>Predict the probability of each data-point belonging to each of the nine classes.
</p>
<p> Constraints:
</p>
* Interpretability
* Class probabilities are needed.
* Penalize the errors in class probabilites => Metric is Log-loss.
* No Latency constraints.








