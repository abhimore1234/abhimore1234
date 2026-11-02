# 👋 Hi, I'm Abhishek More

### Aspiring Data Engineer | AI & Data Science Student | Data & Cloud Enthusiast


Passionate about building scalable data pipelines, designing efficient data warehouses, and transforming raw data into meaningful business insights. I enjoy working with modern data engineering technologies and continuously learning cloud-native solutions.

---

## 👨‍💻 About Me

I am a third-year Artificial Intelligence & Data Science student with a strong interest in Data Engineering, Analytics, Cloud Computing, and Big Data Technologies.

My goal is to build reliable, scalable, and data-driven solutions that help organizations make better decisions through data.

### Areas of Interest

* Data Engineering & Analytics
* ETL / ELT Pipeline Development
* Data Warehousing & Data Modeling
* Cloud Data Platforms
* Big Data Processing with PySpark
* Business Intelligence & Reporting

---

## 🛠️ Technical Skills

**Languages:** Python, SQL, Pandas, NumPy
**Data Engineering:** ETL/ELT, Data Warehousing, Data Modeling, Star Schema, Medallion Architecture
**Big Data:** PySpark, Apache Airflow, Hadoop
**Cloud:** Azure Data Factory, Azure Databricks, ADLS Gen2, Azure Synapse, AWS, GCP
**Databases:** SQL Server, PostgreSQL, MySQL
**Tools:** Git, GitHub, Docker, Power BI, Excel

---

## 🌱 Currently Learning

* Advanced Apache Spark
* Azure Data Engineering Services
* DataOps & MLOps
* Real-Time Data Streaming
* Lakehouse Architecture
* Cloud-Native Data Platforms

---

## 🎯 Career Goal

To become a skilled Data Engineer capable of designing scalable, reliable, and cloud-native data solutions that enable organizations to unlock the full value of their data.

---

## 📫 Connect With Me

💼 LinkedIn:
https://www.linkedin.com/in/abhishek-more-363bb62b8

💻 GitHub:
https://github.com/abhimore1234

🌐 Portfolio:
https://abhimore.netlify.app

📧 Email:
[abhimore475500@gmail.com](mailto:abhimore475500@gmail.com)

---

### 💡 Motto

*"Turning raw data into reliable insights through engineering excellence."*
















# 1 . ML Practical

import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

from sklearn.model_selection import train_test_split
from sklearn.discriminant_analysis import LinearDiscriminantAnalysis
from sklearn.metrics import accuracy_score, confusion_matrix, classification_report

df = pd.read_csv("Iris.csv")

print("First 5 rows:")
print(df.head())

print("\nDataset Information:")
print(df.info())

X = df[['SepalLengthCm', 'SepalWidthCm',
        'PetalLengthCm', 'PetalWidthCm']]

y = df['Species']

X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=42, stratify=y
)

lda = LinearDiscriminantAnalysis()

lda.fit(X_train, y_train)

y_pred = lda.predict(X_test)

accuracy = accuracy_score(y_test, y_pred)

print("\nAccuracy:", accuracy * 100, "%")

print("\nClassification Report:")
print(classification_report(y_test, y_pred))

cm = confusion_matrix(y_test, y_pred)

plt.figure(figsize=(7, 5))
plt.imshow(cm)
plt.xlabel("Predicted Species")
plt.ylabel("Actual Species")
plt.title("Confusion Matrix")
plt.colorbar()
plt.show()


# Predict species for a new flower
new_flower = pd.DataFrame(
    [[5.1, 3.5, 1.4, 0.2]],
    columns=X.columns
)

prediction = lda.predict(new_flower)

print("\nNew Flower Details:")
print(new_flower)

print("\nPredicted Flower Species:", prediction[0])
          
# 2 .  ML pracrical 2
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

from sklearn.model_selection import train_test_split
from sklearn.linear_model import LinearRegression, Ridge, Lasso
from sklearn.metrics import r2_score, mean_squared_error ,mean_absolute_error

# 1. Load Dataset
df = pd.read_csv("uber.csv")

print(df.head())

# 2. Preprocessing
df = df.dropna().drop_duplicates()
df = df.drop(['Unnamed: 0', 'key', 'pickup_datetime'], axis=1, errors='ignore')
df = df[df['fare_amount'] > 0]

# 3. Outlier Detection
sns.kdeplot(df['fare_amount'], fill=True)
plt.title("Fare Amount Outliers")
plt.show()

Q1 = df['fare_amount'].quantile(0.25)
Q3 = df['fare_amount'].quantile(0.75)
IQR = Q3 - Q1

df = df[(df['fare_amount'] >= Q1 - 1.5 * IQR) &
        (df['fare_amount'] <= Q3 + 1.5 * IQR)]

# 4. Correlation
sns.heatmap(df.corr(), annot=True)
plt.title("Correlation Heatmap")
plt.show()

# 5. Split Data
X = df.drop('fare_amount', axis=1)
y = df['fare_amount']

X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=42)

# 6. Apply Regression Models
models = [LinearRegression(), Ridge(), Lasso()]

for model in models:
    model.fit(X_train, y_train)
    pred = model.predict(X_test)

    print("\n", model)
    print("\nR2 Score:", r2_score(y_test, pred))
    print("RMSE:", np.sqrt(mean_squared_error(y_test, pred)))
    print("MAE:", mean_absolute_error(y_test, pred))

# 7. Predict New Fare
new_ride = [[-73.985, 40.748, -73.985, 40.758, 1]]

fare = models[0].predict(new_ride)

print("\nPredicted Uber Fare:", fare[0])

# ML Practical 3
import matplotlib.pyplot as plt

from sklearn.datasets import load_digits
from sklearn.model_selection import train_test_split
from sklearn.svm import SVC
from sklearn.metrics import accuracy_score, confusion_matrix, classification_report

# 1. Load Dataset
digits = load_digits()

X = digits.data
y = digits.target

# 2. Display Images
plt.figure(figsize=(8, 4))

plt.imshow(digits.images[0], cmap='gray')
plt.title(y[0])
plt.show()

# 3. Split Dataset
X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=42
)

# 4. Apply SVM
model = SVC(kernel='linear')
model.fit(X_train, y_train)

# 5. Prediction
y_pred = model.predict(X_test)

# 6. Evaluation
print("Accuracy:", accuracy_score(y_test, y_pred))
print("\nConfusion Matrix:")
print(confusion_matrix(y_test, y_pred))

print("\nClassification Report:")
print(classification_report(y_test, y_pred))

# 7. Predict One Digit
print("\nActual Digit:", y_test[-1])
print("Predicted Digit:", y_pred[-1])

# ML Practical 4
import pandas as pd
import matplotlib.pyplot as plt
from sklearn.cluster import KMeans

df = pd.read_csv("Iris.csv")
print(df.head(5))
X = df.drop(['Id', 'Species'], axis=1, errors='ignore')

wcss = []

for i in range(1, 11):
    model = KMeans(n_clusters=i, random_state=42, n_init=10)
    model.fit(X)
    wcss.append(model.inertia_)

plt.plot(range(1, 11), wcss, marker='o')
plt.xlabel("Number of Clusters")
plt.ylabel("WCSS")
plt.title("Elbow Method")
plt.show()

kmeans = KMeans(n_clusters=3, random_state=42, n_init=10)
df['Cluster'] = kmeans.fit_predict(X)

print("\nNumber of Clusters:", df['Cluster'].nunique())

print(df[['Species', 'Cluster']].head())

plt.scatter(X.iloc[:, 0], X.iloc[:, 1], c=df['Cluster'])
plt.xlabel("Sepal Length")
plt.ylabel("Sepal Width")
plt.title("K-Means Clustering")
plt.show()

# ML practical 5
import pandas as pd
from sklearn.model_selection import train_test_split
from sklearn.preprocessing import LabelEncoder
from sklearn.ensemble import RandomForestClassifier
from sklearn.metrics import accuracy_score, confusion_matrix, classification_report

df = pd.read_csv("car_evaluation.csv", header=None)
df.columns = ['buying', 'maint', 'doors', 'persons', 'lug_boot', 'safety', 'class']
print(df.head())

le = LabelEncoder()

for col in df.columns:
    df[col] = le.fit_transform(df[col])

X = df.drop('class', axis=1)
y = df['class']

X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=42
)

model = RandomForestClassifier(n_estimators=100, random_state=42)
model.fit(X_train, y_train)

y_pred = model.predict(X_test)

print("Accuracy:", accuracy_score(y_test, y_pred))
print("Confusion Matrix:")
print(confusion_matrix(y_test, y_pred))
print("Classification Report:")
print(classification_report(y_test, y_pred))

print("Predicted Car Class:", le.inverse_transform(y_pred[:5]))

# ML practical 6
import random

Q = {}

def winner(b, p):
    wins = [(0,1,2),(3,4,5),(6,7,8),
            (0,3,6),(1,4,7),(2,5,8),
            (0,4,8),(2,4,6)]
    return any(b[a] == b[c] == b[d] == p for a,c,d in wins)

def train():
    for _ in range(5000):
        b = [' '] * 9

        while True:
            s = ''.join(b)
            moves = [i for i in range(9) if b[i] == ' ']
            Q.setdefault(s, [0]*9)

            a = random.choice(moves) if random.random() < 0.1 else max(moves, key=lambda x: Q[s][x])
            b[a] = 'X'

            if winner(b, 'X'):
                Q[s][a] += 1
                break

            if ' ' not in b:
                break

            m = random.choice([i for i in range(9) if b[i] == ' '])
            b[m] = 'O'

            if winner(b, 'O'):
                Q[s][a] -= 1
                break

def play():
    b = [' '] * 9

    while True:
        print(b[0], "|", b[1], "|", b[2])
        print("-----------")
        print(b[3], "|", b[4], "|", b[5])
        print("-----------")
        print(b[6], "|", b[7], "|", b[8])

        m = int(input("Enter position (1-9): ")) - 1

        if m not in range(9) or b[m] != ' ':
            print("Invalid move!")
            continue

        b[m] = 'O'

        if winner(b, 'O'):
            print("You win!")
            break

        if ' ' not in b:
            print("Draw!")
            break

        s = ''.join(b)
        moves = [i for i in range(9) if b[i] == ' ']
        Q.setdefault(s, [0]*9)

        a = max(moves, key=lambda x: Q[s][x])
        b[a] = 'X'

        if winner(b, 'X'):
            print(b[0:3], b[3:6], b[6:9])
            print("Computer wins!")
            break

        if ' ' not in b:
            print("Draw!")
            break

train()
print("Training completed!")
play()

