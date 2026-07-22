### **"The model is designed and trained to be promptable..."**

### What is prompt

The prompt tells GPT **what you want**.

> Can we do the same thing for images?

Instead of text prompts, we give **visual prompts**.
A prompt tells the model **what to segment**.

Possible prompts:
- Point Prompt
- Box Prompt
- Text Prompt
- Mask Prompt

So "promptable" simply means

> **The model can accept different kinds of instructions telling it what to segment.**


**Philosophy of foundation models**

Image + Prompt
↓
SAM
↓
Requested Object

The same model works.
Only the prompt changes.

### Promptable Model

A promptable model can accept different kinds of prompts and generate the required segmentation.

Instead of changing the model,

we only change the prompt.
### Transfer Learning

Learning something once
↓
Using it somewhere else.

In AI,
suppose a model learns millions of objects.

Later,
it sees a new dataset.
Instead of training again,
it already knows enough.

That is called
**transfer**.

### Zero-shot
A "shot" means **an example.**

### One-shot

Show
1 example
↓
Predict.

### Few-shot

Show
5 examples.
↓
Predict.

### Zero-shot

Show
**No examples.**
↓
Still predict correctly.

### What is an image distribution?

A distribution is simply

> **The type of images the model usually sees.**


# Why is zero-shot important?

Traditional segmentation:
New Dataset
↓
Collect labels
↓
Train
↓
Test

SAM hopes to do
New Dataset
↓
Prompt
↓
Done.

### Exactly what the authors mean by **promptable**, **zero-shot**, and **transfer**.

> **The model is not trained to solve one specific task. It is trained to become generally useful.**

| Term                          | Simple meaning                                                                                                     |
| ----------------------------- | ------------------------------------------------------------------------------------------------------------------ |
| **Promptable**                | The model accepts instructions (points, boxes, text, masks) telling it what to segment.                            |
| **Transfer**                  | Knowledge learned during training can be reused on new problems.                                                   |
| **Zero-shot**                 | The model works on new data or tasks without additional training.                                                  |
| **Image distribution**        | The kind or domain of images (natural photos, medical images, satellite images, etc.).                             |
| **Foundation Model**          | A foundation model is a large general-purpose model trained on diverse data so it can solve many downstream tasks. |
| **Fully Supervised Learning** | Training using manually labeled ground truth.                                                                      |
| **Image Segmentation**        | Classifying every pixel into an object or region.                                                                  |
| **Segmentation Mask**         | Pixel-level binary or labeled image showing the object.                                                            |
| **Prompt**                    | Instruction telling the model what to segment.                                                                     |
| **Promptable Segmentation**   | Segmenting an object based on a user/system prompt.                                                                |
| **Promptable Model**          | A model that accepts different prompt types.                                                                       |
| **Foundation Model**          | General-purpose model reusable across many tasks.                                                                  |
| **Zero-shot**                 | Solving a new task without retraining.                                                                             |
| **Transfer Learning**         | Applying learned knowledge to new tasks.                                                                           |
| **Image Distribution**        | Type/domain of images (medical, natural, satellite, etc.).                                                         |
| **Fully Supervised**          | Training with manually labeled ground-truth masks.                                                                 |
| **Data Engine**               | Iterative cycle where the model helps create more training data.                                                   |
| **Efficient Model**           | Fast enough for real-time practical use, especially annotation.                                                    |
| **Licensed Images**           | Legally acquired images.                                                                                           |
| **Privacy Respecting**        | Images processed to protect personal privacy.                                                                      |
They built a general model, and surprisingly, it performs almost as well as—or sometimes even better than—models that were specially trained for individual tasks.

It is a a **general-purpose segmentation model**.

SAM is solving **many tasks with one model**.

# Fully Supervised

Fully supervised means

> Every training image has a manually created ground-truth segmentation mask.

This is expensive.

### Summary of the Abstract so far

The abstract has now established the complete story:

1. **Problem:** Existing segmentation models are specialized.
2. **Solution:** Build a **promptable foundation model** called SAM.
3. **Key innovation:** Use SAM itself to help create a massive dataset (SA-1B) through a data engine.
4. **Result:** A single model can solve many segmentation-related tasks in a **zero-shot** manner, often approaching or surpassing specialized supervised models.

*We hope this project becomes the starting point for many future papers*