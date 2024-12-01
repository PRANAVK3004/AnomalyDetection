
# System Metrics Anomaly Detection

## Overview
This Python script helps you detect and visualize unusual patterns in your system's performance metrics. It analyzes data from hardware monitoring and highlights any unexpected or extreme values across different metrics.

## What Does This Script Do?

### Key Features
- Detects anomalies in system metrics
- Creates visual graphs showing normal and unusual data points
- Provides a summary of anomalies for each metric

### Metrics Analyzed
1. CPU Temperature
2. CPU Usage
3. CPU Load
4. Memory Usage
5. CPU Power

## Prerequisites

### Required Libraries
- pandas
- numpy
- matplotlib
- scipy


## How to Use the Script

### Prepare Your Data
1. Ensure your CSV file contains the following columns:
   - timestamp
   - cpu_temperature
   - cpu_usage
   - cpu_load
   - memory_usage
   - battery_level
   - cpu_power



## Anomaly Detection Methods

The script uses two methods to identify anomalies:

1. **Z-Score Method**
   - Identifies values that are far from the average
   - Marks points more than 3 standard deviations from the mean

2. **Interquartile Range (IQR) Method**
   - Identifies values outside 1.5 times the interquartile range
   - Helps detect outliers in the data

## Output

### Visualization
- Generates a PNG file with graphs for each metric
- Red points indicate detected anomalies
- Saved in the same directory as the script

### Console Output
- Prints a summary of anomalies for each metric
- Shows total number of anomalies
- Displays percentage of anomalous data points

## Example Output
```
Anomaly Detection Summary:
cpu_temperature:
  Total anomalies detected: 778627
  Percentage of anomalies: 3.22%

cpu_usage:
  Total anomalies detected: 3147881
  Percentage of anomalies: 13.00%

cpu_load:
  Total anomalies detected: 1759469
  Percentage of anomalies: 7.27%
...
```

## Customization

### Adjusting Sensitivity
- Modify the `threshold` parameter in `detect_anomalies()` function
- Lower values make the detection more sensitive
- Higher values make it more lenient

## Troubleshooting

### Common Issues
- Ensure CSV file is properly formatted
- Check that all required columns are present
- Verify data types (numeric columns should contain numbers)

### Error Handling
- Script will print error messages if data loading fails
- Provides guidance on potential issues

## Limitations
- Works best with consistent, clean data
- May require manual tuning for specific datasets
- Anomaly detection is statistical and may not catch all unusual patterns

## Contributing
Feel free to fork the repository and submit pull requests with improvements or additional features.



## Contact
kumbhojkarpranav2@gmail.com
