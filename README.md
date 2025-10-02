# 🎨 Image to HTML/CSS Converter

This project is a web application that converts a visual design mockup, screenshot, or wireframe into functional HTML and CSS code. It leverages Google's Gemini API to analyze the input image and generate the corresponding front-end code. Users can also upload their own images to replace placeholders in the generated template, allowing for quick and dynamic prototyping. The application is built with Python and features an interactive web interface powered by Gradio.



## ✨ Features

* **AI-Powered Code Generation**: Utilizes the multimodal capabilities of the Gemini API to interpret visual designs and generate code.
* **Placeholder Replacement**: Supports up to five user-uploaded images to replace standard placeholders (`placeholder1.jpg`, `image2.jpg`, etc.) in the generated HTML.
* **Live Preview**: Instantly renders the generated HTML and CSS for immediate visual feedback.
* **Code Separation**: Provides distinct output fields for the generated HTML and CSS, making it easy to copy and use.
* **Interactive UI**: A simple and intuitive interface built with Gradio for uploading images and viewing results.

***

## ⚙️ How It Works

1.  The user uploads a **template image** (e.g., a screenshot of a website).
2.  Optionally, the user uploads up to five **content images**.
3.  The template image is sent to the Gemini API with a prompt instructing it to create responsive HTML and CSS code that matches the design.
4.  The application receives the model's response, which contains the code formatted in markdown.
5.  Regular expressions are used to **extract the HTML and CSS code** from the response text.
6.  The user's content images are converted to **base64 data URIs** and are used to replace the placeholder `src` attributes in the HTML.
7.  The final HTML and CSS are displayed in separate code blocks, and a combined version is rendered as a live **preview** within the Gradio interface.

***

## 📦 Dependencies

* [google-generativeai](https://pypi.org/project/google-generativeai/): The official Google client library for the Gemini API.
* [Gradio](https://pypi.org/project/gradio/): To create the web-based user interface.
* [Pillow](https://pypi.org/project/Pillow/): For image processing.
* [python-dotenv](https://pypi.org/project/python-dotenv/): To manage environment variables.
