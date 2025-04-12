# IIT Seat Allocation Analysis System

## Overview

The **IIT Seat Allocation Analysis System** allows users to explore trends and patterns in the seat allocation process for Indian Institutes of Technology (IITs). This application provides insightful visualizations and analytics on various aspects, such as the number of programs offered by IITs, seat distribution, gender distribution, and trends in opening and closing ranks over the years. The system is designed using **Streamlit** and integrates with various visualization libraries like **Plotly** and **Matplotlib** to offer interactive graphs.

## Features

- **Overall Analysis**: Provides insights into the number of programs, seat distribution, gender distribution, and seat intake trends across different years.
- **Program-Specific Analysis**: Analyzes specific programs across different IITs, comparing opening and closing ranks over the years.
- **Multiple Institute Comparison**: Compares the opening and closing ranks of different IITs or programs based on user-selected filters.

## Key Components

- **Streamlit**: The main framework for building the user interface and handling the backend logic.
- **Plotly**: Used for creating interactive graphs and charts to visualize data.
- **Matplotlib**: Provides additional visualization options like line graphs and bar charts.
- **Scikit-learn (Linear Regression)**: Used for predicting trends based on seat intake data.

## Installation & Setup

To get started with this application locally, follow these steps:

1. **Clone the repository**:

    ```bash
    git clone <repo_url>
    cd <repo_name>
    ```

2. **Install dependencies**:

    Create a virtual environment (optional but recommended):

    ```bash
    python -m venv venv
    source venv/bin/activate  # For Linux/macOS
    venv\Scripts\activate     # For Windows
    ```

    Install the required libraries:

    ```bash
    pip install -r requirements.txt
    ```

    The required libraries are:
    - streamlit
    - pandas
    - plotly
    - matplotlib
    - scikit-learn

3. **Run the application**:

    Once dependencies are installed, run the application:

    ```bash
    streamlit run try.py
    ```

4. **Access the application**:

    Open your web browser and navigate to the address provided by Streamlit (typically `http://localhost:8501`).

## Functionality

### Sidebar Filters
The sidebar allows users to filter data based on the following options:
- **Year Range**: Select a range of years (from 2016 to 2024).
- **Quota**: Filter based on seat allocation type (e.g., General, OBC, SC, etc.).
- **Gender**: Filter based on gender distribution (Male, Female, etc.).

### Tabs

1. **Overall Analysis**: Displays insights such as:
   - **Number of Programs per Institute**
   - **Seat Distribution Among Institutes**
   - **Gender Distribution in Admissions**
   - **Seat Intake Trend Prediction (Linear Regression)**
   - **Average Closing Rank by Year**

2. **Program-Specific Analysis**: Allows users to select specific programs and institutes to view:
   - **Opening Rank vs Year**
   - **Closing Rank vs Year**
   
3. **Multiple Institute Comparison**: Compares multiple institutes or programs based on the average opening and closing ranks, allowing users to:
   - View Top N institutes or programs based on average opening and closing ranks.
   - Visualize comparisons with line graphs.

### Data Download

Users can download the filtered dataset in CSV format for further analysis by clicking the "Download Filtered Data" button.

## Dataset

The data used in this system is sourced from historical seat allocation data from IITs. It includes information about:

- **Institute**: Name of the IIT.
- **Academic Program Name**: Program offered by the IIT.
- **Seat Type**: Type of seat (e.g., General, OBC, etc.).
- **Opening Rank**: Rank at which the program starts accepting candidates.
- **Closing Rank**: Rank at which the program stops accepting candidates.
- **Year**: Academic year of the seat allocation.

## How It Works

- **Data Preprocessing**: The dataset is cleaned by removing any missing or irrelevant data. The ranks are converted to numeric values for analysis.
- **Trend Analysis**: Linear regression is applied to predict seat intake trends over the years.
- **Visualization**: Data is visualized using interactive charts for easy understanding of trends and comparisons.
- **Interactive Features**: Users can interact with the data by selecting different filters, viewing insights, and comparing institutes/programs.

## License

This project is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for details.
