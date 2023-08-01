# StockMarketApp - Android Test Project

StockMarketApp is an Android test project that allows users to fetch stock listings from the AlphaVantage API, store the data in local cache using Room, and view stock details along with a graphical representation of the stock data using a custom Canvas-based graph. The app is built using Jetpack Compose for the UI, Coil for image loading, and Hilt for dependency injection.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Setup](#setup)
- [Dependencies](#dependencies)
- [Usage](#usage)
- [Clean Architecture](#clean-architecture)
- [CSV Parser](#csv-parser)
- [License](#license)

## Introduction

The StockMarketApp is a simple Android application that demonstrates how to integrate with the AlphaVantage API to fetch stock listings and store them in a local cache using the Room database. It also provides a user interface to view detailed information about individual stocks and displays the stock data using a custom Canvas-based graph. The app utilizes Jetpack Compose for a modern and declarative UI, Coil for efficient image loading, and Hilt for dependency injection to manage and provide dependencies.

## Features

- Fetch stock listings from the AlphaVantage API.
- Store stock data in the local cache using Room.
- Perform search for stocks from the local cache.
- View detailed information about individual stocks.
- Display a graphical representation of the stock data using a custom Canvas-based graph.

## Setup

To run the StockMarketApp project locally, follow these steps:

1. Clone the repository: `git clone https://github.com/mehsan-dev/StockMarketApp.git`
2. Open the project in Android Studio.
3. Make sure you have the latest Android SDK and necessary build tools installed.
4. Set up an AlphaVantage API key. You can obtain one by signing up at https://www.alphavantage.co/support/#api-key.
5. Replace the placeholder API key in the project with your actual AlphaVantage API key.

## Dependencies

The StockMarketApp project uses the following major dependencies:

- AndroidX: A collection of libraries that help you build robust and efficient Android apps.
- Room: A library that provides an abstraction layer over SQLite for database operations.
- Jetpack Compose: A modern toolkit for building native Android UI with a declarative approach.
- Coil: An image loading library that handles image loading efficiently and seamlessly.
- Hilt: A dependency injection library for Android that reduces boilerplate code and simplifies dependency management.

For a complete list of dependencies and their versions, please refer to the `build.gradle` files in the project.

## Usage

The StockMarketApp consists of two main screens:

1. **Stock Listing Screen**: This screen displays the list of available stocks fetched from the AlphaVantage API. The user can search for specific stocks using the search bar. The search results will be displayed from the local cache using Room, ensuring faster access to data.

2. **Stock Details Screen**: When the user taps on a specific stock from the listing screen, they will be navigated to the stock details screen. This screen shows detailed information about the selected stock, including its current price, historical performance, and other relevant data. The graphical representation of the stock's historical data will be displayed using a custom Canvas-based graph.

## Clean Architecture

The StockMarketApp follows the principles of Clean Architecture to maintain separation of concerns and make the codebase more maintainable, scalable, and testable. It is structured into the following layers:

- **Presentation Layer**: Contains the UI components (Activities, Fragments, etc.), ViewModels, and other UI-related logic.
- **Domain Layer**: Defines the business logic and use cases of the app. It contains the Interactors or Use Cases that implement the app's business rules.
- **Data Layer**: Handles data sources, repositories, and data mapping. It includes the implementation of the AlphaVantage API client and Room database.

## CSV Parser

To create the graph, the StockMarketApp uses a CSV parser located in a separate package. This package is responsible for parsing the CSV file provided by AlphaVantage and extracting the data required for the app. By encapsulating this functionality in a separate package, the Single Responsibility Principle (SRP) is adhered to, making the code more modular and maintainable.
