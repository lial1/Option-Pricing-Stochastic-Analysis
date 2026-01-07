# Stochastic Option Pricing: Monte Carlo vs. Black-Scholes
**Applied Math Project | Stony Brook University**

## Why I Built This
As an Applied Math student, I’ve spent a lot of time learning the theory behind probability and differential equations. I wanted to see how those "abstract" concepts actually play out in the stock market. This project was a way for me to bridge the gap between classroom math and real-world finance by building a tool that handles live market data from `yfinance`.

##  The Math Behind the Code
The core of this project is modeling stock price dynamics using **Geometric Brownian Motion (GBM)**. I used the following Stochastic Differential Equation to simulate where a stock might go:

$$dS_t = \mu S_t dt + \sigma S_t dW_t$$

Instead of just trusting the Black-Scholes formula as a "black box," I built a **Monte Carlo engine** to simulate 10,000 potential future paths for Omnicom Group (OMC). By averaging the payoffs of all those paths and discounting them back to today, I could "discover" the fair price numerically.

## Features & Learnings
* **Real-Time Data:** I used the `yfinance` API to pull a full year of historical data. Learning to clean and annualize volatility ($\sigma$) was one of the trickiest parts!
* **Vectorization:** I used **NumPy** to run 10,000 simulations at once. I learned early on that using "for-loops" in Python is way too slow for finance.
* **Validation:** I compared my simulation results against the **Black-Scholes** analytical solution. My Monte Carlo estimate was within 1.3% of the theoretical price—it was a huge "lightbulb moment" to see the two different methods converge.

## Challenges I Faced
* **The Volatility Trap:** Originally, my model was off because I didn't realize I needed to multiply the daily return standard deviation by $\sqrt{252}$ to annualize it. 
* **User Inputs:** I wanted to make the script interactive, so I added `input()` prompts. Now, you can test it with any ticker (like AAPL or TSLA) and any strike price.

## How to Run It

1. **Clone the repo**

   git clone <your-repo-url>


2. **Install dependencies**
 
   pip install yfinance numpy pandas matplotlib scipy


3. **Open the notebook**
   - `Stock_Price_Predictor.ipynb`
   - run the cells and follow prompts




## Contact
Feel free to connect with me on [LinkedIn](https://linkedin.com/in/lialil) :)

