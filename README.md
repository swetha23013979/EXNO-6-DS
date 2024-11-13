# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY
# REG NO:212223040222
# Aim:
  To Perform Data Visualization using seaborn python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:
 ```
import seaborn as sns
import matplotlib.pyplot as plt
df=sns.load_dataset("tips")
df
```
![image](https://github.com/user-attachments/assets/7846eefa-7a9f-445d-9be1-4da8d27956ef)

```
sns.lineplot(x="total_bill",y="tip",data=df,hue="sex",linestyle='solid',legend="auto")
```
![image](https://github.com/user-attachments/assets/0d1b9a98-4286-4ae3-a4d8-3cb6c988f232)

```
import seaborn as sns
import matplotlib.pyplot as plt
tips=sns.load_dataset('tips')
avg_total_bill=tips.groupby('day')['total_bill'].mean()
avg_tip=tips.groupby('day')['tip'].mean()
```
![image](https://github.com/user-attachments/assets/f85cd42a-09bb-4e40-8d5c-13359b9eed72)
```
plt.figure(figsize=(8,6))
p1=plt.bar(avg_total_bill.index,avg_total_bill,label='Total Bill')
p2=plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip')
plt.xlabel('Day of the week')
plt.ylabel('Amount')
plt.title('Amount Total Bill and Tip by Day')
plt.legend()
```
![image](https://github.com/user-attachments/assets/f63102eb-f06a-49dc-bb29-a83dbdf4486e)
```
avg_total_bill=tips.groupby('time')['total_bill'].mean()
avg_tip=tips.groupby('time')['tip'].mean()
```
![image](https://github.com/user-attachments/assets/fe70946e-3837-4241-9d16-a974774d025a)

```
p1=plt.bar(avg_total_bill.index,avg_total_bill,label='Total Bill',width=0.4)
p2=plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label="Tip",width=0.4)
plt.xlabel('Day of the Week')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Day')
plt.legend()
```
![image](https://github.com/user-attachments/assets/3299fd2a-fa47-48ba-bd7c-7a89cae5f3c6)

```

import seaborn as sns
dt=sns.load_dataset('tips')
sns.barplot(x='day',y='total_bill',hue='sex',data=dt,palette='Set1')
plt.xlabel('Day of the Week')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Day')
```
![image](https://github.com/user-attachments/assets/08334173-8820-4160-b4b3-9f1f609564a6)

```
tips=sns.load_dataset('tips')
sns.scatterplot(x='total_bill',y='tip',hue='sex',data=tips)
plt.xlabel('Total Bill')
plt.ylabel('Tip Amount')
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
```
![image](https://github.com/user-attachments/assets/19b3ed3b-b082-47d4-81bd-be7f04405647)

```
sns.boxplot(x='day',y='total_bill',hue="smoker",data=tips,linewidth=2,width=0.6,boxprops={"facecolor":"red","edgecolor":"yellow"},
whiskerprops={"color":"green","linestyle":"--","linewidth":1.5},capprops={"color":"black","linestyle":"--","linewidth":1.5})
```
![image](https://github.com/user-attachments/assets/80cf78a5-01ba-4f7f-a4a7-13fd44684e5e)

```
df=sns.load_dataset("tips")
import seaborn as sns

import matplotlib.pyplot as plt
sns.violinplot(x="day", y="total_bill", hue="smoker", data=df, linewidth=2, width=0.6, palette="Set3", inner="quartile")
plt.xlabel("Day of the Week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")
```
![image](https://github.com/user-attachments/assets/11f814fb-2127-4437-b5c6-09a8ab443a01)

```
sns.set(style = 'whitegrid')
tip = sns.load_dataset('tips')
sns.violinplot(x ='day', y ='tip', data = tip)
```
![image](https://github.com/user-attachments/assets/437b606e-30e0-461c-a9fd-a2e40bba479f)

```
sns.set(style = 'whitegrid')
tip = sns.load_dataset('tips')
sns.violinplot(x=tip["total_bill"])
```
![image](https://github.com/user-attachments/assets/bcd88010-410b-4a0f-a8e5-a097937c33cb)

```
sns.kdeplot(data=tips,x='total_bill',hue='time',multiple='fill',linewidth=3,palette='Set2',alpha=0.8)
```
![image](https://github.com/user-attachments/assets/5092d64f-74fa-410c-b184-6564564d886e)

```
sns.kdeplot(data=tips, x='total_bill', hue='time', multiple='stack', linewidth=3, palette='Set2', alpha=0.8)
```
![image](https://github.com/user-attachments/assets/a12ca451-f42a-41b5-bcb4-895562dd456c)

```
import numpy as np
data=np.random.randint(low=1,high=100,size=(10,10))
print("The data to be plotted")
print(data)
```
![image](https://github.com/user-attachments/assets/25d2c832-c29a-4d72-becc-aa154018bc43)

```
hms=sns.heatmap(data=data)
```
![image](https://github.com/user-attachments/assets/daa96e66-4ed4-410e-b08a-eb708e3a62d3)

```
hms=sns.heatmap(data=data,annot=True)
```
![image](https://github.com/user-attachments/assets/4e155286-4338-4edd-9029-6e343c606440)

```
import numpy as np
df=np.random.randint(low=1,high=100,size=(10,10))
print("The data to be plotted")
print(df)
```
![image](https://github.com/user-attachments/assets/1dd0b780-1466-407d-a2d6-fb9f5bc4a031)

```
hms=sns.heatmap(data=df)
```

```
hms=sns.heatmap(data=df,annot=True)
```
![image](https://github.com/user-attachments/assets/7c8af1b0-d025-4215-a66e-f2ded293dcf3)

```
import seaborn as sns
import numpy as np
import matplotlib.pyplot as plt
tips=sns.load_dataset("tips")
numeric_cols=tips.select_dtypes(include=np.number).columns
corr=tips[numeric_cols].corr()
sns.heatmap(corr,annot=True,cmap="plasma",linewidths=0.5)
```
![image](https://github.com/user-attachments/assets/8a720f25-5348-4911-8718-82c035f1b441)








# Result:

Thus, all the data visualization techniques of seaborn has been implemented.
