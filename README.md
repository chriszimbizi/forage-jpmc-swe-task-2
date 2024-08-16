# Task 2: Enhancing Data Visualization in React Application

## Overview

Updated the `App.tsx` and `Graph.tsx` files to improve data visualization in the React application. Changes include rendering conditional graphs, continuous data fetching, and configuring the `Graph` component for better data presentation.

## Changes Made

### `App.tsx`

- **Graph Rendering**: Modified `renderGraph` method to conditionally render the graph only when `showGraph` state is `true`.
- **Continuous Data Fetching**: Updated `getDataFromServer` method to continuously fetch data using `setInterval` with a guard value for stopping the interval.
- **State Management**: Ensured `setState()` is used for state updates outside the constructor.

### `Graph.tsx`

- **HTMLElement Extension**: Extended `PerspectiveViewerElement` to behave like an `HTMLElement`.
- **Simplified DOM Access**: Updated `componentDidMount` to simplify element access using `document.getElementsByTagName`.
- **Graph Configuration**: Added and configured attributes:
  - `view` set to `y_line` for continuous line graph.
  - `column-pivots` to distinguish between stocks.
  - `row-pivots` for x-axis timestamps.
  - `columns` focused on `top_ask_price`.
  - `aggregates` to handle and average duplicated data points.

## Result

- The application now renders a continuous line graph with real-time data updates.
