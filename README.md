**Time Series Analysis**  
A time series consists of a sequence of measurements taken at consistent intervals over time. Examples of time series data include electrocardiograms, brain wave patterns, air temperature, humidity, population sizes, and offshore tidal heights. Other instances include the yearly count of sunspots, currency exchange rates, interest rates, and complex systems like the Lorenz attractor. It is essential to develop models that not only accurately represent the observed data but also generalize well to new data, such as those in a test dataset. Historically, early efforts to predict weather patterns for agriculture sparked interest in time series forecasting algorithms.

Typically, time series data is visualized using a run chart or a temporal line chart. Time series analysis is employed across various fields such as statistics, signal processing, pattern recognition, econometrics, financial mathematics, weather forecasting, earthquake prediction, brainwave monitoring, control engineering, astronomy, and communications engineering.

Time series analysis involves extracting useful statistics and other information from time series data. Time series forecasting, a technique within this field, is used to predict future values based on past observations. Although regression analysis often explores correlations between multiple time series, this approach isn't typically referred to as "time series analysis." Instead, time series analysis focuses on how a series changes over time, especially before and after an event affecting a specific variable.

Time series data is characterized by an inherent temporal ordering. Unlike cross-sectional data, where observations don't have a specific sequence (such as linking income to education level where the data can be arranged in any order), time series data is sequential.

Time series analysis is distinct from spatial data analysis, where observations are often tied to locations (e.g., accounting for house prices based on both location and house characteristics). Time series models often assume that observations made closer together in time are more closely related than those further apart. These models also take advantage of the one-way progression of time, which allows them to use past values to predict future outcomes.

**RNN (Recurrent Neural Networks)**  
Recurrent Neural Networks (RNNs) are deep learning algorithms that identify multiple layers of representation in input data. Developed in the 1980s, RNNs are among the most widely used models in deep learning. These networks have a memory that stores previously seen data, making them powerful tools for sequential data, such as time series, where they can predict future outputs based on past ones. RNNs include repeating loops within their architecture.

A basic RNN consists of an input layer, a recurrent hidden layer, and an output layer. The input layer comprises N units that take in a sequence of vectors over time, denoted as xt1, xt, xt+1, etc., where xt = (x1, x2,…, xN). A weight matrix (WIH) connects the input units to the hidden units in the hidden layer, which are connected across time through recurrent connections. Initializing the hidden units with small non-zero values can enhance the network's performance and stability. The hidden layer represents the system's state or "memory" as:

h_t = f_H(o_t) 

where

 o_t =  x_t +  h_{t-1} + b_h 

In this equation, b_h  is the bias vector for the hidden units, and f_H() is the activation function. The hidden units are connected to the output layer via weighted connections. The output layer, denoted as  y_t = (y_1, y_2,…, y_P) , is calculated as:

y_t = f_o(W_{ho}  h_t + b_o) 

Here,  b_o  is the bias vector for the output layer, and  f_o()  is the activation function. The process described above is repeated across time steps (t = 1, …, T), resulting in a series of nonlinear state equations that together make up the RNN. The hidden states generate predictions for each time step based on the input vector.

An RNN's hidden state captures all essential information about the network's previous states across multiple time steps, independent of external factors. This integrated knowledge enables accurate predictions of the network's future behavior at the output layer. RNNs use a simple nonlinear activation function for each unit. Despite its simplicity, this structure can replicate complex dynamics when trained appropriately over time steps.

**LSTM (Long Short-Term Memory Networks)**  
Long Short-Term Memory networks, or LSTMs, are a type of RNN designed to learn long-term dependencies. Introduced by Hochreiter & Schmidhuber in 1997 and later popularized by other researchers, LSTMs are highly effective for a wide range of problems. They are specifically designed to avoid the issue of long-term dependency, making it easier to retain information over long periods.

Like all RNNs, LSTMs consist of a sequence of repeating neural network modules. However, unlike conventional RNNs, where each module is typically a simple tanh layer, LSTMs have a more complex structure. The repeating module in an LSTM contains four neural network layers that interact in unique ways. These layers include specialized components called memory blocks, which contain multiplicative units known as gates. These gates control the flow of information and contain memory cells with self-connections that store the network's temporal state.

The original LSTM architecture featured input and output gates. The input gate controls the flow of input activations into the memory cell, while the output gate manages how activations exit the cell and interact with the rest of the network. The forget gate, later added to the architecture, allows LSTM models to process continuous input streams without segmentation. It does this by adaptively resetting the memory of the cell, scaling its internal state before feeding it back into the cell through its self-recurrent link. Modern LSTM architectures also include peephole connections from the internal cells to the gates within the same cell to better determine the timing of outputs.

**Project Prerequisites**  
This project requires Python 3.6 to be installed on your computer. The development environment used for this project is Jupyter Notebook, but you may use any environment you prefer. The necessary Python modules for this project are:

- **Numpy (1.22.4)**: Install using `pip install numpy`
- **Scikit-learn (1.1.1)**: Install using `pip install sklearn`
- **Pandas (1.5.0)**: Install using `pip install pandas`

These are all the dependencies required to run the project.
