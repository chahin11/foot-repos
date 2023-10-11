# foot-repos
Generative AI recreating football  game

**Approach 1: Gait Duration**

In the first approach, the code calculates the gait duration for each label by assuming a constant sampling rate of 50Hz. It then checks whether the calculated gait duration falls within an acceptable range (defined by `min_gait_length` and `max_gait_length`). Finally, it visualizes the gait durations using a bar chart.

**Approach 2: Gait Length**

The second approach takes a more sophisticated approach to estimate gait length. It involves the following steps:

1. **Peak and Valley Detection**: Peaks and valleys are detected in the accelerometer data. These represent significant points in the data that can be associated with steps.

2. **Stance and Swing Phase Duration**: Time durations between consecutive peaks (stance phases) and valleys (swing phases) are calculated.

3. **Mean Stance and Swing Phase Duration**: The mean time duration for both the stance and swing phases is computed.

4. **Gait Length Calculation**: The gait length is determined by summing the mean stance phase duration and mean swing phase duration.

5. **Comparison with Acceptable Range**: Similar to the first approach, the calculated gait length is checked against the acceptable range (`min_gait_length` and `max_gait_length`).

**Differences Between two Approachs who I used:**

1. **Methodology**:
   - Approach 1 focuses solely on the duration of the gait, while Approach 2 considers more detailed aspects of the gait cycle, including stance and swing phases.

2. **Accuracy and Detail**:
   - Approach 2 is likely to provide a more accurate estimation of gait length as it takes into account the specific phases of the gait cycle.

3. **Complexity**:
   - Approach 2 is more complex due to the additional steps involved in peak and valley detection, and the calculation of stance and swing phases.

4. **Data Modification**:
   - Approach 2 modifies the original `donnees1` data by adding information about whether the gait length is within range and including the calculated gait length and 'within_range' field.

5. **Visualization**:
   - Both approaches use Plotly Express to create bar charts, but they visualize different metrics (gait duration vs. gait length).

Overall, Approach 2 provides a more detailed and accurate analysis of gait data, particularly for tasks that require a precise understanding of gait dynamics. However, it is also more complex and involves additional steps compared to Approach 1. 
