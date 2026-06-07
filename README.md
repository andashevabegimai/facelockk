# facelockk

FaceLock Image Protection and Evaluation


Overview
This project demonstrates the use of FaceLock to protect facial images from unauthorized AI-based editing and identity manipulation.

The workflow includes:
Uploading a facial image.
Applying FaceLock protection.
Generating edited versions using text prompts.
Measuring image quality degradation.
Evaluating identity preservation using face embeddings.


Features:
Active Defense:Adds hidden noise (ε  = 0.08) to the image. This noise confuses AI models but keeps the photo looking normal to humans.
Testing: The script tries to edit both the original and the protected image to show the difference.
-Biometric Verification: Uses the ArcFace model to compare the original photo with the edited one. If the difference score (cosine distance) is over 0.68, the system confirms that the identity is successfully protected.
AI Judge Verification: Uses the Gemini API as an automated judge to evaluate the results of the editing attacks. Combined with ArcFace, this creates a strict dual-check system for the defense.

Installation
Clone FaceLock:
git clone https://github.com/taco-group/FaceLock.git
cd FaceLock

Install dependencies:
pip install -r requirements.txt

How to run
1: API Keys Setup
1. Click the “Secrets” tab in Google Colab (the key icon on the left sidebar).
2. Add a secret named “HF_TOKEN” and paste your Hugging Face token.
3. Add a secret named “GEMINI_API_KEY” and paste your Gemini API key.
4. Turn on "Notebook access" for both secrets.
5. And there are some pictures to test with in "assets" folder

Dependencies
Main libraries:
transformers
diffusers
huggingface-hub
peft
accelerate
insightface
onnxruntime-gpu
opencv-python
lpips
deepface
numpy
scipy
matplotlib
pillow

This project relies on the FaceLock framework and follows the licensing terms of the original repository.
https://github.com/taco-group/FaceLock



