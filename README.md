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
    df=sns.load_dataset("tips")
    df


<img width="578" height="465" alt="image" src="https://github.com/user-attachments/assets/5e3ca269-d4d6-415a-8337-380e7bd867ac" />

    sns.lineplot(x="total_bill",y="tip",data=df,hue="sex",linestyle="dashed",legend="auto",palette="Set3")


<img width="720" height="526" alt="image" src="https://github.com/user-attachments/assets/75f5d04a-b15f-4762-951a-6147fa34c7cf" />


    x=[1,2,3,4,5]
    y1=[1,4,9,16,25]
    y2=[2,4,5,6,7]
    y3=[1,9,5,3,2]
    sns.lineplot(x=x,y=y1,label="y1",color="skyblue")
    sns.lineplot(x=x,y=y2,label="y2",color="yellow")
    sns.lineplot(x=x,y=y3,label="y3",color="lightgreen")
    plt.title("Multi Line Plot")
    plt.xlabel("X-Axis")
    plt.ylabel("Y-Axis")
    plt.legend()
    plt.show()


<img width="739" height="513" alt="image" src="https://github.com/user-attachments/assets/671a3c46-1810-425c-a401-b656cd0ca9e6" />


    tips=sns.load_dataset("tips")
    avg_totalbill=tips.groupby("day")["total_bill"].mean()
    avg_tips=tips.groupby("day")["tip"].mean()
    p1=plt.bar(avg_totalbill.index,avg_totalbill,label="Avg Total Bill",color="skyblue")
    p2=plt.bar(avg_tips.index,avg_tips,bottom=avg_totalbill,label="Avg Total Bill",color="yellow")
    plt.xlabel("Day")
    plt.ylabel("Amount")
    plt.title("Average Total Bill and Tips by Day")
    plt.legend()
    plt.show()


<img width="787" height="630" alt="image" src="https://github.com/user-attachments/assets/c658e91e-9f9b-4adf-8534-1907a33747e6" />

    tips=sns.load_dataset("tips")
    avg_totalbill=tips.groupby("time")["total_bill"].mean()
    avg_tips=tips.groupby("time")["tip"].mean()
    p1=plt.bar(avg_totalbill.index,avg_totalbill,label="Avg Total Bill",color="skyblue")
    p2=plt.bar(avg_tips.index,avg_tips,bottom=avg_totalbill,label="Avg Total Bill",color="yellow")
    plt.xlabel("Time")
    plt.ylabel("Amount")
    plt.title("Average Total Bill and Tips by time")
    plt.legend()
    plt.show()

<img width="734" height="543" alt="image" src="https://github.com/user-attachments/assets/2ad4e0e0-6a06-405e-9227-1b82604d00b3" />

    sns.barplot(x="day",y="total_bill",data=tips,hue="sex",palette='Set3')
    plt.xlabel("Day")
    plt.ylabel("Total Bill")
    plt.title("Total Bill by Day and Sex")
    plt.show()


<img width="729" height="521" alt="image" src="https://github.com/user-attachments/assets/255345f1-aaf2-46fe-934d-eddeaedb9af7" />

    sns.scatterplot(x="total_bill",y="tip",hue="sex",data=df,palette="Set3")
<img width="711" height="484" alt="image" src="https://github.com/user-attachments/assets/2f4d764c-e920-4610-aaed-57afd48c3c65" />

    sns.histplot(data=df,x="total_bill",hue="smoker",kde=True,palette="Set3")

<img width="770" height="516" alt="image" src="https://github.com/user-attachments/assets/6a041946-148b-4267-98fe-aa9db30a3efa" />

    sns.boxplot(x='day',y='total_bill',data=df,palette='Set3')
<img width="707" height="541" alt="image" src="https://github.com/user-attachments/assets/78bb5e1e-37e3-4a17-9e91-23f8b31e7782" />

    sns.boxplot(x='day',y='total_bill',hue='smoker',data=df,linewidth=2,width=0.6,palette='Set3')
<img width="732" height="511" alt="image" src="https://github.com/user-attachments/assets/32e5bf43-cb66-4abd-aaaf-c41e9d50a7d2" />
    
    sns.violinplot(x='day',y='total_bill',hue="smoker",data=df,palette='Set3')
    plt.xlabel("Day")
    plt.ylabel("Total Bill")
    plt.title("Total Bill by Day and Smoker")
    plt.show()

<img width="719" height="525" alt="image" src="https://github.com/user-attachments/assets/560d5a42-988f-4872-a4e6-37c5d5576c07" />

    sns.violinplot(x='day',y='tip',hue="smoker",data=df,palette='Set3')
    plt.show()

<img width="734" height="505" alt="image" src="https://github.com/user-attachments/assets/f4f275fa-5e80-478e-a51b-a12f0c840c51" />

    sns.violinplot(x="total_bill",data=df,palette="Set3")
<img width="615" height="520" alt="image" src="https://github.com/user-attachments/assets/62053f1e-1b5c-4cfe-bb16-238921d2953e" />

    sns.violinplot(x="tip",y="day",data=df,palette="rainbow")
<img width="726" height="556" alt="image" src="https://github.com/user-attachments/assets/b55aabb1-c8a0-4aec-9b12-4f70a5ca8f18" />

    sns.kdeplot(data=df,x="total_bill",hue="time",multiple='layer',palette="Set3")
<img width="746" height="509" alt="image" src="https://github.com/user-attachments/assets/deed6e3a-a68c-4d46-9345-a5fcc686b425" />

    sns.kdeplot(data=df,x="total_bill",hue="time",multiple='stack',palette="Set3")
<img width="682" height="495" alt="image" src="https://github.com/user-attachments/assets/1ffb317f-714a-41ce-8b30-d5a19c1166ae" />

    sns.kdeplot(data=df,x="total_bill",hue="time",multiple='fill',palette="Set3")
<img width="722" height="508" alt="image" src="https://github.com/user-attachments/assets/3638c7b4-990e-496b-9115-27b3d84c729b" />
    
    num=tips.select_dtypes(include=['float64','int64']).columns
    corr=tips[num].corr()
    sns.heatmap(corr,annot=True,cmap='YlGnBu')


<img width="634" height="515" alt="image" src="https://github.com/user-attachments/assets/ad39c42a-cf37-43ea-8250-bc1abe994a64" />

    sns.heatmap(corr,cmap='YlGnBu')
<img width="692" height="522" alt="image" src="https://github.com/user-attachments/assets/9a692b3f-d5d5-4b0f-b511-81d941bf76d0" />



# Result:
 Thus the expected output is achieved
