# Loan Data Analysis

The dataset contains information about various borrowers, including their pending loan amounts, demographic details, tenure, interest rates, bounce behavior, disbursed amounts, and unique loan identifiers.

## Table of Contents

- [Introduction](#introduction)
- [Analysis](#analysis)
 - [Risk Analysis](#risk-analysis)
 - [Ticket Size Segmentation](#ticket-size-segmentation)
 - [Tenure Segmentation](#tenure-segmentation)
 - [Channel Recommendations](#channel-recommendations)
- [Tools](#tools)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Introduction

The problem statement suggests several analyses, including risk labeling, tenure labeling, ticket size labeling, and channel recommendations. This project covers all of these analyses in detail.

## Analysis

### Risk Analysis

Borrowers are categorized into risk segments based on their bounce behavior:

- **Unknown Risk (New Customers)**: Borrowers new to the system with insufficient historical data to assess their risk profile.
- **Low Risk**: Borrowers with consistent repayment behavior and no bounces in the last 6 months.
- **Medium Risk**: Borrowers with occasional bounces (less than twice in the last 6 months) but no bounce in the most recent month.
- **High Risk**: Borrowers who do not fall into the above categories and pose a higher risk of default.

### Ticket Size Segmentation

Borrowers are grouped into three cohorts based on the size of their pending amount:

- **Low Ticket Size**: Borrowers with pending amounts less than 0.9 * (mean of pending amount column).
- **High Ticket Size**: Borrowers with pending amounts greater than 1.28 * (mean of pending amount column).
- **Medium Ticket Size**: Borrowers who do not fall into the above two categories.

### Tenure Segmentation

Borrowers are categorized into three tenure segments based on the duration of their loan tenure:

- **Early Tenure**: Borrowers in the initial phase of their loan tenure (3 months in the book).
- **Late Tenure**: Borrowers nearing the end of their loan tenure (3 months away from closing the loan).
- **Mid Tenure**: Borrowers in the intermediate phase of their loan tenure.

### Channel Recommendations

Optimized channel spend strategies are proposed based on risk label, ticket size, tenure status, metropolitan city, and new customer status. Borrowers are assigned scores, and the following channels are recommended:

- **WhatsApp Bot**: Borrowers with a score <= 3.
- **Voice Bot**: Borrowers with a score <= 7 or belonging to a metropolitan city.
- **Human Calling**: Borrowers who do not fall into the above two categories.

## Tools

The following tools were used for the analysis:

- Python
- Pandas
- NumPy

## Usage

1. Clone the repository: `git clone https://github.com/your-username/loan-data-analysis.git`
2. Navigate to the project directory: `cd loan-data-analysis`
3. Open the Jupyter Notebook: `jupyter notebook`
4. Run the notebook cells to reproduce the analysis.

## Contributing

Contributions are welcome! If you find any issues or have suggestions for improvements, please open an issue or submit a pull request.

## License

This project is licensed under the [MIT License](LICENSE).
