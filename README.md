
# 🌦️ Rainfall Prediction Web App

This Flask-based web application predicts whether it will rain or not based on various weather-related inputs. It uses a pre-trained machine learning model (`cat.pkl`) to provide predictions and renders appropriate result pages based on the output.

---

## 🚀 Features

- Accepts weather inputs like temperature, humidity, wind speed, cloud cover, etc.
- Extracts date components (day and month) for temporal features.
- Sends the input to a CatBoost model (`cat.pkl`) for prediction.
- Renders a different HTML page based on prediction:
  - `after_sunny.html` if no rain is predicted.
  - `after_rainy.html` if rain is predicted.

---

## 🛠️ Tech Stack

- **Flask**: Web framework
- **HTML templates**: `index.html`, `predictor.html`, `after_sunny.html`, `after_rainy.html`
- **Model**: Pre-trained CatBoost model (`cat.pkl`)
- **Libraries**: `pandas`, `numpy`, `datetime`, `pickle`

---

## 📄 File Structure

```
project/
│
├── models/
│   └── cat.pkl               # Pre-trained ML model
├── template/
│   ├── index.html            # Home page
│   ├── predictor.html        # Input form
│   ├── after_sunny.html      # Output page (no rain)
│   └── after_rainy.html      # Output page (rain)
├── app.py                    # Flask backend logic
```

---

## 🧪 How to Run

1. **Clone the repository**

```bash
git clone <repo_url>
cd project
```

2. **Install dependencies**

```bash
pip install flask pandas numpy scikit-learn flask-cors
```

3. **Place the model**

Ensure the `cat.pkl` model file is inside the `models/` directory.

4. **Run the app**

```bash
python app.py
```

5. **Visit in browser**

Navigate to `http://127.0.0.1:5000/`

---

## 📥 Inputs Required

- Date (YYYY-MM-DD)
- Min/Max Temperature
- Rainfall, Evaporation, Sunshine
- Wind speeds and directions (9am/3pm)
- Humidity (9am/3pm)
- Pressure (9am/3pm)
- Cloud cover (9am/3pm)
- Rain Today (0 or 1)
- Location (as float-encoded value)
