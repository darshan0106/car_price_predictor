# Car Price Predictor

An end-to-end Machine Learning project that predicts the selling price of a used car based on key features such as brand, fuel type, mileage, engine CC, and more.
The project includes:

* A **Jupyter Notebook** for data cleaning, preprocessing, model training, and model export using Pickle.
* A **Streamlit web app** where users can interactively input car details and get price predictions.

---

## ⭐ Features

* Cleaned and preprocessed the raw dataset (removed missing values, duplicates, and irrelevant columns).
* Extracted car brand names and encoded categorical features.
* Trained a **Linear Regression** model using Scikit-Learn.
* Deployed a user-friendly **Streamlit** interface for prediction.
* Saved and loaded the trained model using **Pickle**.

---

## 🧠 Tech Stack

### Backend / ML

* Python
* Pandas
* NumPy
* Scikit-Learn
* Pickle

### Frontend / UI

* Streamlit

---

## 📘 Dataset Info

The dataset used (`Cardetails.csv`) contains the following major columns:

* `name`
* `year`
* `km_driven`
* `fuel`
* `seller_type`
* `transmission`
* `owner`
* `mileage`
* `engine`
* `max_power`
* `seats`
* `selling_price` *(target)*

Certain columns like **torque** are removed during preprocessing.

---

## 🔧 Model Training Pipeline

1. **Load and clean dataset**

   * Remove missing values & duplicates.
   * Drop irrelevant columns.
   * Convert text-based fields (e.g., mileage, max_power, engine) into numeric.

2. **Encode categorical values**

   * Car brand → numerical label
   * Fuel type, seller type, transmission, owner → numerical encoding

3. **Split the dataset**

   ```
   train_test_split(test_size=0.2)
   ```

4. **Train Linear Regression model**

5. **Predict and evaluate model performance**

6. **Export model**

   ```python
   pk.dump(model, open('model.pkl', 'wb'))
   ```

---

## 🚀 How to Run the Project

### 1. Install Dependencies

```bash
pip install pandas numpy scikit-learn streamlit
```

### 2. Run the Streamlit App

```bash
streamlit run app.py
```

### 3. Access the Web App

Open the URL displayed in the terminal (usually):

```
http://localhost:8501/
```

---

## 📂 Project Structure

```
│── Car Price Predictor.ipynb        # Jupyter notebook for training
│── app.py                           # Streamlit application
│── model.pkl                        # Trained ML model
│── Cardetails.csv                   # Dataset
│── README.md                        # Project documentation
```

---

## 🧪 Usage Instructions

1. Launch the Streamlit app.
2. Select or enter car details:

   * Brand
   * Manufacturing year
   * Kilometers driven
   * Fuel type
   * Transmission type
   * Seller type
   * Owner type
   * Mileage
   * Engine CC
   * Max Power
   * Seats
3. Click **Predict** to view the estimated price.

---

## 🔮 Future Improvements

* Use **advanced ML models** (Random Forest, XGBoost, Gradient Boosting).
* Implement **feature scaling** for better performance.
* Add **visualizations** and model performance metrics in the UI.
* Improve dataset size and accuracy.
* Deploy the app on **Streamlit Cloud / Render / Heroku**.

---

## 📜 License

This project is free to use for learning and academic purposes.
