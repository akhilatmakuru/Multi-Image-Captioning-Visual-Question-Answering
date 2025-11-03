# Multi-Image Visual Question Answering (VQA) Demo

This project demonstrates a **state-of-the-art Visual Question Answering (VQA) system** capable of analyzing multiple images, generating general captions, and answering custom questions with confidence scores. The notebook showcases **multimodal AI integration** using **pre-trained transformer models** in a polished and professional workflow.

## Key Features

### 1. Multi-Image Support

* Process multiple images in a single notebook.
* Each image is displayed with:

  * A **general caption** describing the scene.
  * A set of **custom questions** with answers and confidence scores.

### 2. BLIP Captions (Image Description)

* Model: `Salesforce/blip-image-captioning-base`.
* Generates a **human-like summary of the image** (e.g., “an elephant standing in the dirt near a body of water”).
* Captions provide **context** and improve interpretability of the VQA outputs.

### 3. VQA with Confidence Scores

* Model: `dandelin/vilt-b32-finetuned-vqa`.
* Answers **specific questions** about the image using both **visual and textual information**.
* Provides **confidence scores** derived from the model’s logits to indicate certainty.
* Example questions:

  * What is in the image?
  * Describe the main objects.
  * What is happening?
  * What is the color of the main object?
  * How many main objects are there?

---

## Understanding the Models

**BLIP (Bootstrapped Language-Image Pretraining)**

* Focused purely on image content.
* Produces coherent and accurate descriptions.
* Works well for summarizing complex visual scenes.

**ViLT VQA (Vision-and-Language Transformer)**

* Combines **image understanding and textual reasoning**.
* Trained to answer questions based on image content.
* May produce less accurate answers on complex or unusual images.
* Confidence scores help interpret model uncertainty.

> BLIP provides **contextual understanding**, while VQA provides **question-specific reasoning**. The combination demonstrates **practical multimodal AI integration**.

---

## Example Output

**Image 1**

* **BLIP Caption:** “an elephant standing in the dirt near a body of water”
* **VQA Answers:**

  * Q1: What is in the image? → A1: elephant (Confidence: 0.97)
  * Q3: What is happening? → A3: bathing (Confidence: 0.19)

**Image 3**

* **BLIP Caption:** “a tiger walking through the woods”
* **VQA Answers:**

  * Q1: What is in the image? → A1: zebra (Confidence: 0.79)
  * Q3: What is happening? → A3: walking (Confidence: 0.23)

> The combination of captions and VQA answers provides a **comprehensive view** of the image, demonstrating both general understanding and targeted reasoning.

### Why Captions and VQA Answers Differ 
> BLIP captions provide a general, descriptive overview of the image, focusing solely on visual content, which is why they are often accurate and coherent. In contrast, the VQA model answers specific questions, reasoning over both the image and the text, which can sometimes lead to misclassifications or low-confidence answers for complex scenes. Combining both highlights your multimodal AI skills: BLIP gives context, while VQA delivers targeted reasoning, showcasing a professional and practical implementation.
---

## Tech Stack

* **Python 3.x**
* **Jupyter Notebook**
* **PyTorch**
* **Hugging Face Transformers** (`BLIP` & `ViLT`)
* **Pillow** (Image handling)
