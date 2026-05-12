# Developing a Neural Network Regression Model

## AIM
To develop a neural network regression model for the given dataset.

## THEORY
Explain the problem statement

## Neural Network Model
Include the neural network model diagram.

## DESIGN STEPS
### STEP 1: 

Create your dataset in a Google sheet with one numeric input and one numeric output.

### STEP 2: 

Split the dataset into training and testing

### STEP 3: 

Create MinMaxScalar objects ,fit the model and transform the data.

### STEP 4: 

Build the Neural Network Model and compile the model.

### STEP 5: 

Train the model with the training data.

### STEP 6: 

Plot the performance plot

### STEP 7: 

Evaluate the model with the testing data.

### STEP 8: 

Use the trained model to predict  for a new input value .

## PROGRAM

### Name: ABISHEIK RAJ J

### Register Number: 212224230006

```python
class NeuralNet(nn.Module):
    def __init__(self):
        super().__init__()
        #Include your code here
        super().__init__()
        self.fc1 = nn.Linear(1,8)
        self.fc2 = nn.Linear(8,10)
        self.fc3 = nn.Linear(10,1)
        self.relu=nn.ReLU()
        self.history={'loss':[]}

# Initialize the Model, Loss Function, and Optimizer

def forward(self,x):
        x=self.relu(self.fc1(x))
        x=self.relu(self.fc2(x))
        x=self.fc3(x)
        return x
lig = NeuralNet ()
criterion = nn. MSELoss()
optimizer = optim.RMSprop (lig.parameters(), lr=0.001)


def train_model(ai_brain, X_train, y_train, criterion, optimizer, epochs=2000):
    #Include your code here
    for epoch in range(epochs):
        optimizer.zero_grad()
        loss = criterion(ai_brain(X_train), y_train)
        loss.backward()
        optimizer.step()
        lig.history['loss'].append(loss.item())
        if epoch % 200 == 0:
            print(f'Epoch [{epoch}/{epochs}], Loss: {loss.item():.6f}')

```

### Dataset Information
Include screenshot of the generated data
<img width="267" height="270" alt="image" src="https://github.com/user-attachments/assets/6abb941a-9f86-47bd-ac7c-918998ccfd87" />

### OUTPUT

### Training Loss Vs Iteration Plot
Include your plot here

### New Sample Data Prediction
Include your sample input and output here
<img width="726" height="572" alt="image" src="https://github.com/user-attachments/assets/1297c756-78ae-4a68-9326-70176b8a3a91" />

## RESULT
Thus, a neural network regression model was successfully developed and trained using PyTorch.
