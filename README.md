# Phishing URL Detection with Machine Learning and Streamlit

This project leverages advanced machine learning techniques to detect phishing URLs with high precision. Utilizing a state-of-the-art Streamlit app, users can effortlessly input a URL and receive an immediate prediction on its legitimacy. The solution incorporates robust feature extraction from URLs and is fine-tuned with Optuna for optimal performance.

---

## Installation

To set up the project locally, please follow these steps:

1. **Clone the repository:**

   ```bash
   git clone https://github.com/yourusername/your-repo-name.git
   ```

2. **Navigate to the project directory:**

   ```bash
   cd your-repo-name
   ```

3. **Create a virtual environment (optional but recommended):**

   ```bash
   python -m venv venv
   ```

4. **Activate the virtual environment:**

   - **On Windows:**

     ```bash
     venv\Scripts\activate
     ```

   - **On macOS/Linux:**

     ```bash
     source venv/bin/activate
     ```

5. **Install dependencies:**

   ```bash
   pip install -r requirements.txt
   ```

> **Note:** Ensure you have Python 3.8+ installed, as some dependencies (e.g., Streamlit) may require it.

---

## Usage

To operate the Streamlit app, proceed as follows:

1. **Launch the app:**

   ```bash
   streamlit run app.py
   ```

2. **Access the app:**

   Open your web browser and navigate to [http://localhost:8501](http://localhost:8501).

3. **Check a URL:**

   - Enter a URL in the input field provided.
   - Click the **"Check"** button to receive the prediction (e.g., "Phishing" or "Legitimate").

---

## Model Details

The machine learning model employed is a **[insert model type, e.g., Random Forest Classifier]**. It is trained on a comprehensive dataset of labeled URLs (phishing and legitimate) with extracted features. Hyperparameter optimization is performed using **Optuna** to enhance predictive performance.

---

## Performance Metrics

- **Accuracy: 94.79** 
- **Precision: 0.94**
- **Recall:0.96** 
- **F1 Score:0.95** 

---

## Feature Extraction

The model assesses phishing URLs based on the following features:

- Length of the URL
- Length of the hostname
- Presence of an IP address in the hostname
- Number of dots in the URL
- Number of question marks in the URL
- Number of equal signs in the URL
- Number of slashes in the URL
- Presence of "www" in the URL
- Ratio of digits in the URL
- Ratio of digits in the hostname
- Presence of top-level domain in the subdomain
- Presence of prefix or suffix in the hostname (e.g., "-")
- Length of the shortest word in the hostname
- Length of the longest word in the URL
- Length of the longest word in the path
- Presence of phishing-related keywords (e.g., "secure", "account", "update", "login")
- Number of hyperlinks (if applicable)

For detailed implementation, please refer to the `extract_features` function in `app.py`.

---

## Contributing

We welcome contributions to further enhance this project. To contribute:

- **Report Issues:** Use the GitHub Issues page to report bugs or suggest enhancements.
- **Submit Pull Requests:** Fork the repository, implement your changes, and submit a pull request with a comprehensive description of your updates.
- **Coding Standards:** Adhere to PEP 8 guidelines for Python code.

---

## License

This project is licensed under the **MIT License**. Please refer to the [LICENSE](LICENSE) file for complete details.

---

## Additional Notes

- Replace `yourusername` and `your-repo-name` with your actual GitHub username and repository name.
- Update the model type and performance metrics based on your specific project details.
- Ensure that a `requirements.txt` file is present with all dependencies (e.g., Streamlit, scikit-learn, Optuna, etc.). You can generate it using:
  
  ```bash
  pip freeze > requirements.txt
  ```

- If you opt for a different license, update the "License" section accordingly and include the appropriate LICENSE file.

---

This README.md offers a comprehensive, professional overview of the project, designed to maximize clarity and engagement with GitHub users. Let's innovate and drive success in the cybersecurity space!