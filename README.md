Stock Trading Engine

A simple real-time stock trading engine that matches buy and sell orders based on price and quantity.

Features

	•	Supports up to 1,024 stock tickers.  
	•	Handles real-time buy and sell orders.
	•	Matches orders if buy price ≥ lowest sell price.
	•	Ensures thread safety using locks for concurrency.
	•	Uses O(n) time complexity for efficient matching.
	•	Does not use dictionaries, maps, or other high-level data structures.

⸻

How It Works

1.	Placing Orders
	•	A buy order is added if a trader wants to purchase a stock at a specific price.
	•	A sell order is added if a trader wants to sell a stock at a specific price.
	•	Orders are stored in sorted lists for quick matching.



2.	Matching Logic
	•	Orders are sorted so that highest buy prices and lowest sell prices are processed first.
	•	A match occurs when:
  Buy Price >= Lowest Sell Price•	If a match is found, a transaction occurs for the minimum quantity available.
	•	Orders are updated dynamically to reflect the matched quantity.



3.	Handling Concurrency
	•	Uses threading locks to prevent race conditions when multiple traders place orders simultaneously.
	•	Ensures safe order processing in a multi-threaded environment.
