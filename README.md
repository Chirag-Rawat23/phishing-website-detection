# Detection of Phishing Websites

Flask web app that predicts whether a given URL is phishing or legitimate using a Gradient Boosting model and handcrafted URL/content features.

## Features
- URL classification with probability score (safe vs phishing)
- Web UI for manual URL checks
- CSV upload and preview for batch inspection

## Tech Stack
- Python, Flask
- scikit-learn, numpy, pandas
- BeautifulSoup, requests, whois, googlesearch

## Model Info
- Algorithm: Gradient Boosting Classifier
- Training Accuracy: 0.989
- Test Accuracy: 0.974

## Project Structure
- `app.py` Flask application and routes
- `feature.py` feature extraction for URL analysis
- `model.pkl` trained model
- `templates/` HTML templates
- `static/` CSS/JS/assets
- `test_data/` sample data (if needed)
- `upload.csv` sample upload file

## Setup
1. Create and activate a virtual environment (recommended).
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Run
```bash
python app.py
```
Then open `http://127.0.0.1:5000` in your browser.

## Usage
- **Home**: `http://127.0.0.1:5000/`
- **URL Check**: open `http://127.0.0.1:5000/index`, submit a URL, view result on `/posts`
- **CSV Upload**: open `http://127.0.0.1:5000/upload` and upload a CSV to preview on `/preview`

## Notes
- The app runs in debug mode by default (`app.run(debug=True)`).
- Feature extraction uses live HTTP requests; some URLs may block requests or respond slowly.

## License
Add a license file if you plan to make this repository public.
