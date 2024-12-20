# Simple Machine Learning Model Web Application

## Project Overview
This Django-based web application integrates a machine learning model to make predictions based on user input. The application includes features for:

- **Making Predictions**: Users can input a value, and the app predicts the outcome using the trained model.
- **Saving Predictions**: Each input and its corresponding prediction are stored in the database.
- **Admin Interface**: Manage stored predictions via the Django admin panel.
- **Visual Effects**: Unique animations (e.g., confetti drop) enhance the user experience after predictions.

## Features
1. **Interactive Input**:
   - Users can provide numerical input via a user-friendly web form.
2. **Prediction Storage**:
   - Each prediction is stored in the default SQLite database along with a timestamp.
3. **Admin Management**:
   - Admins can view, edit, or delete saved predictions.
4. **User Interface**:
   - A table displays all saved predictions.
   - Animations make the experience visually engaging.

## Project Structure
```
ml_dir/
├── db.sqlite3                # SQLite database file
├── manage.py                 # Django management script
├── ml_app/                   # Django app folder
│   ├── admin.py              # Admin interface configuration
│   ├── apps.py               # App configuration
│   ├── ml_model.py           # Machine learning model utilities
│   ├── model.pkl             # Serialized ML model
│   ├── models.py             # Database models
│   ├── templates/            # HTML templates
│   │   ├── index.html        # Input form and prediction page
│   │   ├── view_predictions.html # Display saved predictions
│   ├── urls.py               # URL routing
│   ├── views.py              # Core application logic
├── ml_pro/                   # Project configuration folder
    ├── settings.py           # Project settings
    ├── urls.py               # Project-level URL routing
```

## Setup Instructions

### Prerequisites
Ensure the following are installed:
- Python 3.8+
- Django 4.0+
- Required Python libraries (listed in `requirements.txt`)

### Installation Steps
1. **Clone the repository**:
   ```bash
   git clone <repository_url>
   cd ml_dir
   ```

2. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Apply migrations**:
   ```bash
   python manage.py migrate
   ```

4. **Run the server**:
   ```bash
   python manage.py runserver
   ```

5. **Access the app**:
   Open [http://127.0.0.1:8000/](http://127.0.0.1:8000/) in your web browser.

## Usage Guide

### Making Predictions
1. Navigate to the app's main page.
2. Enter a value in the input field and click "Predict".
3. View the predicted value and enjoy the animation.

### Viewing Saved Predictions
1. Navigate to the "Saved Predictions" page.
2. View the table displaying input values, predictions, and timestamps.

### Admin Interface
1. Log in to the Django admin panel at `/admin/`.
2. Manage stored predictions in the "Predictions" section.

## Animations
- **Confetti Drop**: Triggered after a prediction is made.
- **Styling Enhancements**: Parallax and glassy background effects.

## Technologies Used
- **Django Framework**: For backend and database management.
- **SQLite**: For data storage.
- **Pickle**: For model serialization.
- **HTML/CSS**: For frontend design.
- **JavaScript**: For animations and interactivity.

## Customization
1. **Replace the ML Model**:
   - Update the `model.pkl` file with your trained model.
2. **Enhance Animations**:
   - Modify the JavaScript in `index.html` for custom effects.
3. **Database Management**:
   - Configure a different database in `settings.py`.

## Future Improvements
- Add user authentication.
- Integrate more advanced ML models.
- Provide detailed prediction analytics.

## License
This project is licensed under the MIT License.

---
Enjoy building and extending this application!

