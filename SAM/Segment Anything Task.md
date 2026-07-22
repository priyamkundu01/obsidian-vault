
SAM is **not required to guess the user's exact intention**.

It only needs to predict **one reasonable segmentation mask** corresponding to the prompt.

SAM gives **one valid segmentation mask**, even if multiple interpretations exist.


After training, SAM can solve many segmentation tasks:
- without retraining,
- simply by changing the prompt.

This is **zero-shot transfer**.