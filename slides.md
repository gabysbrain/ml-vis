% Visualization of machine learning algorithms
% Thomas Torsney-Weir
% VDA research group, University of Vienna

## Outline

* Introduction to Machine learning
* Vis helping machine learning
* Machine learning helping vis

## What is machine learning?

> "A rational agent is one that acts so as to achieve the best
> outcome or, when there is uncertainty, the best expected
> outcome" 

[@Russell:2009]

Algorithms that can improve their performance based on training data

## What is machine learning?

![](images/ml_why_1.svg)

<aside class="notes">
Let's say you want to help your friend Isaac Newton figure out 
how to dodge apples
</aside>

## What is machine learning?

![](images/ml_why_2.svg)

<aside class="notes">
Record data on behavior, come up with a model. This was done in the past!
This is hard!
</aside>

## What is machine learning?

![](images/ml_why_3.svg)

<aside class="notes">
So we can replace the human. Computers are good at processing data!
</aside>

## What is machine learning?

![](images/ml_why_4.svg)

<aside class="notes">
So we can just use a machine learning algorithm to replace the model for us!
How does this work?
</aside>

## Types of algorithms

* Regression
* Classification
* Clustering

<aside class="notes">
go over types of algorithms, ask about tasks.
</aside>

## What to use?

* Regression: Predict continuous values
* Classification: Predict discrete values
* Clustering: Find distributions

<aside class="notes">
People often confuse clustering as classification where they don't 
know the classes
</aside>

## Regression

Predict continuous values

![](images/regression1.png)

[@Bishop:2006]

## Regression

Predict continuous values

![](images/regression2.png)

[@Bishop:2006]

## Regression

Predict continuous values

![](images/regression3.png)

[@Bishop:2006]

## Regression

Predict continuous values

![](images/regression4.png)

[@Bishop:2006]

## Regression

Predict continuous values

![](images/regression5.png)

[@Bishop:2006]

## Regression

Predict continuous values

![](images/regression6.png)

[@Bishop:2006]

## Regression

Predict continuous values

![](images/regression7.png)

[@Bishop:2006]

## Classification

Predict discrete values

![](images/classification.png)

[@Bishop:2006]

<aside class="notes">
Discrete values are also called classes
</aside>

## Clustering

Find distributions

![](images/Figure9.1a.png)

[@Bishop:2006]

## Clustering

Find distributions

![](images/Figure9.1b.png)

[@Bishop:2006]

## Clustering

Find distributions

![](images/Figure9.1c.png)

[@Bishop:2006]

## Clustering

Find distributions

![](images/Figure9.1d.png)

[@Bishop:2006]

## Clustering

Find distributions

![](images/Figure9.1h.png)

[@Bishop:2006]

## Clustering

Find distributions

![](images/Figure9.1i.png)

[@Bishop:2006]

## Types of ML algorithms

* Regression: Predict continuous values
* Classification: Predict discrete values
* Clustering: Find distributions

## Uses

* naive Bayes: spam filtering
* classification: recommender systems
* neural networks: handwriting recognition
* HMM: speech recognition

## Email filtering

* is email spam or not?
* use words as features

$$
P(C=c_k | X=x) = \frac{P(X=x | C=c_k) P(C=c_k)}{P(X=x)}
$$

[@Sahami:1998]

## Recommender systems

![](images/recommenders.jpg)

http://blog.soton.ac.uk/hive/2012/05/10/recommendation-system-of-hive/

## Handwriting recognition

![](images/mnist.png)

## Speech recognition

![](images/hmm_speech.png)

http://recognize-speech.com/images/LanguageModel/left_to_right_HMM.png

## Vis and ML

* both vis and ML seem to have similar goals: make sense of complex data

<div class="columns">
  <div class="column">
    <h3>Machine learning</h3>
    ![](images/ml_why_4.svg)
  </div>
  <div class="column">
    <h3>Visualization</h3>
    ![](images/morton2012.png)
    [@Morton:2012]
  </div>
</div>

## Who helps whom?

### both!

* Vis helps ML: evaluating models
* ML helps vis: ML for embedded analysis

## Now to the vis part

How do they work together?

* Building models
* Validating models
* Understanding models
* Embedding ML algorithms

# Building models

## What are meta parameters?

Meta parameters control how learning takes place

* Learning rate
* Number and size of network layers
* Slack variables
* Stopping conditions

## Why study meta-parameters?

<div class="columns">
  <div class="column">
    <img src="images/raw_brain.png" /> 
  </div>
  <div class="column">
    <img src="images/good_seg.png" class="fragment" />
  </div>
</div>
<aside class="notes">
So let's talk about image segmentation
</aside>

## Why study meta-parameters?

<div class="columns">
  <div class="column">
    <img src="images/good_seg.png" /> 
  </div>
  <div class="column">
    <img src="images/bad_seg.png" />
  </div>
</div>
<aside class="notes">
Same algo different params
</aside>

## Manual method

<figure>
<img src="images/2d_sampling_1.svg" />
</figure>

## Manual method

<figure>
<img src="images/2d_sampling_2.svg" />
</figure>

## How to study them?

run a bunch of models and examine outputs

* design galleries
* paramorama

<aside class="notes">
Works well when you have no real metric for what you're looking for
</aside>

## Design galleries

![](images/design_galleries_1.png)

[@Marks:1997]

## Design galleries

![](images/design_galleries_2.png)

[@Marks:1997]

## Paramorama

![](images/paramorama_interface.png)

[@Pretorius:2011]

## How to study them?

use a more principled approach

## Objective measures

<figure>
<img src="images/obj_measures.svg" />
</figure>

## Visual parameter space exploration

* intro
* conceptual pipeline

<figure>
<img src="images/vpsa_pipeline.png" alt="conceptual pipeline" />
</figure>
<p>
<span class="citation" data-cites="Sedlmair:2014">
  Michael Sedlmair, Christoph Heinzl, Stefan Bruckner, Harald Piringer, and Torsten Möller
  &quot;Visual parameter space analysis: A conceptual framework&quot;
  IEEE Transactions on Visualization and Computer Graphics. 20(12) 2014.
</span>
</p>

## Tuner

<figure>
<img src="images/tuner_pipeline.svg" alt="image segmentation pipeline" />
</figure>

[@Torsney-Weir:2011]

## Real-time parameter tuning

![](images/lindhart.png)

Lindhart et al. 2018?

## Building models

* Meta parameters can have a large influence on performance
* Almost *all* ML algorithms require tuning
* Manual tuning is time consuming and error prone

<aside class="notes">
Conclude

CS people love algorithms but params are important
</aside>

# Validating and verifying models

## What do we mean?

* How do we know our models are working?
* model selection

![model](images/vv_model.png)
[@UQreport:2012]

## Examples

* HyperMoVal - local inspection
* Sliceplorer - global inspection
* Tuner - error inspection

## HyperMoVal

![](images/hypermoval_interface.png)

[@Piringer:2010]

## Sliceplorer views

<div class="columns">
<div class="column">
### Single layer NN (26 nodes)
![](images/sp1.png)

### SVM (polynomial kernel)
![](images/sp2.png)
</div>
<div class="column">

### Dual layer NN (5 and 3 nodes)
![](images/sp3.png)

### SVM (RBF kernel)
![](images/sp4.png)
</div>
</div>

[@Torsney-Weir:2017]

## Tuner error views

Examining multi-dimensional functions

* error view shows where model is unsure
* can visually verify the model

<div class="columns">
  <div class="column">
    <h3 id="prediction">Prediction</h3>
    <figure>
    <img src="images/error_view.png" alt="Error view" /><figcaption>Error view</figcaption>
    </figure>
  </div>
  <div class="column">
    <h3 id="optimization">Optimization</h3>
    <figure>
    <img src="images/gain_view.png" alt="Gain view" /><figcaption>Gain view</figcaption>
    </figure>
  </div>
</div>

## Validating and verifying models

* Summary statistics are not always enough
* Balancing multiple objectives is difficult
* Certain training points might be very important

<aside class="notes">
Conclude
</aside>

# Understanding models

## Who needs this?

* models are complex
* the business world likes spreadsheets because they can 
  walk through the calculations

## Simple vs complex models

<div class="columns">
  <div class="column">
    ### Simple

    * small integer factors
    * small number of factors
    * low-depth trees
  </div>

  <div class="column">
    ### Complex

    * multi-layer neural network
    * gaussian process model
    * tSNE
    * non-linear
    * many decisions
  </div>
</div>

<aside class="notes">
Think about tutorials, etc to learn complex systems. These complex ML 
algorithms are trying to replicate these systems in some sense
</aside>

## What does complexity buy us?

* Global vs local models
* Deep-learning networks can deal with feature selection
* Can deal with edge cases

<aside class="notes">
- ask the students what is the simplest classifier they can think of
- simplest classifier: pick the most frequent class
</aside>

## Methods

* interaction
* walkthroughs
* simpler models ala LIME (Ribeiro et al. 2016)
* direct inspection

## Examples

* regression: Muhlbacher and Piringer
* clustering: Dis-function
* text processing: TagRefinery
* smaller models: Explanation explorer

## A partition-based framework for building and validating regression models

Directly interact with the model building process

![](images/muhlbacher2013.png)

[@Muhlbacher:2013]

## Dis-function

Build a distance function interactively

![](images/brown2012.png)

[@Brown:2012]

## TagRefinery

Tutorial/walkthrough system

![Text processing pipeline](images/tagrefinery_pipeline.png)

[@Kralj:2017]

<aside class="notes">
Popular in video games
</aside>

## TagRefinery

![](images/tagrefinery_interface.png)

[@Kralj:2017]

## TagRefinery

![](images/tagrefinery_interface2.png)

[@Kralj:2017]

## LIME method

![](images/lime1.png)

![](images/lime2.png)

[@Ribeiro:2016a]

## Explanation explorer

![](images/krause2017.png)

[@Krause:2017]

## Direct inspection

e.g. hidden states in a neural network

![](images/nn.jpg)

## LSTMvis

![](images/lstmvis_interface.png)

[@Strobelt:2018]

## LSTMvis

![](images/lstmvis_detail.png)

[@Strobelt:2018]

## DeepEyes

![](images/deepeyes_interface.png)

[@Pezzotti:2018]

## DeepEyes

![](images/deepeyes_detail.png)

[@Pezzotti:2018]

# Machine learning helping vis

## How?

![](images/sacha2014.png)

[@Sacha:2014]

* Use the strengths of ML and vis together
    - machines are good at calculating
    - humans are good at intuition
* Vis assisted by ML algorithms

## Book ad!

![](images/accelerando.jpg)

## Clustering

* Cluster and calendar view
* KeyVis
* FluidExplorer

<aside class="notes">
Clustering is used alot to group elements before visual inspection
</aside>

## Cluster and calendar view

![](images/wijk1999_1.png)

[@Van-Wijk:1999]

## Cluster and calendar view

![](images/wijk1999_2.png)

[@Van-Wijk:1999]

## Cluster and calendar view

![](images/wijk1999_3.png)

[@Van-Wijk:1999]

## KeyVis

step 1: cluster the papers based on keywords

![](images/keyvis_clustering.png)
[@Isenberg:2017]

<aside class="notes">
Goal is to find relevant papers
</aside>

## KeyVis

step 2: give an interface to this clustering

![](images/keyvis_interface.png)
[@Isenberg:2017]

## FluidExplorer

![](images/fluidexplorer_pipeline.png)

[@Bruckner:2010]

<aside class="notes">
Goal is to find good flame simulations. This is hard even for experts!
</aside>

## FluidExplorer

![](images/fluidexplorer_interface.png)

[@Bruckner:2010]

## FluidExplorer

![](images/fluidexplorer_clustering.png)

[@Bruckner:2010]

## Classification

![](images/brochu2010.png)

[@Brochu:2010]

<aside class="notes">
Same idea, different implementation.
Goal is to find good flame simulations. This is hard even for experts!
</aside>

## Understanding models

* Just an answer is not enough (show your work)
* Humans have trouble understanding complex models
* Interactivity can bring people into the model

# The future!

## Interesting projects

* More using ML to build models for vis tools
* More generalized tools
* Understand what "understandability" means

<aside class="notes">
Active learning
Humans: intuition, computers: data processing

Many tools are specific to a type of model

Understandability is only asserted
</aside>

## Thanks!

thomas.torsney-weir@univie.ac.at

http://www.tomtorsneyweir.com


