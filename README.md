# CS2MarketMonitoring

A Mobile App to monitor CS2 (Counter-Strike 2) items on the Steam Market.

# About

This project is made for CS2 players who enjoy investing in the Steam Market and want a solution to monitor desirable items to buy or sell at specific prices.  
  
The **backend** will be developed using **Supabase** (PostgreSQL Database) to store the complete list of CS2 items from the Steam Market, a list of popular items, and the items selected by users for more precise analysis and monitoring.  
  
The **frontend** will use **Flutter** with **Dart** to create the UI and to cache the user's item list, delivering a better and faster user experience.  

# Key Features

- Custom Price Alerts: Users can add up to 10 items to their personal watchlist (refreshed hourly) and set custom minimum (buy) and maximum (sell) price alerts.

- Hybrid Price Caching: The app provides instant prices for a "VIP List" of ~500 popular items, which are refreshed hourly by the backend.

- On-Demand Price Checking: For rare items (not on the VIP list), users can perform a limited number of on-demand checks per day. This invokes an Edge Function that fetches live prices securely without using the user`s IP address.

- Local-First Caching: The user's watchlist is saved to a local database (possibly Hive) on the device. This ensures instant loading times and offline access to the last-known prices.

- Smart Search: A robust search and pagination system (with a minimum-character limit) to efficiently query the 19,000+ item database.
