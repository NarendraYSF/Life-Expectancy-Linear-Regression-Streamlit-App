# Life Expectancy Prediction Application

A comprehensive Python application for predicting life expectancy based on various health, economic, and social indicators using multiple machine learning models and advanced data analysis techniques.

## 🎯 Project Overview

This application analyzes the World Health Organization (WHO) Life Expectancy dataset to predict life expectancy using various health, economic, and social indicators. The project implements a complete machine learning pipeline from data preprocessing to model deployment with an interactive web interface.

## ✨ Latest Features (v2.0)

### 🌍 **Interactive Map Visualization**
- **Interactive Markers**: Clickable country markers with detailed popups
- **Choropleth Maps**: Color-coded countries based on metric values
- **Heatmaps**: Density visualization showing concentration of values
- **Geographic Statistics**: Regional analysis and country rankings
- **Temporal Trends**: Time series analysis showing changes over years
- **Multiple Map Layers**: Different tile styles (OpenStreetMap, CartoDB)

### 🔍 **Comprehensive Outlier Detection System**
- **Multiple Detection Methods**: Z-score, IQR, Modified Z-score, Isolation Forest
- **Multivariate Analysis**: Local Outlier Factor, Elliptic Envelope
- **Interactive Handling**: Choose detection methods and removal strategies
- **Impact Analysis**: Assess the effect of outlier removal on data statistics
- **Detailed Information**: Show exactly what data was recognized as outliers
- **Visualization**: Comprehensive plots showing outlier distribution and impact

### 🤖 **Enhanced Model Training & Prediction**
- **Real-time Prediction**: Accurate predictions using trained models
- **Preprocessing Pipeline**: Consistent data transformation for predictions
- **Model Persistence**: Save and load trained models
- **Feature Engineering**: Advanced feature creation and selection
- **Cross-validation**: Robust model evaluation

### 📊 **Advanced Data Analysis**
- **Feature vs Target Analysis**: Interactive scatter plots with custom regression lines
- **Country Statistics**: Regional and country-wise analysis
- **Correlation Analysis**: Comprehensive correlation matrices
- **Data Quality Assessment**: Missing value analysis and data validation

### 🎨 **Improved User Interface**
- **Modern Design**: Clean, responsive interface with custom CSS
- **Navigation Tabs**: Organized sections for different functionalities
- **Interactive Controls**: Dynamic parameter adjustment
- **Real-time Updates**: Live data visualization and analysis
- **Mobile Responsive**: Works on desktop and mobile devices

## 📁 Project Structure

```
WHO Life Expectancy/
├── Dataset/
│   └── WHO Life Expectancy Descriptive Statistics - Raw Data.csv
├── __pycache__/                     # Python cache files
├── data_preprocessing.py            # Data preprocessing module
├── model_training.py                # Model training and evaluation
├── visualization.py                 # Visualization functions
├── outlier_detection.py             # Comprehensive outlier detection
├── streamlit_app.py                # Main Streamlit web application
├── Main.py                         # Command-line application
├── requirements.txt                # Python dependencies
├── README.md                       # Project documentation
└── Various test and demo files     # Additional utilities
```

## 🚀 Installation

### Prerequisites
- Python 3.8 or higher
- pip (Python package installer)

### Step 1: Clone the Repository
```bash
git clone <repository-url>
cd "WHO Life Expectancy"
```

### Step 2: Install Dependencies
```bash
pip install -r requirements.txt
```

### Step 3: Verify Installation
```bash
python -c "import pandas, numpy, sklearn, streamlit, plotly, folium; print('All dependencies installed successfully!')"
```

## 📖 Usage

### Web Application (Recommended)

Launch the Streamlit web app:
```bash
streamlit run streamlit_app.py
```

The web application provides:

#### 🏠 **Home Page**
- Project overview and features
- Dataset information and quick statistics
- Navigation to all sections

#### 📈 **Data Analysis**
- Dataset overview and missing value analysis
- Correlation analysis with interactive heatmaps
- Feature vs target analysis with custom regression lines
- Country statistics and regional comparisons

#### 🌍 **Map Visualization** *(NEW)*
- **Interactive Markers**: Click countries to see detailed information
- **Choropleth Maps**: Color-coded global distribution
- **Heatmaps**: Density visualization of metrics
- **Geographic Statistics**: Regional analysis and rankings
- **Temporal Trends**: Time series analysis by region
- **Filtering Options**: By year, region, and metric

#### 🔍 **Outlier Detection**
- Multiple detection methods (Z-score, IQR, Isolation Forest, etc.)
- Interactive parameter adjustment
- Comprehensive outlier analysis
- Impact assessment of outlier removal
- Visual outlier identification

#### 📋 **Outlier Details**
- Detailed information about detected outliers
- Country-specific outlier analysis
- Multivariate outlier examination
- Impact analysis of outlier removal

#### 🤖 **Model Training**
- Configure preprocessing options
- Train multiple models with cross-validation
- Real-time performance monitoring
- Model comparison and selection

#### 📊 **Results**
- Model performance metrics
- Actual vs predicted plots
- Feature importance analysis
- Best model identification

#### 🔮 **Predictions**
- Interactive prediction interface
- Real-time life expectancy predictions
- Input validation and suggestions
- Prediction context and interpretation

#### 📋 **About**
- Comprehensive project documentation
- Technical details and methodology
- Usage instructions and troubleshooting

### Command Line Application

Run the main application:
```bash
python Main.py
```

## 📊 Dataset Information

### Source
World Health Organization (WHO) Life Expectancy Dataset

### Features
- **22 Variables**: Health, economic, and social indicators
- **2,929 Records**: Country-year observations
- **193 Countries**: Global coverage
- **16 Years**: 2000-2015 time period

### Key Variables
- **Target**: Life expectancy (years)
- **Health Indicators**: Adult mortality, infant deaths, BMI, vaccination coverage
- **Economic Indicators**: GDP, income composition, expenditure
- **Social Indicators**: Schooling, alcohol consumption, thinness
- **Categorical Variables**: Country, Status (Developed/Developing), Region

## 🔍 Data Preprocessing Pipeline

### 1. Data Cleaning
- Handle European number formats (commas as decimal separators)
- Convert data types appropriately
- Remove or handle inconsistent values
- PyArrow compatibility handling

### 2. Missing Value Imputation
- **Numerical Variables**: Median imputation (robust to outliers)
- **Categorical Variables**: Most frequent value imputation
- **Percentage Missing**: Analysis and reporting

### 3. Feature Engineering
- **Binary Features**: Convert Status to binary (Developed/Developing)
- **Composite Features**: Health expenditure per capita, total mortality rate
- **Normalized Features**: Year normalization, vaccination coverage
- **Economic Indicators**: GDP per capita, thinness composite

### 4. Categorical Encoding
- **Label Encoding**: Convert Status and Region to numerical values
- **One-hot Encoding**: Alternative approach for categorical variables

### 5. Feature Scaling
- **StandardScaler**: Normalize numerical features to zero mean and unit variance
- **Robust Scaling**: Alternative for outlier-sensitive scaling

## 🤖 Model Training Process

### 1. Data Splitting
- **Train/Test Split**: 80/20 split for model evaluation
- **Cross-Validation**: 5-fold CV for robust performance estimation
- **Random State**: Fixed for reproducibility

### 2. Model Training
- **Multiple Algorithms**: Train 6 different models
- **Hyperparameter Tuning**: Grid search for optimal parameters
- **Performance Tracking**: Monitor training and validation metrics

### 3. Model Evaluation
- **Metrics**: R², RMSE, MAE for comprehensive assessment
- **Cross-Validation**: Mean and standard deviation of CV scores
- **Model Comparison**: Side-by-side performance analysis

### 4. Feature Importance
- **Linear Models**: Coefficient magnitudes
- **Tree-based Models**: Feature importance scores
- **Ranking**: Sort features by importance

## 🌍 Map Visualization Features

### 1. Interactive Maps
- **Folium-based Maps**: Interactive web maps with multiple tile layers
- **Marker Clustering**: Groups nearby markers for better performance
- **Custom Popups**: Detailed country information on click
- **Color Coding**: Different colors for developed vs developing countries

### 2. Map Types
- **Interactive Markers**: Clickable markers with detailed information
- **Choropleth Maps**: Color-coded countries based on metric values
- **Heatmaps**: Density visualization showing concentration of values

### 3. Geographic Analysis
- **Regional Statistics**: Average metrics by region
- **Country Rankings**: Top and bottom countries by metric
- **Temporal Trends**: Changes over time by region
- **Growth Analysis**: Annual growth rates by region

### 4. Interactive Controls
- **Metric Selection**: Choose any numerical metric from dataset
- **Year Filtering**: Filter by specific year or view all years
- **Region Filtering**: Focus on specific regions or view global data
- **Map Type Toggle**: Switch between different visualization styles

## 🔍 Outlier Detection System

### 1. Detection Methods
- **Z-score**: Standard deviation-based detection
- **IQR**: Interquartile range method
- **Modified Z-score**: Robust to extreme values
- **Isolation Forest**: Machine learning-based detection
- **Local Outlier Factor**: Density-based detection
- **Elliptic Envelope**: Statistical outlier detection

### 2. Analysis Features
- **Target Outliers**: Life expectancy outlier detection
- **Feature Outliers**: Individual feature outlier analysis
- **Multivariate Outliers**: Complex outlier patterns
- **Impact Analysis**: Effect of outlier removal on statistics

### 3. Interactive Handling
- **Method Selection**: Choose detection methods
- **Parameter Adjustment**: Customize thresholds and parameters
- **Removal Options**: Choose outlier handling strategy
- **Visual Analysis**: Interactive plots for outlier identification

## 📈 Visualization Features

### 1. Data Exploration
- **Distribution Plots**: Histograms and density plots for all variables
- **Correlation Matrix**: Heatmap showing variable relationships
- **Scatter Plots**: Target vs feature relationships with custom regression lines
- **Country Analysis**: Regional and country-wise visualizations

### 2. Model Performance
- **Comparison Charts**: Bar plots comparing model metrics
- **Actual vs Predicted**: Scatter plots with perfect prediction lines
- **Residual Analysis**: Residual plots and distribution

### 3. Feature Importance
- **Bar Charts**: Horizontal bar plots for feature ranking
- **Interactive Plots**: Plotly-based interactive visualizations

### 4. Outlier Analysis
- **Detection Visualization**: Highlight outliers in distributions
- **Impact Analysis**: Before/after outlier removal comparison
- **Detailed Reports**: Comprehensive outlier information

## 🎯 Model Performance

### Expected Results
Based on the dataset characteristics, typical performance metrics include:

- **R² Score**: 0.75 - 0.85 (depending on model and preprocessing)
- **RMSE**: 3-5 years (root mean square error)
- **MAE**: 2-4 years (mean absolute error)

### Best Performing Models
1. **Gradient Boosting**: Usually highest R² score
2. **Random Forest**: Good balance of performance and interpretability
3. **Elastic Net**: Best among linear models with regularization

### Key Predictors
Common important features include:
- Adult Mortality
- GDP per capita
- Schooling
- BMI
- Vaccination coverage
- Economic indicators

## 🔧 Technical Features

### 1. PyArrow Compatibility
- **Environment Variables**: Disable PyArrow to prevent compatibility issues
- **Alternative Display**: HTML tables and safe DataFrame display
- **Error Handling**: Robust error handling for data display issues

### 2. Data Sanitization
- **Safe Display Functions**: Prevent display errors
- **Data Type Handling**: Proper conversion and validation
- **Missing Value Handling**: Comprehensive missing data management

### 3. Session State Management
- **Model Persistence**: Save trained models in session
- **Data Caching**: Efficient data loading and caching
- **State Management**: Maintain user selections and results

### 4. Responsive Design
- **Custom CSS**: Modern styling and layout
- **Mobile Friendly**: Works on various screen sizes
- **Interactive Elements**: Dynamic controls and visualizations

## 🚨 Troubleshooting

### Common Issues

1. **Missing Dependencies**
   ```bash
   pip install --upgrade pip
   pip install -r requirements.txt
   ```

2. **Data File Not Found**
   - Ensure the dataset is in the `Dataset/` folder
   - Check file name: `WHO Life Expectancy Descriptive Statistics - Raw Data.csv`

3. **PyArrow Errors**
   - These are safely ignored - the app uses alternative display methods
   - Check console for any critical errors

4. **Map Loading Issues**
   - Ensure internet connection for map tiles
   - Check folium and streamlit-folium installation

5. **Memory Issues**
   - Reduce dataset size for testing
   - Use smaller models (fewer estimators for ensemble methods)

### Performance Optimization

1. **Faster Training**
   - Reduce cross-validation folds
   - Use smaller parameter grids
   - Reduce number of estimators in ensemble methods

2. **Memory Optimization**
   - Process data in chunks
   - Use data types with smaller memory footprint
   - Clear variables when not needed

## 📝 API Reference

### DataPreprocessor Class
```python
preprocessor = DataPreprocessor()
df_clean = preprocessor.load_and_clean_data(file_path)
X_scaled, y, features = preprocessor.prepare_final_dataset(df)
```

### LifeExpectancyModel Class
```python
model_trainer = LifeExpectancyModel()
results = model_trainer.train_models(X, y, feature_names)
importance = model_trainer.analyze_feature_importance()
```

### OutlierDetectionSystem Class
```python
outlier_system = OutlierDetectionSystem()
analysis = outlier_system.comprehensive_outlier_analysis(df, target_column='Life expectancy')
```

### Map Visualization Functions
```python
map_obj = create_interactive_map(df, metric='Life expectancy', year=2015)
choropleth_fig = create_choropleth_map(df, metric='Life expectancy')
```

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch: `git checkout -b feature-name`
3. Commit changes: `git commit -am 'Add feature'`
4. Push to branch: `git push origin feature-name`
5. Submit a pull request

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🙏 Acknowledgments

- **World Health Organization**: For providing the comprehensive dataset
- **Scikit-learn**: For the excellent machine learning library
- **Streamlit**: For the web application framework
- **Plotly**: For interactive visualizations
- **Folium**: For interactive map visualizations

---

**Note**: This application is designed for educational and research purposes. For production use, additional validation, testing, and deployment considerations should be implemented.
