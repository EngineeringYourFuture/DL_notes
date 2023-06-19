# Deep Learning Note
## Linear Regression
### Loss function
$$
𝓁(\mathbf{X},\mathbf{y},\mathbf{w}, b)=\frac{1}{2n}\mathbf{\sum}_{i=1}^{n} (y_i-\langle \mathbf{x}_i, \mathbf{w} \rangle-b)=\frac{1}{2n} ||\mathbf{y} - \mathbf{X}\mathbf{w} - b||^2
$$
### Optimization equation
$$
\mathbf{w}^{\ast},\mathbf{b}^{\ast}= \underset{\mathbf{w}, b}{\mathrm{argmin}} \ 𝓁(\mathbf{X},\mathbf{y},\mathbf{w},b)
$$
### Add bias to weights
$$
\mathbf{X} \rightarrow [\mathbf{X}, \mathbf{1}] &emsp; \mathbf{w}\rightarrow \begin{bmatrix}
\mathbf{w}\\
b \\
\end{bmatrix}
$$
$$
𝓁(\mathbf{X},\mathbf{y},\mathbf{w})=\frac{1}{2n} ||\mathbf{y} - \mathbf{X}\mathbf{w} ||^2 &emsp;
 \frac{\partial}{\partial\mathbf{w}}𝓁(\mathbf{X},\mathbf{y},\mathbf{w})=\frac{1}{n}(\mathbf{y} - \mathbf{X}\mathbf{w})^{T}\mathbf{X}
$$
#### The loss function of linear regression is convex, therefore the optimal weights are:
$$
\begin{gather*}
\frac{\partial}{\partial\mathbf{w}}𝓁(\mathbf{X},\mathbf{y},\mathbf{w})=0 \\ 
\frac{1}{n}(\mathbf{y} - \mathbf{X}\mathbf{w})^{T}\mathbf{X}=0 \\ 
\mathbf{w}^{\ast}=(\mathbf{X}\mathbf{X}^{T})^{-1}\mathbf{X}\mathbf{y}
\end{gather*}
$$
### Optimizatin method
#### Gradient Descent
#### Choose all the dataset to calculate the gradient
$$
\mathbf{w_{t}} =\mathbf{w_{t-1}}-\eta\frac{\partial𝓁} {\partial \mathbf{w_{t-1}}}
$$
#### Stochastic Gradient Descent
##### Choose a batch of the entire dataset randomly
$$
\mathbf{w_{t}} =\mathbf{w_{t-1}}-\eta\frac{\partial𝓁_{b}} {\partial \mathbf{w_{t-1}}}
$$

