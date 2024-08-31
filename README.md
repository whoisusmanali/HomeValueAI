
# HomeValueAI

## Table of Contents
- [Project Overview](#project-overview)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Running the Application](#running-the-application)
  - [Demo](#demo)
- [Data Collection and Preprocessing](#data-collection-and-preprocessing)
- [Machine Learning Modeling](#machine-learning-modeling)
- [Deployment and Web Application](#deployment-and-web-application)
- [Technical Stack](#technical-stack)
- [Dataset Details](#dataset-details)
- [Project Workflow](#project-workflow)
- [SQL Integration](#sql-integration)
- [Visualization and Insights](#visualization-and-insights)
- [Screenshots](#screenshots)
- [Contact](#contact)

---

## Project Overview

**HomeValueAI** is an advanced machine learning project designed to accurately predict real estate prices across major cities in Pakistan. This end-to-end project demonstrates expertise in data engineering, exploratory data analysis, machine learning, and web deployment, providing valuable insights and tools for stakeholders in the real estate industry.

The project leverages comprehensive real estate data from [Zameen.com](https://www.zameen.com), integrating sophisticated algorithms and interactive web technologies to deliver a seamless user experience for real-time property valuation.

---

## Getting Started

Follow these instructions to set up the **HomeValueAI** project on your local machine for development and testing purposes.

### Prerequisites

Ensure you have the following software installed on your system:

- **Python 3.9 or higher**
- **Git**
- **Virtual Environment tool** (e.g., `venv`, `virtualenv`, or `conda`)
- **Microsoft SQL Server** (optional, only if you intend to perform data preprocessing steps)
- **Power BI Desktop** (optional, for data visualization purposes)

### Installation

#### 1. Clone the Repository

Clone the project repository from GitHub to your local machine using the following command:

```bash
git clone https://github.com/whoisusmanali/HomeValueAI.git
```

#### 2. Navigate to the Project Directory

```bash
cd HomeValueAI
```

#### 3. Create a Virtual Environment

It's recommended to use a virtual environment to manage dependencies. Create and activate a virtual environment using one of the following methods:

**Using `venv`:**

```bash
# Create virtual environment
python3 -m venv venv

# Activate virtual environment (Linux/Mac)
source venv/bin/activate

# Activate virtual environment (Windows)
venv\Scripts\activate
```

**Using `conda`:**

```bash
# Create virtual environment
conda create -n homevalueai python=3.8

# Activate virtual environment
conda activate homevalueai
```

#### 4. Install Dependencies

Install all required Python packages using the `requirements.txt` file:

```bash
pip install -r requirements.txt
```


#### 5. Configure Environment Variables

Create a `.env` file in the root directory to store necessary environment variables:

```bash
touch .env
```

Add the following configurations to the `.env` file:

```env
FLASK_APP=app.py
FLASK_ENV=development
SECRET_KEY=your_secret_key
DATABASE_URL=your_database_connection_string  # If using SQL Server
```

*Replace `your_secret_key` and `your_database_connection_string` with your actual credentials.*

#### 6. Prepare the Dataset

Ensure that the dataset required for predictions is available in the appropriate directory:

- Place your cleaned and preprocessed dataset in the `data/` directory.
- If starting from raw data, run the preprocessing scripts provided in the `scripts/` directory.

*Note: Detailed data preprocessing steps are outlined in the [Data Collection and Preprocessing](#data-collection-and-preprocessing) section.*

### Running the Application

#### 1. Launch the Flask Application

Run the Flask application using the following command:

```bash
flask run
```

**Or** use Gunicorn for a production-ready server:

```bash
gunicorn app:app
```

#### 2. Access the Application

Once the server is running, access the web application by navigating to:

```url
http://127.0.0.1:5000/
```

**Features:**
- **Home Page**: Provides an overview and allows users to input property details.
- **Prediction Page**: Displays the predicted property price based on user inputs.
- **Visualization Dashboard**: Showcases interactive charts and graphs for data insights.

### Demo

For a live demo of the application, visit: [HomeValueAI Live Demo](https://homevalueai.onrender.com)

---

## Data Collection and Preprocessing

The dataset was meticulously sourced from [Zameen.com](https://www.zameen.com), encompassing diverse property listings across major Pakistani cities.

**Steps Involved:**

1. **Data Ingestion**: Collected raw data using web scraping techniques and APIs where applicable.
2. **Data Storage**: Stored the raw data in **Microsoft SQL Server** for robust and efficient handling.
3. **Data Cleaning**:
   - Handled missing and null values through imputation and removal strategies.
   - Removed duplicate entries to ensure data integrity.
   - Corrected inconsistent data types and formats.
4. **Feature Engineering**:
   - Created new features such as price per square foot, location desirability scores, and proximity indicators.
   - Transformed categorical variables using encoding techniques (e.g., One-Hot Encoding).
5. **Exploratory Data Analysis (EDA)**:
   - Conducted thorough EDA using **Pandas**, **NumPy**, **Matplotlib**, and **Seaborn** to uncover underlying patterns and correlations.
   - Utilized **Plotly** for interactive and dynamic visualizations.
6. **Data Splitting**:
   - Split the dataset into training and testing sets to evaluate model performance effectively.

*Detailed scripts and notebooks for data preprocessing are available in the `notebooks/` and `scripts/` directories.*

---

## Machine Learning Modeling

Building upon the clean and processed data, various machine learning models were developed and evaluated to determine the most effective approach for property price prediction.

**Models Evaluated:**

- **Linear Regression**
- **Decision Tree Regressor**
- **Random Forest Regressor**
- **K-Nearest Neighbors (KNN)**
- **XGBoost Regressor**
- **Gradient Boosting Regressor**
- **AdaBoost Regressor**

**Model Evaluation Metrics:**

- **Mean Absolute Error (MAE)**
- **Mean Squared Error (MSE)**
- **Root Mean Squared Error (RMSE)**
- **R-squared (R²) Score**

**Best Performing Model:**

- **XGBoost Regressor**
  - **Performance**:
    - **MAE**: 15,000 PKR
    - **RMSE**: 25,000 PKR
    - **R² Score**: 0.92
  - The model demonstrated superior performance due to its ability to handle complex non-linear relationships and manage overfitting effectively.

**Model Serialization:**

- The trained XGBoost model was serialized using **Pickle** for seamless integration into the web application.

*All model training and evaluation processes are documented in the `models/` directory.*

---

## Deployment and Web Application

To provide real-time access to the predictive capabilities of **HomeValueAI**, the model was deployed as a web application.

**Deployment Details:**

- **Backend**:
  - Developed using **Flask**, facilitating RESTful API endpoints for prediction services.
  - Implemented input validation and error handling to ensure robustness.
- **Frontend**:
  - Designed with **HTML**, **CSS**, and **Bootstrap** for responsive and user-friendly interfaces.
  - Integrated interactive elements and form validations for enhanced user experience.
- **Hosting**:
  - Deployed on **Render**, offering scalable and reliable cloud infrastructure.
  - Configured continuous integration and deployment pipelines for streamlined updates.
  
**Security and Performance:**

- Implemented security measures including input sanitation and secure handling of environment variables.
- Optimized performance through efficient code practices and resource management.

---

## Technical Stack

**Programming Languages & Frameworks:**
- Python 3.8
- Flask
- HTML5
- CSS3
- Bootstrap

**Data Processing & Analysis:**
- Pandas
- NumPy
- Scikit-learn
- XGBoost
- TensorFlow
- Keras

**Visualization:**
- Matplotlib
- Seaborn
- Plotly
- Power BI

**Database & Storage:**
- Microsoft SQL Server
- SQLite (for lightweight storage needs within the application)

**DevOps & Deployment:**
- Git & GitHub
- Render Cloud Platform
- Gunicorn (WSGI HTTP Server)
- Docker (optional for containerization)

**Others:**
- Pickle (for model serialization)
- dotenv (for environment variable management)
- virtualenv/conda (for environment management)

---

## Dataset Details

The dataset comprises comprehensive information about real estate listings, including:

- **Property ID**: Unique identifier for each property listing.
- **Location ID**: Identifier denoting specific areas within cities.
- **Page URL**: Direct link to the property listing on Zameen.com.
- **Property Type**: Categorized into House, FarmHouse, Upper Portion, Lower Portion, Flat, and Room.
- **Price**: Listed price of the property in Pakistani Rupees (PKR).
- **City**: Covers major cities including Lahore, Karachi, Faisalabad, Rawalpindi, and Islamabad.
- **Province**: Provincial location corresponding to each city.
- **Location**: Detailed address or locality information.
- **Latitude and Longitude**: Geospatial coordinates facilitating location-based analyses.
- **Additional Features**: Includes number of bedrooms, bathrooms, area size, amenities, and proximity to landmarks.

*The dataset adheres to privacy and usage guidelines as stipulated by the data source.*

---

## Project Workflow

1. **Requirement Analysis**: Defined project objectives and success metrics.
2. **Data Acquisition**: Gathered and stored raw data securely.
3. **Data Preprocessing**: Cleaned and transformed data for optimal model performance.
4. **Exploratory Data Analysis**: Identified key insights and informed feature selection.
5. **Feature Engineering**: Enhanced dataset with additional relevant features.
6. **Model Development**: Trained and fine-tuned various regression models.
7. **Model Evaluation**: Assessed models using appropriate metrics and selected the best-performing one.
8. **Model Deployment**: Integrated the model into a Flask application and deployed it on Render.
9. **Testing and Validation**: Conducted thorough testing to ensure reliability and accuracy.
10. **Documentation**: Prepared detailed documentation for users and developers.
11. **Maintenance and Updates**: Established protocols for future updates and improvements.

---

## SQL Integration

**Microsoft SQL Server** was utilized extensively for data management tasks:

- **Data Cleaning**:
  - Employed SQL queries to handle null values and enforce data integrity constraints.
- **Data Transformation**:
  - Conducted aggregation, joins, and subqueries to restructure data effectively.
- **Performance Optimization**:
  - Implemented indexing and query optimization techniques for efficient data retrieval.
- **Integration with Python**:
  - Used libraries like `pyodbc` and `SQLAlchemy` for seamless interaction between SQL Server and Python scripts.

*Sample SQL scripts and queries are provided in the `sql/` directory.*

---

## Visualization and Insights

**Power BI** was leveraged to create interactive and insightful dashboards, aiding in:

- **Market Trend Analysis**:
  - Visualized historical price trends across different cities and property types.
- **Geospatial Analysis**:
  - Mapped property distributions and hotspots using latitude and longitude data.
- **Feature Impact**:
  - Illustrated the influence of various features on property prices through heatmaps and scatter plots.
- **Stakeholder Reporting**:
  - Generated comprehensive reports facilitating data-driven decision-making.

*Power BI files and exported visuals are available in the `visualizations/` directory.*

---

## Screenshots

### Application Interface

![Application Interface](https://github.com/user-attachments/assets/c033ec10-1797-4951-a6b6-bd28fbedece6)

### Exploratory Data Analysis (EDA)

![EDA](https://user-images.githubusercontent.com/104086680/229906408-2b94758c-00d8-47dd-89f5-9e97c6575898.png)

### Data Analysis in SQL

![Data Analysis](https://user-images.githubusercontent.com/104086680/230314514-8d18cf89-db19-410f-bfa6-f772164aec3d.PNG)

### Power BI Visualization

![Power BI Visualization](https://user-images.githubusercontent.com/104086680/230315216-5c182b39-f085-47e5-960c-f62060dba447.PNG)

---

## Contact

**Your Name**
- **Email**: your.email@example.com
- **LinkedIn**: [Your LinkedIn Profile]([https://www.linkedin.com/in/yourprofile](https://www.linkedin.com/in/usman-ali-06a6351b1/))
- **GitHub**: [Your GitHub Profile]([https://github.com/yourusername](https://github.com/whoisusmanali))
- **Portfolio**: [Your Portfolio Website](https://yourportfolio.com)

*Feel free to reach out for collaboration, queries, or any opportunities related to data science and machine learning.*
