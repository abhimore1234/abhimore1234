
# 👋 Hi, I'm Abhishek More 

**Data Science & Full Stack Developer**<br><br>
🌐 Explore My Portfolio : [abhimore.netlify.app](https://abhimore.netlify.app/) <br>
A living canvas of my projects, capabilities, and innovations.

---



## 👨‍💻 About Me

I specialize in turning complex data into actionable insights. With a strong foundation in data analysis, machine learning, and statistical modeling, I help organizations unlock valuable patterns and drive informed decisions.

- **Core Skills:** Data analysis, machine learning, statistical modeling
- **Technologies:** Python, R, SQL, Apache Spark, Hadoop
- **Specializations:** Predictive analytics, deep learning, scalable data pipelines
- **Interests:** AI-driven solutions for business optimization and fraud detection
- **Continuous Learning:** Cloud-based AI, MLOps, efficient model deployment


---

## 🚀 What I Do

- Always curious, always learning—exploring the endless possibilities in data science and full stack development.
- Experiment with new tools, frameworks, and approaches to keep my skills sharp.
- Enjoy breaking down complex topics into easy-to-understand concepts.
- Believe in the power of data to make a positive impact, one project at a time.

---

## 🌱 Motto

> “Data doesn’t lie, but interpretation is everything.”

> “Continuous learning is the key to growth.”

---

## 📫 Connect with Me

[![LinkedIn](https://img.shields.io/badge/LinkedIn-blue?logo=linkedin&logoColor=white)](https://www.linkedin.com/in/abhishek-more-363bb62b8)

---

_Simplicity is the ultimate sophistication._

## 👨‍💻 About Me

I specialize in turning complex data into actionable insights. With a strong foundation in data analysis, machine learning, and statistical modeling, I help organizations unlock valuable patterns and drive informed decisions.

- **Core Skills:** Data analysis, machine learning, statistical modeling
- **Technologies:** Python, R, SQL, Apache Spark, Hadoop
- **Specializations:** Predictive analytics, deep learning, scalable data pipelines
- **Interests:** AI-driven solutions for business optimization and fraud detection
- **Continuous Learning:** Cloud-based AI, MLOps, efficient model deployment

---

## 🚀 What I Do

- Always curious, always learning—exploring the endless possibilities in data science and full stack development.
- Experiment with new tools, frameworks, and approaches to keep my skills sharp.
- Enjoy breaking down complex topics into easy-to-understand concepts.
- Believe in the power of data to make a positive impact, one project at a time.

---

## 🌱 Motto

> “Data doesn’t lie, but interpretation is everything.”

> “Continuous learning is the key to growth.”

---

## 📫 Connect with Me

[![LinkedIn](https://img.shields.io/badge/LinkedIn-blue?logo=linkedin&logoColor=white)](https://www.linkedin.com/in/abhishek-more-363bb62b8)

---

# ANN


# Write a Python program to plot a few activation functions that are being used in neural 
--- networks.
import
 numpy 
as np
import
 matplotlib.pyplot 
as plt
x =
 np.linspace(
10, 10
y = 1 / (1 +
, 100)
 np.exp(
x))
plt.plot(x, y)
plt.title(
"Sigmoid")
plt.show()
y =
 np.tanh(x)
plt.plot(x, y)
plt.title(
plt.show()
"Tanh")
y =
 np.maximum(0
plt.plot(x, y)
plt.title(
, x)
"ReLU")
plt.show()
y =
 np.where(x > 0
, x, 
0.01 * x)
plt.plot(x, y)
plt.title(
"Leaky ReLU")
plt.show()
y =
 np.log(1 +
 np.exp(x))
plt.plot(x, y)
plt.title(
"Softplus")
plt.show()---




�
� Activation Functions in Neural Networks (Theory)
1.
Introduction (Easy Understanding)
In Artificial Neural Networks (ANN), activation functions are used to decide whether a neuron 
should activate (fire) or not.
📘 Simple meaning: Activation function = Decision maker of neuron
Real-life example:
Think of a student giving exam:
If marks > passing marks → PASS (activate) If marks < passing marks → FAIL (not activate)
Same way:
Input comes → processed → activation function decides output
1.
Why Activation Function is Needed?
Without activation function:
Output will be linear only Network cannot learn complex patterns
📘 So activation function adds:
Non-linearity Helps model learn real-world problems (image, speech, AI)
1.
Common Activation Functions (From Your Code)
Your code plots 5 important activation functions:
(1) Sigmoid Function 📘 Formula: σ(x)= 1+e −x 1 
�
� Logic: Takes any value → converts between 0 and 1 Works like probability 📘 Example:
If x = 2
σ(2)= 1+e −2 1 
≈0.88
📘 Output ≈ 1 (activated)
📘 Graph Behavior: S-shaped curve Smooth 📘 Use: Binary classification (Yes/No problems)
(2) Tanh Function 📘 Formula: tanh(x)= e x +e −x e x −e −x 
�
� Logic: Output range: -1 to +1 Better than sigmoid (centered at 0) 📘 Example:
If x = 1
tanh(1)≈0.76 📘 Graph: S-shape but centered at zero 📘 Use: Hidden layers in neural networks
(3) ReLU (Rectified Linear Unit) 📘 Formula: f(x)=max(0,x) 📘 Logic: If x > 0 → output = x If x ≤ 0 → 
output = 0 📘 Example: x = 5 → output = 5 x = -3 → output = 0 📘 Graph: Straight line for positive 
values Zero for negative 📘 Use: Most commonly used activation function 📘 Advantage: Fast 
computation Solves vanishing gradient problem
(4) Leaky ReLU 📘 Formula: f(x)={ x 0.01x 
if x>0 if x≤0 
�
� Logic: Similar to ReLU But allows small negative values 📘 Example: x = -5 → output = -0.05 x = 5 
→ output = 5 📘 Use: Fixes problem of “dead neurons” in ReLU
(5) Softplus Function 📘 Formula: f(x)=log(1+e x ) 📘 Logic: Smooth version of ReLU Always 
positive 📘 Example:
If x = 2
f(2)=log(1+e 2 )≈2.13 📘 Use: When smooth output is needed
1.
Algorithm Used in Your Code
Your Python code follows this simple algorithm:
Step-by-step Algorithm: Import libraries: NumPy → for calculations Matplotlib → for plotting 
graph
Create input values:
x = np.linspace(-10, 10, 100)
📘 Generates 100 values from -10 to +10
Apply activation function: Sigmoid → 1 / (1 + np.exp(-x)) Tanh → np.tanh(x) ReLU → 
np.maximum(0, x) Leaky ReLU → np.where(x > 0, x, 0.01*x) Softplus → np.log(1 + np.exp(x))
Plot graph:
plt.plot(x, y) plt.title("Function Name") plt.show()
1.
2.
3.
✔
Important Logic Summary Function Output Range Key Idea Sigmoid (0,1) Probability 
Tanh (-1,1) Zero-centered ReLU [0,∞) Fast & simple Leaky ReLU (-∞,∞) Fix dead neurons 
Softplus (0,∞) Smooth ReLU
Real-World Use Sigmoid → Email spam detection Tanh → Deep learning hidden layers 
ReLU → Image recognition (CNN) Leaky ReLU → Advanced deep networks Softplus → 
Smooth prediction models
Exam Important Points
 Activation function adds non-linearity 
binary output 
✔
✔
 ReLU is most used in practice 
 Tanh is better than sigmoid (zero centered) 
✔
problem  Softplus is smooth version of ReLU
1.
Short Conclusion
✔
✔
 Sigmoid used for 
 Leaky ReLU solves dead neuron 
Activation functions are the core part of neural networks. They help the model:
Learn complex patterns Make decisions Improve performance
Without them, neural networks behave like simple linear models.
Generate ANDNOT function using McCulloch-Pitts neural net by a python program.
import numpy as np
def step_function(x):
    if x>= 1:
        return 1
    else:
        return 0
inputs = np.array([
    [0,0],
    [0,1],
    [1,0],
    [1,1]
])
weights = np.array([1,-1])
print("A B | Output")
for i in inputs:
    net_input = np.dot(i, weights)
    output = step_function(net_input)
    print(i[0], i[1], "|", output)
A B | Output
0 0 | 0
0 1 | 0
1 0 | 1
1 1 | 0
📘 McCulloch-Pitts Neural Network – AND-NOT Function (Theory)
1. Introduction
The McCulloch-Pitts (MP) Neural Network is one of the earliest neural models used to perform 
basic logical operations.
📘 It behaves like a logic gate:
Takes binary inputs (0 or 1) Produces binary output (0 or 1)
In this practical, it is used to implement the AND-NOT function.
1. Idea of AND-NOT Function
The AND-NOT function is a combination of:
AND operation NOT operation
📘 Output is 1 only when:
First input is 1 Second input is 0
In all other cases, output is 0.
1.
Working of MP Neuron
The MP neuron works as a decision-making unit:
Takes inputs Assigns importance to each input Combines them Makes decision based on a limit
📘 If condition is satisfied → output = 1 📘 Otherwise → output = 0
1.
Logic Used for AND-NOT
To implement AND-NOT:
First input is given positive importance Second input is given negative importance
📘 Why?
Because we want second input to behave like NOT
So:
When second input is 1 → it reduces the result When second input is 0 → it does not affect
1.
Decision Process
After combining inputs:
The neuron checks whether the result is strong enough
📘 If strong → output becomes 1 📘 If weak → output becomes 0
This ensures correct AND-NOT behavior.
1.
Step-by-Step Behavior When both inputs are 0 → no activation When second input is 1 → 
negative effect → output remains 0 When first input is 1 and second is 0 → strong signal → 
output becomes 1 When both inputs are 1 → second cancels effect → output becomes 0
📘 This matches AND-NOT logic perfectly.
1.
2.
Algorithm (Conceptual) Take binary inputs Assign importance (weights) to inputs 
Combine inputs Check against a decision limit Produce output (0 or 1) Repeat for all input 
combinations
Role of Python Program
The Python program:
Tests all input combinations Applies MP neuron logic Produces output for each case
📘 It simulates how a neuron behaves like a logic gate.
1.
Key Concepts
✔
 Works with binary inputs and outputs  Uses simple decision rule  Negative importance 
✔
✔
✔
implements NOT operation  Acts like a logic gate model  Easy to understand and implement
✔
1.
Conclusion
The McCulloch-Pitts neural network:
Successfully implements the AND-NOT function Uses simple decision logic Demonstrates how 
neurons can perform logical operations
📘 It forms the foundation of neural network concepts.
With a suitable example demonstrate the perceptron learning law with its decision regions using 
python. Give the output in graphical form
import
 numpy 
as np
import
 matplotlib.pyplot 
as plt
X =
 np.random.randn(
50, 2)
y =
 np.array([1 
if x1 +
 x2 > 0 
else -1 
w =
 np.zeros(2)
b = 0
lr = 
0.1
for
 x1, x2 
in X])
for _ 
in range(
for i 
20):
in range(
len
(X)):
if y[i] *
 (np.dot(w, X[i]) +
            w 
+= lr *
 y[i] *
 X[i]
            b 
+= lr *
 y[i]
plt.scatter(X[:, 0
 b) 
<= 0:
], X[:, 1
], c=
y, cmap=
'RdYlGn'
, s=80)
<matplotlib.collections.PathCollection at 0x208832d9f90>
x_vals =
 np.array([-3
if w[1
] != 0:
    y_line = 
, 3])
(w[0]*
x_vals +
 w[1]
    plt.plot(x_vals, y_line, color=
 b) /
'black')
plt.figure()   
# IMPORTANT
plt.scatter(X[:, 0
], X[:, 1
x_vals =
 np.array([-3
if w[1
] != 0:
    y_line = 
], c=
y, cmap=
, 3])
(w[0]*
x_vals +
'RdYlGn'
, s=80)
 w[1]
    plt.plot(x_vals, y_line, color=
 b) /
plt.title(
"Perceptron Classifier")
plt.xlabel(
"X1")
plt.ylabel(
plt.grid()
plt.show()
"X2")
'black')
�
� Perceptron Learning Law & Decision Regions (Theory)
1.
Introduction
A Perceptron is a simple neural network used for classification.
📘 It divides data into two groups:
Class 1 Class 0
In this practical:
The perceptron is trained using a dataset Then it shows how data is separated using a graph
1.
Basic Idea of Learning
The perceptron learns from examples.
Process:
It takes input data Predicts output Compares with correct output If wrong → it adjusts itself
📘 This process is called: Perceptron Learning Law
1.
Learning Behavior At the beginning → predictions may be wrong After training → 
predictions become correct
�
� The model improves step by step by correcting its mistakes.
1.
Example (Conceptual)
Suppose we have input points:
Some belong to Class 0 Some belong to Class 1
📘 The perceptron learns:
How to separate these points
1.
Decision Region Concept
A decision region is the area where:
The perceptron predicts a particular class
📘 The perceptron creates a:
Decision boundary (line)
This line divides the graph into two parts:
One side → Class 0 Other side → Class 1
1.
Graphical Representation
In the output graph:
Points are plotted based on input values Different colors represent different classes A straight 
line separates them
📘 This line is the decision boundary
1.
Training Process
The perceptron follows these steps:
Initialize values Take input data Predict output Compare with actual output Adjust internal 
values if wrong Repeat many times
📘 After training, the boundary becomes correct
1.
Role of Python Program
The Python program:
Takes input dataset Trains perceptron Adjusts weights automatically Plots graph using 
matplotlib
📘 Output graph shows:
Data points Decision boundary
1.
Key Concepts
✔
 Perceptron performs binary classification  Learns using error correction  Creates decision 
✔
✔
✔
boundary  Divides data into decision regions  Graph helps visualize learning
✔
1.
Important Observation
📘 Works only when data is:
Linearly separable
If data cannot be separated by a straight line:
Perceptron will not work properly
1.
Conclusion
The perceptron learning law:
Helps the model learn from errors Adjusts decision boundary Correctly separates data into 
regions
📘 Graphical output clearly shows how the perceptron classifies data.
Write a Python Program using Perceptron Neural Network to recognise even and odd numbers. 
Given numbers are in ASCII form 0 to 9
import numpy as np
def ascii_to_binary(a):
    return np.array([int(i) for i in format(a,'08b')])
def train(x,y):
    w = np.zeros(8)
    b = 0
    for epoch in range (100):
        for xi, t in zip(x,y):
            output = 1 if np.dot(w,xi) + b >= 0 else -1
            if output !=t:
                w = w + t * xi
                b = b + t
    return w,b            
digits = "0123456789"
x = np.array([ascii_to_binary(ord(d)) for d in digits])
x
array([[0, 0, 1, 1, 0, 0, 0, 0],
       [0, 0, 1, 1, 0, 0, 0, 1],
       [0, 0, 1, 1, 0, 0, 1, 0],
       [0, 0, 1, 1, 0, 0, 1, 1],
       [0, 0, 1, 1, 0, 1, 0, 0],
       [0, 0, 1, 1, 0, 1, 0, 1],
       [0, 0, 1, 1, 0, 1, 1, 0],
       [0, 0, 1, 1, 0, 1, 1, 1],
       [0, 0, 1, 1, 1, 0, 0, 0],
       [0, 0, 1, 1, 1, 0, 0, 1]])
y = np.array ([1 if int(d) % 2 == 0 else -1 for d in digits])
w, b = train(x,y)
num = input("Enter a digit (0-9): ")
xi = ascii_to_binary(ord(num))
out = 1 if np.dot(w, xi) + b >= 0 else -1
if out == 1:
    print ("Number is even")
else:
print(
"number is odd")
Enter a digit (0-9):  5
number is odd
📘 Perceptron for Even–Odd Number Recognition (Theory)
1.
Introduction
A Perceptron Neural Network is a simple model used for binary classification.
In this practical, it is used to:
Take numbers from 0 to 9 (in ASCII form) Classify them into: Even numbers Odd numbers
📘 This is a supervised learning problem because correct outputs are already known.
1.
Data Representation Numbers from 0 to 9 are represented using ASCII values These 
ASCII values are used as input to the perceptron
Example:
'0' → 48 '1' → 49 '2' → 50 ... '9' → 57
📘 These numeric values are given to the network as input features.
1.
Target Output
The network is trained with:
Even numbers → Output = 0 Odd numbers → Output = 1
📘 So the perceptron learns to distinguish between two classes.
1.
Working of Perceptron
The perceptron works like a decision unit:
Takes input value (ASCII number) Processes it internally Produces output Compares output with 
correct answer Adjusts itself if output is wrong
📘 This process repeats until it learns correctly.
1.
Learning Process Initially, the perceptron does not know the correct classification It 
makes predictions If prediction is wrong: It adjusts its internal values (weights and bias)
📘 Over time, it improves accuracy
1.
Training Process
The steps followed are:
Provide input data (ASCII values) Assign correct output (even or odd) Predict output Compare 
with actual output Adjust internal parameters Repeat for all inputs Train for multiple cycles
�
� After training, the perceptron can classify correctly.
1.
Decision Making
After training:
The perceptron creates a decision boundary This boundary separates: Even numbers Odd 
numbers
📘 Any new input is classified based on this boundary.
1.
Role of Python Program
The Python program:
Converts numbers into ASCII form Trains the perceptron using given data Adjusts weights 
automatically Predicts whether number is even or odd
📘 It simulates the learning behavior of a neural network.
1.
✔
Key Concepts
 Performs binary classification 
✔
✔
 Uses ASCII numeric input  Learns using repeated training  
Adjusts weights based on error  Creates a decision boundary
✔
1.
Important Observation
📘 Even and odd numbers can be separated easily 📘 So perceptron can learn this classification 
effectively
1.
Conclusion
The perceptron neural network:
Learns to classify numbers into even and odd Uses ASCII values as input Improves through 
training
📘 It demonstrates how neural networks can solve simple classification problems.
✔
Write a python program to design a Hopfield Network which stores 4 vectors
import numpy as np
p1 = np.array([1, -1, 1, -1])
p2 = np.array([1, 1, -1, -1])
p3 = np.array([-1, 1, 1, -1])
p4 = np.array([-1, -1, 1, 1])
patterns = [p1, p2, p3, p4]
n = len(p1)
W = np.zeros((n, n))
for p in patterns:
    W += np.outer(p, p)
# Remove self-connections
np.fill_diagonal(W, 0)
print("Weight Matrix:\n", W)
Weight Matrix:
 [[ 0.  0. -2. -2.]
 [ 0.  0. -2. -2.]
 [-2. -2.  0.  0.]
 [-2. -2.  0.  0.]]
def sign(x):
    return np.where(x >= 0, 1, -1)
# Give noisy input
test = np.array([1, -1, 1, 1])
print("Initial Input:", test)
# Update state
for _ in range(5):
    test = sign(np.dot(W, test))
print("Recovered Pattern:", test)
print("Weight Matrix:\n", W)
Initial Input: [ 1 -1  1  1]
Recovered Pattern: [-1 -1  1  1]
Weight Matrix:
 [[ 0.  0. -2. -2.]
 [ 0.  0. -2. -2.]
 [-2. -2.  0.  0.]
 [-2. -2.  0.  0.]]
�
� Hopfield Network (Storing 4 Vectors) – Theory
1.
Introduction
A Hopfield Network is a type of neural network used for storing and recalling patterns.
📘 It works like a memory system:
Stores patterns (vectors) Recalls them when given a similar or noisy input
In this practical, the network is used to store 4 vectors.
1.
Basic Idea The network remembers multiple patterns When a new input is given: It tries 
to match with stored patterns Gradually updates the input Finally gives the closest 
stored pattern
📘 This is called associative memory
1.
Data Representation Each vector contains values: +1 (active) -1 (inactive)
📘 In your program:
4 vectors are stored Each vector represents a pattern
1.
Storage Process
During training:
All 4 vectors are stored in the network A connection structure (weight matrix) is created This 
matrix represents memory of the network
1.
Working Process
The network works in steps:
A test input is given The network compares it with stored patterns Neuron values are updated 
Updated output is again processed This continues repeatedly
📘 The process stops when output becomes stable
1.
Stability Concept The network keeps updating values When no further change occurs: 
The network reaches a stable state
📘 This stable output is one of the stored vectors
1.
Recall Ability
📘 Important feature:
Even if input is: Noisy Incomplete
The network can still:
Recover the correct stored pattern
1.
Algorithm (Conceptual) Store 4 vectors Create connection matrix Give input pattern 
Update neuron values Repeat updating Stop when stable Output final pattern
2.
Role of Python Program
The Python program:
Stores vectors using arrays Builds memory using connections Updates input using iterative 
process Stops when output stabilizes
📘 It demonstrates pattern storage and recall
1.
✔
Key Concepts
✔
 Works as memory system  Stores multiple patterns  Uses iterative updating  Works with 
bipolar values (+1, -1) 
1.
✔
 Produces stable output
✔
✔
Advantages Can recover noisy patterns Simple to implement Useful in pattern 
recognition
2.
Conclusion
The Hopfield Network:
Stores 4 vectors as memory Recalls correct pattern from input Updates values until stable result 
is achieved
📘 It shows how neural networks can act like a content-addressable memory system.
Write a python Program for Bidirectional Associative Memory with two pairs of vectors.
import numpy as np
x = np.array ([
    [1,-1,1],
    [-1,1,-1]
])
y = np.array ([
    [1,1,-1],
    [-1,-1,1]
])
w = np.dot(x.T,y)
def recall (input_vector, weight_matrix, is_forward=True):
    output = np.sign(np.dot(input_vector, weight_matrix))
    output[output == 0]=1
    return output
test_x = np.array([[1,-1,1]])
recalled_y = recall(test_x, w, is_forward=True)
print ("Recalled y for given x:", recalled_y)
Recalled y for given x: [[ 1  1 -1]]
test_y = np.array([[1,1,-1]])
recalled_x = recall(test_y, w.T, is_forward=False)
print("Recalled x for given y:", recalled_x)
Recalled x for given y: [[ 1 -1  1]]
📘 Bidirectional Associative Memory (BAM) – Theory
1. Introduction
Bidirectional Associative Memory (BAM) is a type of neural network used to store and recall 
paired patterns.
📘 Unlike simple networks:
It does not store single data It stores pairs of related data
Example:
One pattern is linked with another pattern
1. Basic Idea
In BAM, we store relationships like:
�
� Pattern X is associated with Pattern Y
So:
If X is given → network recalls Y If Y is given → network recalls X
📘 This is why it is called bidirectional
1.
Data Representation Data is stored in pairs: (X1 
↔
 Y1) (X2 
�
� Each pair represents a connection between two patterns
Values are usually:
+1 (active) -1 (inactive)
1.
Working Concept
The network works in two directions:
↔
(1) Forward Direction Input X is given Network produces output Y
(2) Backward Direction Input Y is given Network produces output X
📘 Both directions work using the same stored relationship
1.
Learning Process
During training:
 Y2)
Each pair of vectors is stored in the network Connections are formed between X and Y
📘 These connections help in recalling patterns later
1.
Recall Process
When input is given:
Network compares it with stored patterns Produces corresponding pair Output is refined step by 
step
📘 Process continues until output becomes stable
1.
Iterative Nature
BAM works iteratively:
Output is updated again and again Each update improves matching Stops when no change 
occurs
📘 This final result is called stable state
1.
2.
Algorithm (Conceptual) Store two pairs of vectors Create connections between them 
Give input pattern Generate output in one direction Feed output back in opposite 
direction Repeat updating Stop when stable
Role of Python Program
The Python program:
Stores vector pairs Creates weight connections Performs forward and backward updates Uses 
iteration to reach stable output
📘 It shows how patterns are associated and recalled
1.
✔
Key Concepts
 Stores paired patterns 
output 
✔
✔
 Works in two directions 
 Acts as associative memory
1.
✔
 Uses iterative updating 
✔
 Reaches stable 
Advantages Can recall data from partial input Works in both directions Useful for pattern 
association
2.
Conclusion
Bidirectional Associative Memory:
Stores relationships between patterns Recalls data in forward and backward direction Uses 
iterative process to reach correct output
📘 It is useful in applications where two types of data are linked together.
Write a python program to illustrate ART neural network
import numpy as np
data = np.array([
    [1, 1, 0, 0],
    [1, 1, 1, 0],
    [0, 0, 1, 1],
    [1, 0, 0, 0]
])
rho = 0.7
cluster = []
for sample in data:
    print("\nInput:", sample)
    
    # First cluster
    if len(cluster) == 0:
        cluster.append(sample.copy())
        print("Created Cluster 1")
        continue
    found = False
    for i in range(len(cluster)):
        w = cluster[i]
        match = np.sum(np.minimum(sample, w)) / np.sum(sample)
        print("Match with cluster", i+1, "=", round(match, 2))
        if match >= rho:
            print("Added to cluster", i+1)
            cluster[i] = np.minimum(w, sample)
            found = True
            break
    if not found:
        cluster.append(sample.copy())
        print("New Cluster Created")
Input: [1 1 0 0]
Created Cluster 1
Input: [1 1 1 0]
Match with cluster 1 = 0.67
New Cluster Created
Input: [0 0 1 1]
Match with cluster 1 = 0.0
Match with cluster 2 = 0.5
New Cluster Created
Input: [1 0 0 0]
Match with cluster 1 = 1.0
Added to cluster 1
print("
\n
Final Clusters:")
for i 
in range(
len
(cluster)):
print(
"Cluster"
, i+1
Final Clusters:
Cluster 1 : [1 0 0 0]
Cluster 2 : [1 1 1 0]
Cluster 3 : [0 0 1 1]
, ":"
, cluster[i])
📘 ART Neural Network (Theory)
1.
Introduction
Adaptive Resonance Theory (ART) is a neural network used for pattern recognition and 
clustering.
📘 It groups similar inputs into categories and can learn continuously without forgetting previous 
knowledge.
1.
Main Idea
ART network works by:
Receiving an input pattern Comparing it with stored patterns Deciding whether it matches an 
existing category Or creating a new category
📘 This makes it useful for unsupervised learning
1.
Important Feature
The most important concept in ART is:
📘 Vigilance Parameter
It controls how strict the matching should be High value → very strict (more categories) Low 
value → less strict (fewer categories)
1.
Working Process
The ART network works in steps:
Input pattern is given Network compares it with stored categories If it matches: Category is 
updated If it does not match: New category is created
1.
Matching and Learning
�
� If similarity is high:
The network accepts the pattern Learning occurs (called resonance)
📘 If similarity is low:
The category is rejected Search continues
1.
Stability–Plasticity Balance
ART solves an important problem:
Stability → remembers old patterns Plasticity → learns new patterns
📘 It maintains balance between both
1.
2.
Training Process Initialize categories Give input patterns one by one Compare with 
existing categories Check similarity Accept or reject Update or create new category 
Repeat for all inputs
Role of Python Program
The Python program:
Takes input data Compares patterns Uses vigilance parameter Groups data into clusters Creates 
new clusters when needed
1.
✔
Key Concepts
 Used for clustering and pattern recognition 
✔
✔
 Works in unsupervised learning  Uses 
vigilance parameter  Learns continuously  Avoids forgetting old data
✔
1.
✔
Advantages Learns new data without losing old knowledge Flexible and adaptive 
Suitable for real-time applications
2.
Conclusion
ART neural network:
Groups similar patterns Adapts to new data Maintains balance between learning and memory
📘 It is useful in systems where continuous learning is required.
Implement Artificial Neural Network training process in Python by using Forward Propagation, 
Back Propagation.
import numpy as np
def sigmoid(x):
    return 1 / (1 + np.exp(-x))
def sigmoid_derivative(x):
    return x * (1 - x)
X = np.array([[0, 0],
              [0, 1],
              [1, 0],
              [1, 1]])
y = np.array([[0],
              [1],
              [1],
              [0]])
np.random.seed(0)
W1 = np.random.uniform(-1, 1, (2, 2))
W2 = np.random.uniform(-1, 1, (2, 1))
b1 = np.zeros((1, 2))
b2 = np.zeros((1, 1))
lr = 0.5
def forward_propagation(X):
    hidden_input = np.dot(X, W1) + b1
    hidden_output = sigmoid(hidden_input)
    final_input = np.dot(hidden_output, W2) + b2
    final_output = sigmoid(final_input)
    return hidden_input, hidden_output, final_input, final_output
def backward_propagation(X, y, hidden_output, final_output):
    global W1, W2, b1, b2
    error = y - final_output
    d_output = error * sigmoid_derivative(final_output)
    hidden_error = d_output.dot(W2.T)
    d_hidden = hidden_error * sigmoid_derivative(hidden_output)
    W2 += lr * hidden_output.T.dot(d_output)
    W1 += lr * X.T.dot(d_hidden)
    b2 += lr * np.sum(d_output, axis=0, keepdims=True)
    b1 += lr * np.sum(d_hidden, axis=0, keepdims=True)
for epoch in range(10000):
    hidden_input, hidden_output, final_input, final_output = 
forward_propagation(X)
    
    backward_propagation(X, y, hidden_output, final_output)
    if epoch % 1000 == 0:
        loss = np.mean(np.square(y - final_output))
        print(f"Epoch {epoch}: Loss = {loss:.5f}")
Epoch 0: Loss = 0.25042
Epoch 1000: Loss = 0.24337
Epoch 2000: Loss = 0.00788
Epoch 3000: Loss = 0.00222
Epoch 4000: Loss = 0.00124
Epoch 5000: Loss = 0.00085
Epoch 6000: Loss = 0.00065
Epoch 7000: Loss = 0.00052
Epoch 8000: Loss = 0.00043
Epoch 9000: Loss = 0.00037
_, _, _, final_output = forward_propagation(X)
print("\nFinal outputs after training:")
print(final_output)
Final outputs after training:
[[0.01984931]
 [0.98285981]
 [0.9828567 ]
 [0.01775138]]
📘 Artificial Neural Network Training (Forward & Back Propagation)
1. Introduction
An Artificial Neural Network (ANN) is a system that learns from data and makes predictions.
Training an ANN means: 📘 Teaching the network to give correct output for given input
This learning happens using two main steps:
Forward Propagation Back Propagation
1. Structure of ANN
An ANN consists of:
(1) Input Layer Receives input data
(2) Hidden Layer(s) Processes data and finds patterns
(3) Output Layer Produces final result
Connections between neurons have weights that control how important each input is.
1.
Forward Propagation
Forward propagation is the prediction step.
Process:
Input data is passed through the network Each layer processes the data Output is generated
📘 Data always moves in one direction (forward)
1.
Output and Error
After prediction:
The output is compared with the correct answer
📘 If output is wrong:
An error is calculated
This error shows how much the prediction needs improvement.
1.
Back Propagation
Back propagation is the learning step.
Process:
Error is sent backward through the network Each layer adjusts its weights Goal is to reduce the 
error
📘 This helps the network learn from mistakes
1.
Training Process
The complete training includes:
Initialize weights randomly Perform forward propagation Generate output Compare with 
correct output Calculate error Perform back propagation Update weights Repeat many times
📘 With each cycle, accuracy improves
1.
Learning Behavior
During training:
Error decreases step by step Output becomes closer to correct answer
After training:
Network can predict correctly for new inputs
1.
Role of Python Program
The Python program:
Simulates the ANN model Performs forward propagation Calculates error Applies back 
propagation Updates weights repeatedly
📘 It shows how the network learns automatically
1.
✔
Key Concepts
✔
 Forward propagation → makes prediction  Back propagation → corrects mistakes  Training 
✔
happens in multiple iterations 
prediction
1.
Conclusion
✔
 Network improves over time  Used for classification and 
✔
ANN training using forward and back propagation allows the network to:
Learn from data Reduce errors Improve performance
📘 This process is the foundation of modern machine learning and deep learning systems.
Write a python program in python program for creating a Back Propagation Feed-forward 
neural network
import numpy as np
X = np.array([[0, 0],
              [0, 1],
              [1, 0],
              [1, 1]])
y = np.array([[0],
              [1],
              [1],
              [1]])
input_neurons = 2
hidden_neurons = 2
output_neurons = 1
np.random.seed(1)
W1 = np.random.randn(input_neurons, hidden_neurons)
W2 = np.random.randn(hidden_neurons, output_neurons)
def sigmoid(x):
    return 1 / (1 + np.exp(-x))
def sigmoid_derivative(x):
    return x * (1 - x)
epochs = 10000
lr = 0.1
for i in range(epochs):
    hidden_input = np.dot(X, W1)
    hidden_output = sigmoid(hidden_input)
    final_input = np.dot(hidden_output, W2)
    final_output = sigmoid(final_input)
    error = y - final_output
    d_output = error * sigmoid_derivative(final_output)
    error_hidden = d_output.dot(W2.T)
    d_hidden = error_hidden * sigmoid_derivative(hidden_output)
    W2 += hidden_output.T.dot(d_output) * lr
    W1 += X.T.dot(d_hidden) * lr
print("Final Output:")
print(final_output)
Final Output:
[[0.06156428]
 [0.96693118]
 [0.9678494 ]
 [0.98080152]]
📘 Back Propagation Feed-Forward Neural Network (Theory)
1. Introduction
A Feed-Forward Neural Network (FFNN) is a type of artificial neural 
network where data flows in only one direction:
From input layer → hidden layer → output layer
There is no looping or feedback, which makes it simple and easy to 
understand.
When this network is trained using an error-correction method, it is 
called a:
📘 Back Propagation Neural Network
2. Structure of the Network
The network is made up of three main parts:
(1) Input Layer
Takes input data from the user or dataset
(2) Hidden Layer(s)
Performs processing
Extracts patterns and features
(3) Output Layer
Produces final result or prediction
Each connection between neurons has:
A weight (importance of input)
A bias (adjustment value)
3. Forward Propagation (Data Flow)
Forward propagation is the process where:
Input data is passed through the network
Each layer processes the data
Output is generated at the final layer
📘 This is simply the prediction step
4. Error Calculation
After getting the output:
The network compares it with the correct answer (target)
📘 If output is wrong:
An error is generated
This error shows how far the network is from the correct result.
5. Back Propagation (Learning Step)
Backpropagation is the process of:
📘 Sending the error backward through the network
Starts from output layer
Moves toward hidden layer
Adjusts weights to reduce error
📘 This helps the network learn from its mistakes
6. Training Process
The complete training works like this:
Initialize weights randomly
Perform forward propagation
Generate output
Compare with correct output
Calculate error
Apply backpropagation
Update weights
Repeat many times
📘 With each iteration, the network improves
7. Role of Activation Function
Activation function:
Decides whether a neuron should activate or not
Helps the network learn complex patterns
Without it, the network cannot solve real-world problems.
8. Important Characteristics
✔ Data flows in one direction only
✔ Learning happens using error correction
✔ Uses hidden layers 
for
 processing
✔ Improves accuracy over time
✔ Requires multiple training iterations
9.
 Advantages
Can learn 
complex
Widely used 
 relationships
in
 machine learning 
and AI
Gives accurate results after training
10.
 Conclusion
A Back Propagation Feed
Forward Neural Network:
Makes predictions using forward flow
Learns by correcting errors using backward flow
Improves continuously 
with
 training
📘 It is
 one of the most important 
models.
and
 widely used neural network 
implement an ann in python to learn the behaviour of an AND gate using forward propagation 
and back propagation
import numpy as np
x = np.array([[0, 0],
              [0, 1],
              [1, 0],
              [1, 1]])
y = np.array([[0],
              [0],
              [0],
              [1]])
input_neu = 2
hidden_neu = 2
out_neu = 1
np.random.seed(1)
w1 = np.random.randn(input_neu, hidden_neu)
w2 = np.random.randn(hidden_neu, out_neu)
def sigmoid(x):
    return 1 / (1 + np.exp(-x))
def sigmoid_derivative(x):
    return x * (1 - x)
epoch = 10000
lr = 0.1
for i in range(epoch):
    Hidden_input = np.dot(x, w1)
    Hidden_output = sigmoid(Hidden_input)
    final_input = np.dot(Hidden_output, w2)
    final_output = sigmoid(final_input)
    error = y - final_output
    d_output = error * sigmoid_derivative(final_output)
    Hidden_error = d_output.dot(w2.T)
    d_Hidden = Hidden_error * sigmoid_derivative(Hidden_output)
    w2 += Hidden_output.T.dot(d_output) * lr
    w1 += x.T.dot(d_Hidden) * lr
print("The final output is:\n", final_output)
The final output is:
 [[0.01594596]
 [0.105487  ]
 [0.07964549]
 [0.90435953]]
📘 ANN for AND Gate using Forward & Back Propagation (Theory)
1.
Introduction
An Artificial Neural Network (ANN) can be trained to learn logical operations like the AND gate.
📘 In this practical:
The network learns input-output behavior of AND gate Training is done using: Forward 
Propagation (prediction) Back Propagation (learning)
1.
AND Gate Behavior
The AND gate works as:
Output is 1 only when both inputs are 1 Otherwise output is 0
📘 This behavior is given to the network as training data.
1.
Network Structure
The ANN used has:
(1) Input Layer Takes two inputs (X1, X2)
(2) Hidden Layer Processes input and learns pattern
(3) Output Layer Produces final result (0 or 1)
1.
Forward Propagation (Prediction Step)
In this step:
Inputs are passed through the network Each layer processes the data Output is generated
📘 This is how the network makes a prediction.
1.
Error Calculation
After prediction:
Output is compared with actual AND gate output
📘 If prediction is wrong:
Error is generated
This error tells the network how much it needs to improve.
1.
Back Propagation (Learning Step)
Back propagation is used to: 📘 Correct the error
Process:
Error is sent backward through the network Weights are adjusted Output becomes closer to 
correct value
1.
Training Process
The ANN follows these steps:
Initialize weights randomly Perform forward propagation Generate output Compare with actual 
output Calculate error Perform back propagation Update weights Repeat multiple times
📘 With each iteration, accuracy improves.
1.
Learning Behavior Initially, network gives wrong outputs After training, it learns correct 
AND logic
📘 Finally:
It predicts correct output for all inputs
1.
Role of Python Program
The Python program:
Defines input and output of AND gate Builds neural network Performs forward propagation 
Applies back propagation Trains the network over iterations
📘 It shows how ANN learns logical operations.
1.
✔
Key Concepts
✔
 ANN learns from training data  Forward propagation → prediction  Back propagation → 
error correction 
✔
✔
✔
 Training improves accuracy  Works well for simple logic like AND
1.
Conclusion
The ANN successfully learns AND gate behavior by:
Using forward propagation for prediction Using back propagation to reduce error
📘 It demonstrates how neural networks can learn logical relationships from data.
TensorFlow/Pytorch implementation of CNN
import tensorflow as tf
from tensorflow.keras import datasets, layers, models
import matplotlib.pyplot as plt
(x_train, y_train), (x_test, y_test) = datasets.cifar10.load_data()
x_train = x_train / 255.0
x_test = x_test / 255.0
C:\Users\shash\AppData\Local\Packages\
PythonSoftwareFoundation.Python.3.11_qbz5n2kfra8p0\LocalCache\local
packages\Python311\site-packages\keras\src\datasets\cifar.py:18: 
VisibleDeprecationWarning: dtype(): align should be passed as Python 
or NumPy boolean but got `align=0`. Did you mean to pass a tuple to 
create a subarray type? (Deprecated NumPy 2.4)
  d = cPickle.load(f, encoding="bytes")
model = models.Sequential()
model.add(layers.Input(shape=(32,32,3)))
# 1st Layer
model.add(layers.Conv2D(32,(3,3),padding='same',activation='relu'))
model.add(layers.MaxPooling2D((2,2)))
# 2nd Layer
model.add(layers.Conv2D(64,(3,3),padding='same',activation='relu'))
model.add(layers.MaxPooling2D((2,2)))
# 3rd Layer
model.add(layers.Conv2D(128,(3,3),padding='same',activation='relu'))
model.add(layers.MaxPooling2D((2,2)))
# Fully Connected
model.add(layers.Flatten())
model.add(layers.Dense(128,activation='relu'))
model.add(layers.Dense(128,activation='relu'))
model.add(layers.Dense(10,activation='softmax'))
model.summary()
Model: "sequential"
┏━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┳━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┳
━━━━━━━━━━━━━━━━━┓
┃ Layer (type)                         ┃ Output Shape                ┃ 
Param # ┃
┡━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━╇━━━━━━━━━━━━━━━━━━━━━━━━━━━━━╇
━━━━━━━━━━━━━━━━━┩
│ conv2d (Conv2D)                      │ (None, 32, 32, 32)          │ 
896 │
├──────────────────────────────────────┼─────────────────────────────┼
─────────────────┤
│ max_pooling2d (MaxPooling2D)         │ (None, 16, 16, 32)          │ 
0 │
├──────────────────────────────────────┼─────────────────────────────┼
─────────────────┤
│ conv2d_1 (Conv2D)                    │ (None, 16, 16, 64)          │ 
18,496 │
├──────────────────────────────────────┼─────────────────────────────┼
─────────────────┤
│ max_pooling2d_1 (MaxPooling2D)       │ (None, 8, 8, 64)            │ 
0 │
├──────────────────────────────────────┼─────────────────────────────┼
─────────────────┤
│ conv2d_2 (Conv2D)                    │ (None, 8, 8, 128)           │ 
73,856 │
├──────────────────────────────────────┼─────────────────────────────┼
─────────────────┤
│ max_pooling2d_2 (MaxPooling2D)       │ (None, 4, 4, 128)           │ 
0 │
├──────────────────────────────────────┼─────────────────────────────┼
─────────────────┤
│ flatten (Flatten)                    │ (None, 2048)                │ 
0 │
├──────────────────────────────────────┼─────────────────────────────┼
─────────────────┤
│ dense (Dense)                        │ (None, 128)                 │ 
262,272 │
├──────────────────────────────────────┼─────────────────────────────┼
─────────────────┤
│ dense_1 (Dense)                      │ (None, 128)                 │ 
16,512 │
├──────────────────────────────────────┼─────────────────────────────┼
─────────────────┤
│ dense_2 (Dense)                      │ (None, 10)                  │ 
1,290 │
└──────────────────────────────────────┴─────────────────────────────┴
─────────────────┘
 Total params: 373,322 (1.42 MB)
 Trainable params: 373,322 (1.42 MB)
 Non-trainable params: 0 (0.00 B)
model.compile(
    optimizer='adam',
    loss='sparse_categorical_crossentropy',
    metrics=['accuracy']
)
WARNING:tensorflow:TensorFlow GPU support is not available on native 
Windows for TensorFlow >= 2.11. Even if CUDA/cuDNN are installed, GPU 
will not be used. Please use WSL2 or the TensorFlow-DirectML plugin.
history = model.fit(
    x_train, y_train,
    epochs=10,
    validation_data=(x_test, y_test)
)
Epoch 1/10
1563/1563 ━━━━━━━━━━━━━━━━━━━━ 17s 10ms/step - accuracy: 0.4757 - 
loss: 1.4381 - val_accuracy: 0.6157 - val_loss: 1.0686
Epoch 2/10
1563/1563 ━━━━━━━━━━━━━━━━━━━━ 14s 9ms/step - accuracy: 0.6513 - loss: 
0.9823 - val_accuracy: 0.6785 - val_loss: 0.9107
Epoch 3/10
1563/1563 ━━━━━━━━━━━━━━━━━━━━ 14s 9ms/step - accuracy: 0.7121 - loss: 
0.8158 - val_accuracy: 0.6936 - val_loss: 0.8714
Epoch 4/10
1563/1563 ━━━━━━━━━━━━━━━━━━━━ 16s 10ms/step - accuracy: 0.7536 - 
loss: 0.7010 - val_accuracy: 0.7104 - val_loss: 0.8454
Epoch 5/10
1563/1563 ━━━━━━━━━━━━━━━━━━━━ 15s 9ms/step - accuracy: 0.7841 - loss: 
0.6138 - val_accuracy: 0.7205 - val_loss: 0.8317
Epoch 6/10
1563/1563 ━━━━━━━━━━━━━━━━━━━━ 15s 9ms/step - accuracy: 0.8127 - loss: 
0.5348 - val_accuracy: 0.7360 - val_loss: 0.7985
Epoch 7/10
1563/1563 ━━━━━━━━━━━━━━━━━━━━ 15s 9ms/step - accuracy: 0.8326 - loss: 
0.4719 - val_accuracy: 0.7382 - val_loss: 0.8111
Epoch 8/10
1432/1563 ━━━━━━━━━━━━━━━━━━━━ 1s 8ms/step - accuracy: 0.8622 - loss: 
0.3860
test_loss, test_acc = model.evaluate(x_test, y_test)
print("Test Accuracy:", test_acc)
prediction = model.predict(x_test[0].reshape(1,32,32,3))
predicted_class = tf.argmax(prediction[0]).numpy()
actual_class = y_test[0][0]
print("Predicted class:", predicted_class)
print("Actual class:", actual_class)
plt.imshow(x_test[10])
plt.title(f"Predicted: {predicted_class}")
plt.axis(
'off')
plt.show()
📘 CNN using TensorFlow / PyTorch (Theory)
1.
Introduction
A Convolutional Neural Network (CNN) is a type of deep learning model mainly used for:
Image recognition Object detection Pattern identification
📘 Frameworks like TensorFlow and PyTorch are used to implement CNN easily in Python.
1.
Basic Idea of CNN
CNN works by:
Taking an image as input Extracting important features Classifying the image
📘 It automatically learns patterns like:
Edges Shapes Objects
1.
Main Layers in CNN
(1) Convolution Layer Applies filters to the image Detects features like edges and textures
(2) Activation Function Adds non-linearity Helps the network learn complex patterns
(3) Pooling Layer Reduces size of data Keeps important features Makes computation faster
(4) Fully Connected Layer Takes extracted features Produces final output (classification)
1.
2.
Working Process Input image is given Convolution layer extracts features Activation 
function is applied Pooling reduces data size Process repeats for deeper layers Fully 
connected layer gives output
Training Process
CNN is trained using:
Forward propagation → generates output Back propagation → corrects errors
📘 The network improves after multiple iterations.
1.
2.
TensorFlow vs PyTorch TensorFlow: Developed by Google Easy for deployment Used in 
production systems PyTorch: Developed by Meta More flexible and easy to debug 
Popular in research
Role of Python Program
The Python implementation:
Loads dataset (images) Builds CNN model using layers Trains model using data Tests model 
accuracy
📘 Both TensorFlow and PyTorch provide built-in functions to simplify this process.
1.
Applications of CNN Face recognition Image classification Medical image analysis Self
driving cars Object detection
2.
✔
Key Concepts
✔
 CNN is used for image processing  Automatically extracts features  Uses multiple layers  
✔
✔
Trained using forward & back propagation  Implemented using TensorFlow or PyTorch
1.
✔
Advantages High accuracy in image tasks Automatic feature extraction Works well with 
large datasets
2.
Conclusion
CNN implemented using TensorFlow or PyTorch:
Helps in solving image-based problems Learns patterns automatically Provides powerful deep 
learning solutions
📘 It is one of the most important models in modern AI.
MNIST Handwritten Character Detection using PyTorch, Keras and Tensorflow
import tensorflow as tf
from tensorflow.keras import datasets, layers, models
import matplotlib.pyplot as plt
(x_train, y_train), (x_test, y_test) = datasets.mnist.load_data()
x_train = x_train / 255.0
x_test = x_test / 255.0
# reshape to CNN format (IMPORTANT)
x_train = x_train.reshape(-1, 28, 28, 1)
x_test = x_test.reshape(-1, 28, 28, 1)
Downloading data from https://storage.googleapis.com/tensorflow/tf
keras-datasets/mnist.npz
11490434/11490434 ━━━━━━━━━━━━━━━━━━━━ 6s 1us/step
model = models.Sequential()
model.add(layers.Input(shape=(28,28,1)))
# 1st Layer
model.add(layers.Conv2D(32,(3,3),padding='same',activation='relu'))
model.add(layers.MaxPooling2D((2,2)))
# 2nd Layer
model.add(layers.Conv2D(64,(3,3),padding='same',activation='relu'))
model.add(layers.MaxPooling2D((2,2)))
# 3rd Layer
model.add(layers.Conv2D(128,(3,3),padding='same',activation='relu'))
model.add(layers.MaxPooling2D((2,2)))
# Fully Connected
model.add(layers.Flatten())
model.add(layers.Dense(128,activation='relu'))
model.add(layers.Dense(128,activation='relu'))
model.add(layers.Dense(10,activation='softmax'))
model.summary()
Model: "sequential"
┏━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┳━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┳
━━━━━━━━━━━━━━━━━┓
┃ Layer (type)                         ┃ Output Shape                ┃ 
Param # ┃
┡━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━╇━━━━━━━━━━━━━━━━━━━━━━━━━━━━━╇
━━━━━━━━━━━━━━━━━┩
│ conv2d (Conv2D)                      │ (None, 28, 28, 32)          │ 
320 │
├──────────────────────────────────────┼─────────────────────────────┼
─────────────────┤
│ max_pooling2d (MaxPooling2D)         │ (None, 14, 14, 32)          │ 
0 │
├──────────────────────────────────────┼─────────────────────────────┼
─────────────────┤
│ conv2d_1 (Conv2D)                    │ (None, 14, 14, 64)          │ 
18,496 │
├──────────────────────────────────────┼─────────────────────────────┼
─────────────────┤
│ max_pooling2d_1 (MaxPooling2D)       │ (None, 7, 7, 64)            │ 
0 │
├──────────────────────────────────────┼─────────────────────────────┼
─────────────────┤
│ conv2d_2 (Conv2D)                    │ (None, 7, 7, 128)           │ 
73,856 │
├──────────────────────────────────────┼─────────────────────────────┼
─────────────────┤
│ max_pooling2d_2 (MaxPooling2D)       │ (None, 3, 3, 128)           │ 
0 │
├──────────────────────────────────────┼─────────────────────────────┼
─────────────────┤
│ flatten (Flatten)                    │ (None, 1152)                │ 
0 │
├──────────────────────────────────────┼─────────────────────────────┼
─────────────────┤
│ dense (Dense)                        │ (None, 128)                 │ 
147,584 │
├──────────────────────────────────────┼─────────────────────────────┼
─────────────────┤
│ dense_1 (Dense)                      │ (None, 128)                 │ 
16,512 │
├──────────────────────────────────────┼─────────────────────────────┼
─────────────────┤
│ dense_2 (Dense)                      │ (None, 10)                  │ 
1,290 │
└──────────────────────────────────────┴─────────────────────────────┴
─────────────────┘
 Total params: 258,058 (1008.04 KB)
 Trainable params: 258,058 (1008.04 KB)
 Non-trainable params: 0 (0.00 B)
model.compile(
    optimizer='adam',
    loss='sparse_categorical_crossentropy',
    metrics=['accuracy']
)
WARNING:tensorflow:TensorFlow GPU support is not available on native 
Windows for TensorFlow >= 2.11. Even if CUDA/cuDNN are installed, GPU 
will not be used. Please use WSL2 or the TensorFlow-DirectML plugin.
history = model.fit(
    x_train, y_train,
    epochs=10,
    validation_data=(x_test, y_test)
)
Epoch 1/10
1875/1875 ━━━━━━━━━━━━━━━━━━━━ 17s 8ms/step - accuracy: 0.9573 - loss: 
0.1373 - val_accuracy: 0.9869 - val_loss: 0.0415
Epoch 2/10
1875/1875 ━━━━━━━━━━━━━━━━━━━━ 15s 8ms/step - accuracy: 0.9858 - loss: 
0.0450 - val_accuracy: 0.9886 - val_loss: 0.0340
Epoch 3/10
1875/1875 ━━━━━━━━━━━━━━━━━━━━ 15s 8ms/step - accuracy: 0.9898 - loss: 
0.0328 - val_accuracy: 0.9919 - val_loss: 0.0248
Epoch 4/10
1875/1875 ━━━━━━━━━━━━━━━━━━━━ 15s 8ms/step - accuracy: 0.9927 - loss: 
0.0240 - val_accuracy: 0.9855 - val_loss: 0.0476
Epoch 5/10
1875/1875 ━━━━━━━━━━━━━━━━━━━━ 15s 8ms/step - accuracy: 0.9938 - loss: 
0.0206 - val_accuracy: 0.9904 - val_loss: 0.0322
Epoch 6/10
1875/1875 ━━━━━━━━━━━━━━━━━━━━ 15s 8ms/step - accuracy: 0.9943 - loss: 
0.0182 - val_accuracy: 0.9925 - val_loss: 0.0242
Epoch 7/10
1875/1875 ━━━━━━━━━━━━━━━━━━━━ 15s 8ms/step - accuracy: 0.9956 - loss: 
0.0144 - val_accuracy: 0.9927 - val_loss: 0.0233
Epoch 8/10
1875/1875 ━━━━━━━━━━━━━━━━━━━━ 15s 8ms/step - accuracy: 0.9962 - loss: 
0.0125 - val_accuracy: 0.9922 - val_loss: 0.0265
Epoch 9/10
1875/1875 ━━━━━━━━━━━━━━━━━━━━ 15s 8ms/step - accuracy: 0.9966 - loss: 
0.0116 - val_accuracy: 0.9905 - val_loss: 0.0360
Epoch 10/10
1875/1875 ━━━━━━━━━━━━━━━━━━━━ 15s 8ms/step - accuracy: 0.9967 - loss: 
0.0110 - val_accuracy: 0.9908 - val_loss: 0.0347
test_loss, test_acc = model.evaluate(x_test, y_test)
print("Test Accuracy:", test_acc)
313/313 ━━━━━━━━━━━━━━━━━━━━ 1s 4ms/step - accuracy: 0.9908 - loss: 
0.0347
Test Accuracy: 0.9908000230789185
prediction =
 model.predict(x_test[0
].reshape(1,
28,28,1
))
predicted_class =
 tf.argmax(prediction[0
]).numpy()
actual_class =
 y_test[0]
print(
"Predicted class:"
, predicted_class)
print(
"Actual class:"
, actual_class)
1/1 ━━━━━━━━━━━━━━━━━━━━ 0s 132ms/step
Predicted class: 7
Actual class: 7
plt.imshow(x_test[0
], cmap=
plt.title(
'gray')
f"Predicted: {
predicted_class}")
plt.axis(
'off')
plt.show()
📘 MNIST Handwritten Digit Detection (Theory)
1.
Introduction
MNIST Handwritten Digit Detection is a popular deep learning task where a model learns to 
recognize handwritten digits from images.
📘 The dataset used is MNIST dataset, which contains:
Images of digits from 0 to 9 Each image is small (28×28 pixels) Used for training and testing 
models
1.
Objective
The goal is:
Take an image of a handwritten digit Predict which digit it represents (0–9)
📘 This is an image classification problem
1.
Frameworks Used
(1) TensorFlow Developed by Google Widely used for production
(2) Keras High-level API built on TensorFlow Easy to use for beginners
(3) PyTorch Developed by Meta Flexible and popular in research
1.
Working Process
The system works in steps:
Load MNIST dataset Preprocess images (normalize, reshape) Build neural network model Train 
model using training data Test model using unseen data Predict output (digit)
1.
Model Used
Usually, a Convolutional Neural Network (CNN) is used because:
It works well with images Automatically extracts features
1.
Training Process
During training:
Images are given to model Model predicts output Prediction is compared with correct label Error 
is calculated Model improves using learning process
📘 This repeats for many iterations until accuracy improves.
1.
Testing and Prediction
After training:
Model is tested on new images It predicts digits it has never seen before
📘 High accuracy can be achieved (around 95%+)
1.
Role of Python Program
The Python implementation:
Loads dataset using libraries Builds CNN model Trains model Evaluates performance Displays 
predictions
📘 Each framework (TensorFlow, Keras, PyTorch) provides tools to simplify this.
1.
Key Concepts
✔
✔
 Image classification problem  Uses MNIST dataset  CNN is commonly used  Training 
✔
✔
improves accuracy  Frameworks simplify implementation
1.
✔
Applications Digit recognition (bank cheques, forms) Postal code reading Handwriting 
recognition systems Document processing
2.
Conclusion
MNIST digit detection:
Demonstrates how deep learning models recognize images Uses powerful frameworks like 
TensorFlow, Keras, and PyTorch Provides a foundation for advanced image processing systems
📘 It is one of the most important beginner projects in deep learning.
