# Risk Management in Trading and Investment Portfolios

This project focuses on implementing and optimizing various risk measures for trading and investment portfolios. It includes calculations and optimizations for Semi-Variance (SV), Mean Absolute Deviation (MAD), Semi Absolute Deviation (SAD), as well as advanced techniques like Stochastic Programming and the Augmented ε-constraint Method. 

## Features

### 1. Semi-Variance (SV) Risk Measure
- **Calculation**: Measures the downside risk by considering deviations below the mean.
- **Optimization**: Minimizes the semi-variance in the portfolio to reduce downside risk.

### 2. Mean Absolute Deviation (MAD) Risk Measure
- **Calculation**: Measures the average deviation from the mean return.
- **Optimization**: Minimizes the MAD to create a more stable portfolio with reduced volatility.

### 3. Semi Absolute Deviation (SAD) Risk Measure
- **Calculation**: Measures the downside deviations below a specified threshold.
- **Optimization**: Minimizes the SAD, focusing on reducing risks that fall below the threshold.

### 4. Portfolio Optimization with Constraints
- **Constraints**: Includes constraints such as minimum and maximum asset weights, and the number of assets in the portfolio.
- **Mixed-Integer Optimization**: Uses binary variables for handling cardinality constraints.

### 5. Stochastic Programming Model
- **Scenario Analysis**: Minimizes regret by considering multiple market scenarios.
- **Optimization**: Finds the portfolio that minimizes the worst-case regret.

### 6. Augmented ε-constraint Method
- **Risk-Return Trade-off**: Optimizes the portfolio by adjusting ε (return threshold) to explore the trade-off between risk and return.
- **Multiple Solutions**: Provides a range of solutions with different risk and return profiles.

## Installation

1. **Clone the Repository**:
    ```bash
    git clone https://github.com/yourusername/risk-management-portfolio.git
    cd risk-management-portfolio
    ```

2. **Install the Required Libraries**:
    ```bash
    pip install numpy cvxpy
    ```

## Usage

### Running the Optimization Scripts

1. **Semi-Variance Optimization**:
    ```python
    optimized_weights = optimize_portfolio_semi_variance(example_returns)
    print("Optimized Portfolio Weights:", optimized_weights)
    ```

2. **Mean Absolute Deviation Optimization**:
    ```python
    optimized_weights = optimize_portfolio_mad(example_returns)
    print("Optimized Portfolio Weights:", optimized_weights)
    ```

3. **Semi Absolute Deviation Optimization**:
    ```python
    optimized_weights = optimize_portfolio_sad(example_returns)
    print("Optimized Portfolio Weights:", optimized_weights)
    ```

4. **Optimization with Constraints**:
    ```python
    optimized_weights = optimize_portfolio_with_constraints(example_returns, min_assets, max_assets, min_weight, max_weight)
    print("Optimized Portfolio Weights:", optimized_weights)
    ```

5. **Stochastic Programming Optimization**:
    ```python
    optimized_weights = minimize_regret(scenario_returns, scenario_probabilities)
    print("Optimized Portfolio Weights:", optimized_weights)
    ```

6. **Augmented ε-constraint Method**:
    ```python
    portfolio_solutions = augmented_epsilon_constraint(returns, covariance_matrix, epsilon_range)
    for solution in portfolio_solutions:
        print(f"Epsilon: {solution['epsilon']:.4f}, Risk: {solution['risk']:.4f}, Return: {solution['return']:.4f}, Weights: {solution['weights']}")
    ```

### Example Outputs

- **Epsilon: -0.0014, Risk: 0.0000, Return: 0.0020, Weights: [0.3382, 0.5086, 0.1532, -1.19e-18]**
- **Epsilon: 0.0005, Risk: 0.0000, Return: 0.0020, Weights: [0.3382, 0.5086, 0.1532, -1.19e-18]**
- **Epsilon: 0.0023, Risk: 0.0000, Return: 0.0023, Weights: [0.3546, 0.4714, 0.1658, 0.0083]**
- **Epsilon: 0.0042, Risk: 0.0000, Return: 0.0042, Weights: [0.3900, 0.3402, 0.1624, 0.1075]**
- **Epsilon: 0.0060, Risk: 0.0000, Return: 0.0060, Weights: [0.4254, 0.2090, 0.1590, 0.2066]**
- **Epsilon: 0.0078, Risk: 0.0000, Return: 0.0078, Weights: [0.4608, 0.0778, 0.1556, 0.3058]**
- **Epsilon: 0.0097, Risk: 0.0000, Return: 0.0097, Weights: [0.4471, 1.25e-20, 0.1084, 0.4445]**
- **Epsilon: 0.0115, Risk: 0.0001, Return: 0.0115, Weights: [0.3597, 9.95e-25, 1.05e-24, 0.6403]**
- **Epsilon: 0.0134, Risk: 0.0002, Return: 0.0134, Weights: [0.1799, -4.71e-24, -1.10e-24, 0.8201]**
- **Epsilon: 0.0152, Risk: 0.0004, Return: 0.0152, Weights: [-2.53e-06, -1.10e-06, -3.18e-06, 1.00e+00]**

## Contributing

1. **Fork the Repository**.
2. **Create a New Branch**:
    ```bash
    git checkout -b feature-branch
    ```
3. **Commit Your Changes**:
    ```bash
    git commit -m "Description of the feature"
    ```
4. **Push to the Branch**:
    ```bash
    git push origin feature-branch
    ```
5. **Open a Pull Request**.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
