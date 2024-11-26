A Report

On

**Assignment\_1**

# **(**Rare-Human Action Video Generator**)**

BY

**Team 7**

	

**Bhanu Chand Pothina \- SE21UARI024**

**Harsha Vardhan Reddy Ailuri \- SE21UARI043**

**Heshika Pokala \- SE21UARI050**

**Vasundhara Kandadi \- SE21UARI062**

**CS 4124 : AI in Industry 4.0**

**BY**

**Lecturer: Meg Rajendran** 

**Teaching Assistant: Dhathri Meda**


## *About*

This project provides a pipeline to upload videos, generate captions for human actions, and produce rare-human synthetic action videos using AI models.

## **Overview**

This tool allows users to:

* Upload input videos.  
* Generate descriptive captions for the actions in the videos.  
* Create synthetic human action videos with captions overlayed for demonstration purposes.

## **Features**

* Gradio-powered user interface for ease of use.  
* Automated video captioning with the BLIP model.  
* Synthetic video generation using open-source AI models.  
* Side-by-side comparison of input and generated videos.

		

## 

## 

## *Installation*

**Step 1: Clone the Repository**

*git clone (https://github.com/UnknOwn23504/Rare-human-action-generator)*

*cd rare-human-action-generator*

**Step 2: Set Up the Environment**

*pip install gradio moviepy transformers torch torchvision torchaudio \-q*

*pip install git+https://github.com/openai/CLIP.git \-q*

**Step 3: Set Up the SORA Model**

*git clone https://github.com/lyogavin/train\_your\_own\_sora.git sora\_model*

*cd sora\_model*

*pip install \-r requirements.txt*

*cd ..*

## *Usage*

**Step 1: Launch the Interface**

Run the Python code to start the Gradio interface:

*python app.py*

### **Step 2: Use the Interface**

* Upload an input video (drag and drop or select a file).  
* Click "Submit" to process the video.  
* View the results:  
  * **Input Video**: The original uploaded video.  
  * **Generated Video**: The output video with captions overlayed.  
  * **Generated Captions**: A textual description of the video's content.


## *Demo*

**Check out the demo video showcasing the interface and outputs: (https://youtu.be/UqLKl37R1Xc))**
