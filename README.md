- 👋 Hi, I’m Alireza Keivan, I'm a bachelor of computer engineering and at Hakim Sabzevari University.
- 👀 I’m interested in computer vision, CNNs, and Artificial intelligence.
- 📫 How to reach me: 
  1. alirezakeyvan06@yahoo.com
  2. www.linkedin.com/in/alireza-keivan
# Data Visualization: Class Distribution Pie Chart

This code snippet generates a pie chart visualizing the distribution of classes within a dataset. It's a common technique used to understand the balance or imbalance of different categories in your data.

## Code Explanation

The following Python code uses `matplotlib` and `seaborn` to create the pie chart:

```python
import matplotlib.pyplot as plt
import seaborn as sns
import pandas as pd # Assuming your data is in a pandas DataFrame

# Assuming your dataframe is named main_df
# and has a column called 'classes'

plt.figure(figsize=(5,5))
class_cnt = main_df.groupby(['classes']).size().reset_index(name = 'counts')
colors = sns.color_palette('Paired')[0:9]
plt.pie(class_cnt['counts'], labels=class_cnt['classes'], colors=colors, autopct='%1.1f%%')
plt.legend(loc='upper right')
plt.show()
