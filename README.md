# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY

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
 import seaborn as sns
 
import matplotlib.pyplot as plt

x=[1,2,3,4,5]

y=[3,6,2,7,1]

sns.lineplot(x=x,y=y)

<img width="699" height="543" alt="image" src="https://github.com/user-attachments/assets/87e07461-e435-4a9f-8294-a70c57284e09" />

df=sns.load_dataset("tips")

df
<img width="540" height="507" alt="image" src="https://github.com/user-attachments/assets/2f0304ef-31a0-4ce7-afb1-f44a8059a0c1" />

sns.lineplot(x="total_bill",y="tip",data=df,hue="sex",linestyle='solid',legend="auto")

<img width="746" height="589" alt="image" src="https://github.com/user-attachments/assets/bd627f60-f662-430e-9dcb-7d0898bfead5" />

x=[1,2,3,4,5]

y1=[3,5,2,6,1]

y2=[1,6,4,3,8]

y3=[5,2,7,1,4]

sns.lineplot(x=x,y=y1)

sns.lineplot(x=x,y=y2)

sns.lineplot(x=x,y=y3)

plt.title('Multi-:Line Plot')

plt.xlabel('X-Label')

plt.ylabel('Y-Label')

<img width="762" height="614" alt="image" src="https://github.com/user-attachments/assets/b552c21e-2a07-49fe-a5c9-3a060680636c" />

tips=sns.load_dataset('tips')

avg_total_bill=tips.groupby('day')['total_bill'].mean()

avg_tip=tips.groupby('day')['tip'].mean()

plt.figure(figsize=(8,6))

p1=plt.bar(avg_total_bill.index,avg_total_bill,label='Total Bill')

p2=plt.bar(avg_tip.index,avg_tip,label='Tip')

plt.xlabel('Day of the Week')

plt.ylabel('Amount')

plt.title('Average Total Bill and Tip by Day')

plt.legend()

<img width="861" height="673" alt="image" src="https://github.com/user-attachments/assets/b7fedac7-d321-4266-8444-00b12d336d6e" />


avg_total_bill=tips.groupby('time')['total_bill'].mean()

avg_tip=tips.groupby('time')['tip'].mean()

p1=plt.bar(avg_total_bill.index,avg_total_bill,label='Total Bill',width=0.4)

p2=plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip',width=0.4)

plt.xlabel('Time of Day')

plt.ylabel('Amount')

plt.title('Average Total Bill and Tip by Time of Day')

plt.legend()

<img width="666" height="541" alt="image" src="https://github.com/user-attachments/assets/10f0094e-692a-4cd3-8f04-89ce56aac537" />

years=range(2000,2012)
apples=[0.895,0.91,0.919,0.926,0.929,0.931,0.934,0.936,0.937,0.9375,0.9372,0.939]

oranges=[0.962,0.941,0.930,0.923,0.918,0.908,0.907,0.904,0.901,0.898,0.9,0.896]

plt.bar(years,apples)

plt.bar(years,oranges,bottom=apples)

<img width="756" height="536" alt="image" src="https://github.com/user-attachments/assets/ac86be7e-bdd9-4513-b7bf-9b1c48792e7c" />

import seaborn as sns

dt=sns.load_dataset('tips')

sns.barplot(x='day',y='total_bill',hue='sex',data=dt,palette='Set1')

plt.xlabel('Day of the Week')

plt.ylabel('Total Bill')

plt.title('Total Bill by Day and Gender')

<img width="728" height="587" alt="image" src="https://github.com/user-attachments/assets/8261e011-85a3-422c-93ca-86acae5f3d2c" />

import pandas as pd

tit=pd.read_csv("/content/titanic_dataset (2).csv")

tit

<img width="525" height="554" alt="image" src="https://github.com/user-attachments/assets/0b47a981-ab52-407b-988b-7d5fba0cc42d" />

plt.figure(figsize=(8,5))

sns.barplot(x='Embarked',y='Fare',data=tit,palette='rainbow')

plt.title("Fare of Passenger by Embarked Town")

<img width="933" height="629" alt="image" src="https://github.com/user-attachments/assets/0c115d2f-9330-42ce-89e7-b54237b045c7" />

plt.figure(figsize=(8,5))

sns.barplot(x='Embarked',y='Fare',data=tit,palette='rainbow',hue='Pclass')

plt.title("Fare of Passenger by Embarked Town,Divided by Class")

<img width="864" height="574" alt="image" src="https://github.com/user-attachments/assets/38c4a2c6-bcda-4962-b967-9e45d31a30e4" />

tips=sns.load_dataset('tips')

sns.scatterplot(x='total_bill',y='tip',hue='sex',data=tips)

plt.xlabel('Total Bill')

plt.ylabel('Tip Amount')

plt.title('Scatter Plot of Total Bill vs. Tip Amount')

<img width="698" height="578" alt="image" src="https://github.com/user-attachments/assets/f73e42bb-dfb5-4d35-a8eb-46c2ba7698c3" />

import seaborn as sns

import numpy as np

import pandas as pd

np.random.seed(1)

num_var=np.random.randn(1000)

num_var=pd.Series(num_var,name="Numerical Variable")

num_var

<img width="247" height="528" alt="image" src="https://github.com/user-attachments/assets/4505fd88-cef3-4a4e-a210-069b72a510b9" />

sns.histplot(data=num_var,kde=True)

<img width="728" height="552" alt="image" src="https://github.com/user-attachments/assets/7b981e60-db2f-4a4c-b56b-e4c4d8aed5e6" />

sns.histplot(data=tit,x="Pclass",hue="Survived",kde=True)

<img width="704" height="544" alt="image" src="https://github.com/user-attachments/assets/c37e7b66-8f74-4e1e-a422-b90595a6e14b" />

import matplotlib.pyplot as plt

np.random.seed(0)

marks=np.random.normal(loc=70,scale=10,size=100)

marks

<img width="704" height="439" alt="image" src="https://github.com/user-attachments/assets/7f4f989e-665a-4fc0-ad8b-77d474e3a5b6" />

sns.histplot(data=marks,bins=10,kde=True,stat='count',cumulative=False,multiple='stack',element='bars',palette='Set1',shrink=0.7)

plt.xlabel('Marks')

plt.ylabel('Density')

plt.title('Histogram of Student Marks')

<img width="684" height="533" alt="image" src="https://github.com/user-attachments/assets/22121c7b-96d3-488d-81ed-5ae67ca59af3" />

tips=sns.load_dataset('tips')

sns.boxplot(x=tips['day'],y=tips['total_bill'],hue=tips['sex'])

<img width="696" height="540" alt="image" src="https://github.com/user-attachments/assets/74c7e825-db6e-4197-aaa9-fa60e00d395d" />

 sns.boxplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6,
 boxprops= {"facecolor": "lightblue", "edgecolor": "darkblue"}, whiskerprops={"color":
 "black", "linestyle": "--", "linewidth": 1.5}, capprops={"color": "black", "linestyle": "--",
 "linewidth": 1.5})
 
 <img width="752" height="592" alt="image" src="https://github.com/user-attachments/assets/1ab8dcd6-9070-40f1-86f1-76c39e5f373a" />

  sns.violinplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6,
 palette="Set3", inner="quartile")
 
 plt.xlabel("Day of the Week")
 
 plt.ylabel("Total Bill")
 
 plt.title("Violin Plot of Total Bill by Day and Smoker Status")

 <img width="765" height="626" alt="image" src="https://github.com/user-attachments/assets/d8168138-6bb4-4c81-ac26-ed965e688310" />

  mart=pd.read_csv("titanic_dataset.csv")
  
 mart

 <img width="783" height="278" alt="image" src="https://github.com/user-attachments/assets/0e879b2e-6246-4c5d-b467-6bfad225ddb9" />

  mart=mart[['PassengerId', 'Survived', 'Age', 'Name', 'Ticket', 'Embarked']]

  mart.head(10)

  <img width="772" height="332" alt="image" src="https://github.com/user-attachments/assets/fe8fbd5e-1bcd-410a-b0bb-de897d0559c5" />

 sns.kdeplot(data=mart,x='PassengerId')

 <img width="744" height="564" alt="image" src="https://github.com/user-attachments/assets/d2296315-50bc-4156-bc89-21221ca2b043" />

  sns.kdeplot(data=mart,x='Age')

  <img width="795" height="559" alt="image" src="https://github.com/user-attachments/assets/cf6d2d55-209d-45b6-8a70-392b8bc37293" />
  
 sns.kdeplot(data=mart)

<img width="778" height="599" alt="image" src="https://github.com/user-attachments/assets/97c059a0-95bd-4265-a46a-b2ba187f30c7" />


 







# Result:
 Include your result here
