<a id="readme-top"></a>

<h1 align="center">Emotion-Aware Music System⁠</h1>

<p align="center">
 AI-powered system that detects emotions from text and selects music based on user mood.
</p>
<p align="center">
  <img src="https://img.shields.io/badge/Python-3.10-F472B6" />
  <img src="https://img.shields.io/badge/Task-Emotion%20Analysis-FBBF24" />
  <img src="https://img.shields.io/badge/Model-Logistic%20Regression-60A5FA" />
  <img src="https://img.shields.io/badge/Framework-Flask-22C55E" />
  <img src="https://img.shields.io/badge/Domain-NLP-A78BFA" />
</p>
</br>

## Table of Contents

1. [Overview](#overview)  
2. [Application Screenshots](#application-screenshots)  
3. [Key Features](#key-features)  
4. [Getting Started](#getting-started)  
   - [Prerequisites](#prerequisites)  
5. [Usage](#usage)  
6. [Technical Details](#technical-details)  
   - [Dependencies](#dependencies)  
   - [Dataset & Model](#dataset--model)  
   - [Model Insights](#model-insights)  
   - [Supporting Files](#supporting-files)  
7. [Folder Structure](#folder-structure)  
8. [License](#license)

<p align="right">(<a href="#readme-top">back to top</a>)</p>
<br>

## Overview

**Emotion-Aware Music System** is an NLP-based system designed to detect emotions from text and select music based on user mood.  
The system uses a **pretrained emotion classification model** and provides a simple **Flask-based interface**.

Users simply enter a sentence, and the system:
- Detects the **emotion** (e.g., happy, sad, angry).
- Selects **music tracks** that match the detected mood.

<p align="right">(<a href="#readme-top">back to top</a>)</p>
<br>

## Application Screenshots

<p align="center">
  <img src="static/homepage.png" alt="Homepage" width="700"/>
  <br>
  <em>Homepage – Users can input a sentence to analyze their emotion and get music recommendations.</em>
</p>
<br>
<p align="center">
  <img src="static/results.png" alt="Prediction Result Page" width="700"/>
  <br>
  <em>Result Page – Displays predicted emotion and selected music based on the input text.</em>
</p>
<br>
<p align="right">(<a href="#readme-top">back to top</a>)</p>
<br>


## Key Features

| **Functionality**             | **Details** |
|-------------------------------|-------------|
| **Emotion Detection**         | Predicts emotions from user-provided text using a trained NLP model. |
| **Emotion-Based Music Selection** | Selects music tracks based on detected emotions. |
| **Web Interface**             | User-friendly Flask interface for input and results display. |
| **Pretrained Models**         | Uses `emotion_model.pkl` and `label_encoder.pkl` for emotion classification. |
| **Lightweight Setup**         | No heavy GPU requirements, runs smoothly on CPU. |

<p align="right">(<a href="#readme-top">back to top</a>)</p>
<br>


## Getting Started

To run the system locally, follow these steps:

- Make sure Python 3.10 or later is installed.  
- Ensure `pip` package manager is available.

<br>

### Prerequisites

Install the dependencies from `requirements.txt`:
```bash
pip install -r requirements.txt
```

<p align="right">(<a href="#readme-top">back to top</a>)</p>
<br>


## Usage

1. **Clone the repository and install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

2. **Run the Flask system:**
   ```bash
   python app.py
   ```

3. **Stop the server at any time:**
   ```bash
   CTRL+C
   ```

Then visit **http://127.0.0.1:5000** in your browser.

<p align="right">(<a href="#readme-top">back to top</a>)</p>
<br>


## Technical Details

### Dependencies

This project relies on the following Python libraries:

- Flask  
- scikit-learn  
- numpy  
- pandas  
- pickle  

> Tested on Python 3.10 with Flask 2.3.2

<p align="right">(<a href="#readme-top">back to top</a>)</p>
<br>


### Dataset & Model

The emotion classification is powered by the **Kaggle Emotions Dataset for NLP**, which contains text samples labeled with 6 emotion categories:

```
['joy', 'sadness', 'anger', 'fear', 'love', 'surprise']
```
<br>

**Model Pipeline:**
- **Text Vectorization:** TF-IDF (ngram_range=(1,2), max_features=10,000)
- **Classifier:** Logistic Regression
- **Artifacts:** `emotion_model.pkl` and `label_encoder.pkl`

Basic dataset analysis includes label distribution and text characteristics.

> **Kaggle Notebook:** [Emotion Classification from Text using Supervised](https://www.kaggle.com/code/caglakacar/emotion-classification-from-text-using-supervised)

<p align="right">(<a href="#readme-top">back to top</a>)</p>
<br>


## Model Insights

#### Label Distribution

<p align="center">
  <img src="static/label-distribution.png" alt="Label Distribution" width="500"/>
</p>
<br>

#### Confusion Matrix

<p align="center">
  <img src="static/confusion-matrix.png" alt="Confusion Matrix" width="500"/>
</p>
<br>

#### Sentence Length Distribution

<p align="center">
  <img src="static/sentence-length-distribution.png" alt="Sentence Length Distribution" width="500"/>
</p>

<p align="right">(<a href="#readme-top">back to top</a>)</p>
<br>


### Supporting Files

- **emotion_model.pkl:** Pretrained emotion classification model.  
- **label_encoder.pkl:** Label encoder mapping class IDs to emotion strings.  
- **requirements.txt:** List of required Python packages.  
- **favicon.png:** App icon used in the interface.  

<p align="right">(<a href="#readme-top">back to top</a>)</p>
<br>


## Folder Structure
```
Emotion-Aware-Music-System/
│
├── app.py                       
├── emotion_model.pkl            
├── label_encoder.pkl            
├── templates/
│   └── index.html               
├── static/
│   └── favicon.png              
├── requirements.txt             
```

<p align="right">(<a href="#readme-top">back to top</a>)</p>
<br>


## License

This project is licensed under the MIT License.  
See the [LICENSE](LICENSE) file for details.

<p align="right">(<a href="#readme-top">back to top</a>)</p>
