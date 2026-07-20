The Medical Segment Anything Model (MedSAM) has shown remarkable performance in medical image segmentation, drawing significant attention in the field. However, ==its sensitivity to varying prompt types and locations poses challenges.==

This paper addresses these challenges ==by focusing on the development of reliable prompts== that enhance MedSAM’s accuracy.

We introduce **MedSAM-U**, ==an uncertainty-guided framework== designed to **automatically refine multi-prompt inputs** for more reliable and precise medical image segmentation.

Specifically, we first train a **Multi-Prompt Adapter integrated** with MedSAM, creating MPA-MedSAM, to adapt to diverse multi-prompt inputs. We then employ uncertainty-guided multi-prompt to effectively estimate the uncertainties associated with the prompts and their initial segmentation results.

In particular, a novel uncertainty-guided prompts adaptation technique is then applied automatically to derive reliable prompts and their corresponding segmentation outcomes.

We validate MedSAM-U using datasets from multiple modalities to train a universal image segmentation model. Compared to MedSAM, experimental results on five distinct modal datasets demonstrate that the proposed MedSAMU achieves an average performance improvement of 1.7% to 20.5% across uncertainty-guided prompts.