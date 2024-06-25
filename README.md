# ML Project: Image Classification with CNN

This project aims to build a Convolutional Neural Network (CNN) from scratch for image classification on the CIFAR-10 dataset.

## Dataset

The CIFAR-10 dataset consists of 60,000 32x32 color images in 10 classes, with 6,000 images per class. The dataset is divided into 50,000 training images and 10,000 test images.

## Model Architecture

The CNN architecture consists of the following layers:

1. Convolutional Layer (32 filters, 3x3 kernel)
2. Max Pooling Layer (2x2 pool size)
3. Convolutional Layer (64 filters, 3x3 kernel)
4. Max Pooling Layer (2x2 pool size)
5. Fully Connected Layer (128 units)
6. Output Layer (10 units, softmax activation)

## Usage

1. Clone the repository: `git clone https://github.com/your-username/ml-project.git`
2. Navigate to the project directory: `cd ml-project`
3. Install the required dependencies: `pip install -r requirements.txt`
4. Run the model training script: `python notebooks/model.py`

## Results

The trained model achieved an accuracy of X% on the test set.

## Future Improvements

- Experiment with different CNN architectures and hyperparameters
- Implement data augmentation techniques
- Deploy the model as a web application or API

## Contributing

Contributions are welcome! Please open an issue or submit a pull request.







import pandas as pd

# Original data dictionary
res = {'A': {'neg': 0.1, 'neu': 0.8, 'pos': 0.1},
       'B': {'neg': 0.2, 'neu': 0.6, 'pos': 0.2}}

# Create DataFrame and transpose it
vaders = pd.DataFrame(res).T
print(vaders)

vaders = vaders.reset_index().rename(columns={'index': 'Id'})
print(vaders)

# Another DataFrame for merging
df = pd.DataFrame({'Id': ['A', 'B'], 'info': ['info1', 'info2']})

# Merge on 'Id'
vaders = vaders.merge(df, how='left')
print(vaders)

After merging, the resulting DataFrame has clear and meaningful column names:
  Id  neg  neu  pos  info
0  A  0.1  0.8  0.1  info1
1  B  0.2  0.6  0.2  info2









