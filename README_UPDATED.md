# NBA Game Prediction Model 🏀

A machine learning project that predicts the outcomes of future NBA games based on historical box score data. This repository contains the data processing pipeline, feature engineering scripts, and model training logic used to power the prediction engine.

**Live Demo:** [nba-prediction-project.up.railway.com](https://nba-prediction-project.up.railway.com)

## 🚀 Features

*   **Data Extraction:** Parses thousands of historical NBA box score HTML files using `BeautifulSoup`.
*   **Feature Engineering:** Calculates rolling averages, team efficiency metrics, and advanced stats (e.g., Pace, offensive/defensive ratings).
*   **Machine Learning:** Uses `scikit-learn` (Ridge Classification) to predict game winners based on past performance.
*   **Backtesting:** Includes a robust backtesting framework to evaluate model accuracy across different seasons.
*   **Automated Updates:** (In Progress) Scripts to fetch daily games and update predictions automatically.

## 🛠️ Tech Stack

*   **Language:** Python 3.10+
*   **Libraries:** Pandas, NumPy, Scikit-learn, BeautifulSoup4
*   **Deployment:** Railway (Web App), Docker (Containerization)
*   **Data Source:** Basketball-Reference.com (Html scrapes)

## 📂 Project Structure

*   `get_data.py`: Scripts to scrape and download raw HTML box scores.
*   `parse_data.py`: Extracts structured data from HTML into Pandas DataFrames.
*   `model.py`: Training logic, feature selection, and prediction generation.
*   `app/`: (If applicable) Django/Flask web application code.

## 📈 Performance

The current model achieves approximately **64% accuracy** on historical test data.

## 🔧 Installation & Usage

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/n2pium/NBAgame-prediction.git
    cd NBAgame-prediction
    ```

2.  **Install dependencies:**
    ```bash
    pip install -r requirements.txt
    ```

3.  **Run the data processor:**
    ```bash
    python parse_data.py
    ```

4.  **Train the model:**
    ```bash
    python model.py
    ```

## 🔮 Future Improvements

*   Integrate player-level injury data for more accurate predictions.
*   Implement a neural network (PyTorch/TensorFlow) to capture non-linear relationships.
*   Automate daily data fetching via GitHub Actions.

## 🤝 Contributing

Contributions are welcome! Please open an issue or submit a pull request.

## 📄 License

MIT License
