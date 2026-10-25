# Digital Shadow Risk Score

An AI-powered cybersecurity project designed to help users understand digital privacy risks and identify potentially phishing URLs using machine learning.

## About the Project

Digital Shadow Risk Score aims to improve digital safety awareness by helping users assess online risks and recognize suspicious URLs. The project combines a digital risk assessment interface with a machine-learning-based phishing URL classifier.

## Key Features

- **Digital Risk Assessment:** Helps users understand potential digital privacy and security risks.
- **Phishing URL Detection:** Classifies URLs as legitimate or potentially phishing-related using a trained machine learning model.
- **Risk Results:** Presents classification results and risk-related information through a web interface.
- **Visual Analytics:** Includes dataset exploration charts and model evaluation results.
- **Web Interface:** Built using Flask, HTML, CSS, and JavaScript.

## Machine Learning Approach

The phishing URL detection component uses a Character n-gram Linear Support Vector Machine (Linear SVM).

The model was trained and evaluated using a cleaned, balanced dataset containing 100,000 records, with 50,000 records in each class.

### Model Performance

| Evaluation Metric | Result |
|---|---:|
| Accuracy | 97.87% |
| Phishing Precision | 98.26% |
| Phishing Recall | 97.47% |
| Phishing F1-score | 97.86% |

These results were obtained on a held-out test set of 20,000 records. They do not guarantee the same performance on unseen, real-world URLs. The model also reached its configured iteration limit during training, which should be considered when interpreting the results.

## Technologies Used

- Python
- Flask
- Scikit-learn
- Pandas and NumPy
- HTML, CSS, and JavaScript
- Matplotlib
- Jupyter Notebook

## Project Structure

- `website/` — Flask application, templates, stylesheets, JavaScript, and launcher.
- `Final/` — cleaned dataset, model training script, saved model, evaluation results, and visualizations.
- `notebooks/` — notebook explaining the final model and its evaluation.
- `render.yaml` — deployment configuration for Render.
- `README.md` — project documentation.

## Running the Website Locally

1. Install Python.
2. Install the website dependencies:

   `python -m pip install -r website/requirements.txt`

3. Start the application:

   `python website/app.py`

4. Open the local address displayed in the terminal in your web browser.

Keep the `Final` and `website` folders in their original relative locations so the application can locate the saved model.

## Team Project

This project was developed as a group project. Team members and their respective contributions should be credited in this repository.

## Disclaimer

This project is intended for educational and cybersecurity awareness purposes. Its results should not be treated as a guarantee that a URL is safe or malicious. Always exercise caution when visiting unfamiliar websites.

## Future Improvements

- Expand evaluation using additional, independent datasets.
- Improve model convergence and test generalization on unseen URLs.
- Enhance digital privacy risk assessment and user guidance.
- Improve the web interface and deployment experience.

