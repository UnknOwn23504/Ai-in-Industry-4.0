# Rare-Human Action Video Generator

## Overview

This repository contains a project that uses AI models to generate captions for input videos and create AI-synthesized videos based on those captions. This project integrates Gradio as an interface for uploading videos, generating captions, and displaying generated synthetic videos. The focus is on generating rare-human action videos, and the system leverages multiple cutting-edge machine learning models to accomplish this.

## Features
- **Video Captioning**: Extracts frames from an input video and uses the BLIP model to generate descriptive captions for the video content.
- **AI Synthetic Video Generation**: Uses AnimateDiff to create a synthetic video based on the generated captions.
- **Text Overlay on Input Video**: The generated captions are overlaid on the input video using OpenCV for easier visualization.
- **User-Friendly Gradio Interface**: The entire workflow can be accessed via a simple Gradio-based user interface.

## Requirements

To get started, you need to have the following installed:

- **Python 3.7+**
- **PyTorch** (with CUDA support if using GPU)
- **Packages**: Install all required Python packages using the command below:
  
  ```sh
  pip install gradio av torch transformers diffusers opencv-python-headless moviepy Pillow
  ```

Make sure your PyTorch installation supports GPU for faster processing, especially for video generation.

## Setup Instructions

1. **Clone the Repository**
   ```sh
   git clone <repository_url>
   cd <repository_folder>
   ```

2. **Install Dependencies**
   Install the required Python libraries by running:
   ```sh
   pip install -r requirements.txt
   ```

3. **Download Model Weights**
   - Model weights will be automatically downloaded when the script is run for the first time. Make sure you have a stable internet connection.
   - Pre-trained models used:
     - BLIP Model: `Salesforce/blip-image-captioning-base`
     - AnimateDiff Pipeline: `SG161222/Realistic_Vision_V5.1_noVAE`
     - Motion Adapter: `guoyww/animatediff-motion-adapter-v1-5-2`

4. **Run the Application**
   Start the Gradio interface by running:
   ```sh
   jupyter notebook AI_Video_Generator.ipynb
   ```

   The Gradio interface will be launched in your browser, allowing you to upload videos, view captions, and visualize the generated synthetic video.

## How It Works

1. **Upload a Video**: The user uploads an input video through the Gradio interface.
2. **Caption Generation**: The system extracts frames from the video and uses the BLIP model to generate captions summarizing the actions.
3. **AI Video Generation**: The generated caption is then passed to AnimateDiff, which creates an AI-generated video that visualizes the captioned action.
4. **Results Displayed**: The interface shows three outputs:
   - The original video with captions overlaid.
   - The generated captions in a text box.
   - The AI-generated synthetic video.

## Directory Structure

- **AI_Video_Generator.ipynb**: Contains the main script that runs the Gradio application.
- **uploaded_videos/**: Directory used to store uploaded videos.
- **generated_videos/**: Directory used to store generated synthetic videos.

## Example Use Cases
- Generating synthetic videos to visualize rare human actions for research or entertainment.
- Creating a dataset of synthetic action videos for machine learning model training or benchmarking.

## Gradio Interface
The Gradio interface allows easy interaction with the system:
- Upload an input video file.
- Click on **Generate** to process the video.
- The system generates captions and produces a synthetic video, displayed alongside the original.

## Models and Technologies Used
- **BLIP (Bootstrapping Language-Image Pre-training)**: Used for video captioning. It generates a natural language description of the actions present in the video.
- **AnimateDiff**: A video generation model used for synthesizing videos from textual descriptions, capable of generating realistic visual representations of actions.
- **Gradio**: A simple web UI for easy access and interaction.

## System Requirements
- **Hardware**: GPU with CUDA is highly recommended, as the AI video generation and captioning tasks can be computationally intensive.
- **Storage**: Ensure adequate disk space for storing model weights and generated videos.

## Future Enhancements
- **Enhanced Captioning**: Improve the captioning quality by experimenting with other pre-trained models.
- **Additional Controls**: Add more user controls for adjusting generation parameters like guidance scale, number of inference steps, etc.
- **Comparison**: Display a side-by-side comparison of the input and generated videos for better visualization.

## Troubleshooting
- **Slow Processing**: If the processing is slow, ensure you are running on a GPU-enabled machine.
- **Model Download Issues**: If model weights fail to download, ensure you have a stable internet connection and sufficient disk space.

## License
This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments
- Special thanks to [Hugging Face](https://huggingface.co/) for providing access to the pre-trained models.
- The [Gradio](https://gradio.app/) team for making web UI integration seamless.

Feel free to fork this project and contribute by submitting pull requests with enhancements or fixes.

