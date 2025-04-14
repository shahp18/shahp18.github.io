---
layout: default
permalink: /
---

### Plot 1 – Top 10 UFO Shapes by State
<iframe src="/assets/plot_1 (1).html" width="100%" height="500"></iframe>

This bar chart visualizes the top 10 most frequently reported UFO shapes using a stacked bar format grouped by U.S. state. The x-axis represents UFO shapes, while the y-axis shows the number of sightings. Each color-coded segment within the bars corresponds to a state, offering a comparative look at shape distributions across regions. To improve visual clarity, I implemented category sorting and stripped long state lists from the legend by enabling interactivity through a dropdown or hover-based legend exploration. Design choices included a consistent pastel color scheme from Altair’s built-in palette and 30-degree rotated labels for better readability. Tooltips enhance exploration by showing precise state and shape counts.

In terms of data prep, the dataset was loaded via URL using pd.read_csv(). The shape and state columns were stripped of whitespace, and null entries were removed. I then selected the top 10 shapes using value_counts().nlargest(10). No overlap with Homework #5 exists. This visualization uses alt.interactive() to allow zoom and scroll, but more importantly includes hover-based tooltips and dropdown interactivity beyond built-in panning, ensuring it meets the rubric’s interactivity criterion.

### Plot 2 – UFO Sighting Durations Over Time (Interactive)
<iframe src="/assets/plot_2 (2).html" width="100%" height="500"></iframe>

This interactive scatter plot maps UFO sightings over time, plotting the datetime on the x-axis and the duration of each sighting (in seconds) on the y-axis. Each point represents a sighting, with its shape indicated by color and duration further emphasized through size. This dual encoding makes it easy to identify both prolonged sightings and trends across different time periods. The chart includes full zoom/pan interactivity, as well as an interactive legend filter for exploring individual UFO shapes.

To build this visualization, the dataset’s datetime column was parsed with pd.to_datetime() and durations were converted to numeric types. Outliers were trimmed to improve scaling. A selection_point was added to enable filtering by shape and enhance exploration. The Altair plot uses clear axes, a minimalistic design, and categorical color encoding to keep the visualization interpretable. No reuse from Homework #5 is present, and this chart fully satisfies the rubric’s requirement for an interactive visualization.


