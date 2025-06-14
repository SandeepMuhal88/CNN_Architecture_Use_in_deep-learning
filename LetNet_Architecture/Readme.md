# LeNet-5: Classic CNN Architecture for Image Classification

![LeNet-5 Architecture](assets/lenet_arch.png)  
*Yann LeCun's original LeNet-5 architecture (1998)*

LeNet-5 is a pioneering convolutional neural network (CNN) designed for handwritten digit recognition (MNIST). It introduced key CNN concepts still used today.

## **Key Features**
✔ **First Successful CNN** – Proven effective for digit recognition  
✔ **Simple Architecture** – Only 5 layers (2 conv, 2 subsampling, 1 fully connected)  
✔ **Lightweight** – ~60k parameters (tiny compared to modern networks)  

## **Architecture**
| Layer Type       | Parameters              | Output Size (Input: 32x32x1) |
|------------------|------------------------|-----------------------------|
| Conv2D + Tanh    | 5x5, 6 filters         | 28x28x6                     |
| AvgPooling2D     | 2x2, stride=2          | 14x14x6                     |
| Conv2D + Tanh    | 5x5, 16 filters        | 10x10x16                    |
| AvgPooling2D     | 2x2, stride=2          | 5x5x16                      |
| Flatten          | -                      | 400                         |
| Dense + Tanh     | 120 units              | 120                         |
| Dense + Tanh     | 84 units               | 84                          |
| Output (Softmax) | 10 units (MNIST)       | 10                          |

## **Installation**
```bash
git clone https://github.com/yourusername/lenet-5.git
cd lenet-5
pip install -r requirements.txt