# task-4
import pandas as pd
import matplotlib.pyplot as plt
df = pd.read_csv(r"C:\intern\twitter_training.csv", header=None)
df.columns = ["ID", "Entity", "Sentiment", "Tweet"]
df = df.dropna()
print(df.head())
print("\nSentiment Count:")
print(df["Sentiment"].value_counts())
sentiment_count = df["Sentiment"].value_counts()
plt.bar(sentiment_count.index, sentiment_count.values,
edgecolor="black")
plt.title("Sentiment Distribution")
plt.xlabel("Sentiment")
plt.ylabel("Number of Tweets")
plt.xticks(rotation=20)
plt.show()
