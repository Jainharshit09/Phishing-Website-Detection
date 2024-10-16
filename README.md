# Phishing Website Detection

This project focuses on detecting phishing websites by extracting and analyzing key URL-based features. Using data from PhishTank and legitimate sources, several machine learning models were applied to classify URLs as phishing or legitimate.

## Feature Extraction

### Address Bar Based Features
- Domain of the URL
- IP Address in URL
- "@" Symbol in the URL
- Length and Depth of the URL
- Redirection using "//"
- Use of "http/https" in the domain name
- URL Shortening Services (e.g., TinyURL)
- Prefix or Suffix "-" in the domain

### Domain Based Features
- DNS Record Status
- Website Traffic
- Age of the Domain
- Expiration Period of the Domain

### HTML & JavaScript Based Features
- IFrame Redirection
- Status Bar Customization
- Disabling Right-Click Functionality
- Website Forwarding

## Dataset
- **Phishing URLs:** Collected from PhishTank
- **Legitimate URLs:** Gathered from trusted sources
- **Format:** CSV files containing labeled URLs

## Model Performance

| ML Model                  | Train Accuracy | Test Accuracy |
|---------------------------|----------------|---------------|
| Decision Tree             | 0.814          | 0.818         |
| Random Forest             | 0.823          | 0.826         |
| Multilayer Perceptrons    | 0.870          | 0.863         |
| XGBoost                  | 0.872          | 0.862         |
| SVM                       | 0.808          | 0.817         |

### Top Models
- **Multilayer Perceptrons:** 86.3% Test Accuracy
- **XGBoost:** 86.2% Test Accuracy

## Project Structure
- **dataset/:** Contains CSV files with phishing and legitimate URLs
- **results/:** Evaluation metrics and graphs

## How to Use
1. Place phishing and legitimate URLs in the `data/` folder.
2. Extract features based on the categories outlined above.
3. Train and evaluate the models using the extracted features.
4. Use the performance metrics to identify the best model for deployment.

## Dependencies
- Python 3.x
- Pandas, NumPy
- scikit-learn, XGBoost
- XML API access for domain features

## Contributions
Contributions are welcome! Feel free to raise an issue or submit a pull request to improve the project.

## License
This project is licensed under the MIT License.
