import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt

df = sns.load_dataset("tips")
sns.histplot(df["total_bill"])
plt.show()
sns.boxplot(df["total_bill"])
plt.show()
sns.heatmap(df.corr(), annot=True)
plt.show()
