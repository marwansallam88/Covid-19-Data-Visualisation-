# COVID-19 Data Visualization Tool (MATLAB)

## Description  
A MATLAB application for visualizing global COVID-19 case and death data from Johns Hopkins University. The tool features interactive GUI components for exploring pandemic trends across countries and regions, with customizable plotting options for cumulative/daily views and data averaging.

## Key Features  
- **Interactive GUI**:  
  - Dual listboxes for country/region selection (automatically updates when "Global" or countries with subregions are selected)  
  - Radio buttons to toggle between cases/deaths/both  
  - Slider for N-day moving averages (1-15 days)  
- **Dynamic Plotting**:  
  - Automatic title generation reflecting current selection  
  - Dual-axis support for simultaneous case/death visualization  
  - Bar charts (cumulative) vs. line plots (daily)  
- **Data Processing**:  
  - Calculates global totals from raw country data  
  - Converts cumulative data to daily values when selected  
  - Implements moving average calculations  

## Technical Implementation  
- **Object-Oriented Architecture**:  
  - Custom classes for countries/regions with hierarchical relationships  
  - 80-line data class definition (includes cell array parsing)  
- **GUI Components**:  
  - Built with App Designer (~250 lines of manual code)  
  - Enforces integer slider values  
- **Plotting Techniques**:  
  - `yyaxis` for dual-scale plots  
  - Formatted date labels on x-axis  

## Data Source  
- Johns Hopkins University COVID-19 dataset (provided as MAT-file)  
- Contains cell array (`covid_data`) with:  
  - Country/region names  
  - Cumulative case/death timeseries (Jan 1 - Aug 1)  

## Usage Example  
1. Select "United States" → "Tennessee"  
2. Set "Data to plot" = Both  
3. Change "Option" to Daily  
4. Adjust slider to 7-day average  

## Development Challenges  
- Implementing untaught MATLAB features:  
  - Dual-axis plots  
  - Horizontal date labels  
  - Listbox population  
- Data transformation requirements:  
  - Daily value calculation from cumulative data  
  - Moving average computation  

## Learning Outcomes  
- Practical application of:  
  - Object-oriented programming in MATLAB  
  - Advanced GUI development  
  - Time-series data processing  
  - Self-directed problem solving  

*Total code: ~250 lines (excludes App Designer auto-generated code)*  
