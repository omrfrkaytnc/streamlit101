# Streamlit Session State Example

This repository demonstrates the practical use of Streamlit's session state mechanism.

## Overview

This Streamlit app reads data from a CSV file and displays it in a table. Users can dynamically adjust the number of rows displayed using "Increase" and "Decrease" buttons.

## Features

- **Dynamic Table Display:** The number of rows shown in the table can be increased or decreased.
- **Session State Management:** Maintains the state of the row count between interactions using Streamlit's session state.

## Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/your-username/streamlit-session-state-example.git
    ```

2. Navigate to the project directory:

    ```bash
    cd streamlit-session-state-example
    ```

3. Ensure `data.csv` is in the project directory.

4. Install Streamlit if not already installed:

    ```bash
    pip install streamlit
    ```

5. Run the app:

    ```bash
    streamlit run app.py
    ```

## Code Summary

- **Session State Initialization:** Initializes the row count to 10 if not already set.
- **Data Loading:** Reads data from `data.csv`.
- **Table Display:** Shows the top rows of the dataframe based on the current row count.
- **Buttons:** "Increase" and "Decrease" buttons adjust the row count.
- **State Display:** Displays the current row count.

## License

This project is licensed under the MIT License.

