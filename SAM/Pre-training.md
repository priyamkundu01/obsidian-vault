
### Training Procedure

For each training image:

1. Generate multiple prompts (point, box, mask, etc.).
2. Predict a segmentation mask.
3. Compare the prediction with the ground-truth mask.
4. Compute the loss.
5. Update the model.

---

### Difference from Interactive Segmentation

**Interactive Segmentation**

- Multiple user interactions.
- Prediction improves after each new prompt.

**SAM Pre-training**

- Single prompt.
- Predict a valid mask immediately, even if the prompt is ambiguous.

---

### Why Train This Way?

- Handles ambiguous prompts.
- Supports automatic annotation in the Data Engine.
- Enables zero-shot generalization after pre-training.

---

|Interactive Segmentation|SAM|
|---|---|
|User can provide many prompts|Designed to work from any given prompt|
|Mask improves after repeated interaction|Predicts a valid mask immediately|
|Optimized for interactive correction|Optimized for generalization and automatic annotation|
