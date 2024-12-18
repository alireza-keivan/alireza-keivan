- 👋 Hi, I’m Alireza Keivan, I'm a bachelor of computer engineering and at Hakim Sabzevari University.
- 👀 I’m interested in computer vision, CNNs, and Artificial intelligence.
- 📫 How to reach me: 
  1. alirezakeyvan06@yahoo.com
  2. www.linkedin.com/in/alireza-keivan
plt.figure(figsize=(5,5))
class_cnt = main_df.groupby(['classes']).size().reset_index(name = 'counts')
colors = sns.color_palette('Paired')[0:9]
plt.pie(class_cnt['counts'], labels=class_cnt['classes'], colors=colors, autopct='%1.1f%%')
plt.legend(loc='upper right')
plt.show()
