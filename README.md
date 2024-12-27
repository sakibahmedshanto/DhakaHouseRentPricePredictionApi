# House Rent Price Prediction API

A **Flask-based API** to predict house rental prices using a machine learning model trained on a **home rental price dataset**. The API takes location, area, and property details as input and predicts the monthly rental price in Bangladeshi Taka (BDT).

![Python](https://img.shields.io/badge/Python-3.10-blue?style=flat&logo=python&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-2.0.3-black?style=flat&logo=flask&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-1.4.3-blue?style=flat&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-1.22.4-lightgrey?style=flat&logo=numpy&logoColor=white)

---

## Features
- **POST API endpoint** to predict house rent prices.
- Utilizes **Pandas** and **NumPy** for data handling.
- Deployed on **Render** for easy access.

---

## Tech Stack
- **Backend**: Flask
- **Data Processing**: Pandas, NumPy
- **Deployment**: Render

---

## API Endpoint
The API is live at: [https://houserentprice.onrender.com/](https://houserentprice.onrender.com/predict)

---

## Request & Response

### 1. Input
Send a **POST** request with JSON input containing the following fields:

```json
{
  "Location": "Block H, Bashundhara R-A, Dhaka",
  "Area": 1600,
  "Bed": 2,
  "Bath": 3
}
```

### 2. Output
The API responds with the **predicted rental price** in Bangladeshi Taka (BDT):

```json
{
  "predicted_price_in_taka": 43019.38
}
```

---

## Example Usage

You can test the API using tools like **cURL**, **Postman**, or Python's `requests` library.

### cURL Example:
```bash
curl -X POST https://houserentprice.onrender.com/ \
     -H "Content-Type: application/json" \
     -d '{"Location": "Block H, Bashundhara R-A, Dhaka", "Area": 1600, "Bed": 2, "Bath": 3}'
```

### Python Example:
```python
import requests

url = "https://houserentprice.onrender.com/predict"
data = {
    "Location": "Block H, Bashundhara R-A, Dhaka",
    "Area": 1600,
    "Bed": 2,
    "Bath": 3
}
response = requests.post(url, json=data)
print(response.json())
```

### Response:
```json
{
  "predicted_price_in_taka": 43019.38
}
```


---

## Deployment
Deployed using [Render](https://render.com/).

---

## Contributing
Feel free to fork the repository, create a new branch, and submit a pull request to enhance the project.

---

## License
This project is licensed under the MIT License. See the `LICENSE` file for details.

---

## Acknowledgments
- Kaggle for providing the dataset.
- Flask, Pandas, and NumPy for powering the project.

---

*Created with ❤️ by [Sakib Ahmeed Shanto](https://github.com/sakibahmedshanto)*
