
Because SAM was trained with **many kinds of prompts**, it learns how to interpret them.

So during **inference (testing/real use)**, it can respond correctly to **new prompts** it has never seen before.

### Key Terms

- **Inference time:** When the trained model is used to make predictions.
- **Endows:** Gives the model the ability.

### Core Idea

A model trained on the **Promptable Segmentation Task** can solve **new segmentation tasks without retraining**.
### How?

1. Provide an appropriate prompt.
2. SAM interprets the prompt.
3. SAM generates the required segmentation mask.