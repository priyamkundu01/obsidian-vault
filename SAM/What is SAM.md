![[Pasted image 20260717233713.png]]

**Aim** - Build a foundation model for image segmentation
(Image segmentation - Instead of locating the object, segmentation finds **its exact shape**. Every pixel belonging to the object)
(That is why segmentation is much harder than classification or detection.)

It is an **ecosystem**, a project.

Components
- a promptable segmentation task
- a segmentation model (SAM) that powers data annotation and enables zero-shot transfer to a range of tasks via prompt engineering
- data engine for collecting SA-1B (dataset of over 1 billion masks)

Here, **efficient** means:
- fast
- interactive
- inexpensive to use
- capable of running repeatedly

The model isn't just solving segmentation.
It is **helping create data**.

**Feedback loop** or **data collection loop** or **Data engine**
Collect Data
↓
Train Model
↓
Model helps collect MORE data
↓
Train Better Model
↓
Better Model collects EVEN MORE data
↓
Train Again
↓
Repeat


Human clicks once
↓
SAM predicts mask
↓
Human corrects small mistakes
↓
Save mask

As SAM improves,
the human edits less.

Eventually,
SAM becomes so good that humans barely need to help.


SAM **introduces**,
Data
↓
Model
↓
Better Data
↓
Better Model
↓
Better Data
↓
Better Model


In NLP (GPT-3, GPT-4)
there's a common pattern

Better model
↓
More data
↓
Even better model

Mostly because of
- larger models
- more compute
- more data

### What is a "mask"?
A segmentation mask is **not** the image itself.

It is another image of the same size where each pixel says:
1 = belongs to cat
0 = doesn't belong to cat

1 billion masks, 1 billion images.
Because one image contains many objects.

1 Image
↓
Many Masks

Example of **Responsible AI (RAI)**

**Licensed Images**
They acquired images through proper licensing agreements.

**Privacy Respecting**
They intentionally avoided exposing personal information.
Things like blurring faces and license plates before releasing the dataset.

### Mental Map

             Humans
                │
                ▼
      Annotate a small dataset
                │
                ▼
          Train SAM
                │
                ▼
SAM helps annotate more images
                │
                ▼
       More training data
                │
                ▼
          Better SAM
                │
                ▼
     Even faster annotation
                │
                ▼
        1.1 Billion Masks


Can we build a segmentation model that is so good and so fast that *it helps create its own training data*, allowing us to build an enormous segmentation dataset and, in turn, an even better model?

Instead of humans doing all the labeling, can the model become the annotator's assistant?

**Self-improving system**
Where the model and the dataset grow together.