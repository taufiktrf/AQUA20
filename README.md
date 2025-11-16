# AQUA20 Dataset

The AQUA20 dataset is a comprehensive benchmark dataset designed for **underwater species classification** under challenging real-world conditions. It comprises 8,171 underwater images across 20 distinct marine species, specifically curated to reflect environmental complexities such as turbidity, low illumination, and occlusion, which commonly degrade the performance of standard vision systems. This dataset provides a valuable resource for advancing robust visual recognition in aquatic environments.

The dataset was presented in the paper [AQUA20: A Benchmark Dataset for Underwater Species Classification under Challenging Conditions](https://arxiv.org/abs/2506.17455).

## Sample Usage

You can easily load the AQUA20 dataset using the Hugging Face `datasets` library:

```python
from datasets import load_dataset

# Load the dataset
dataset = load_dataset("AQUA20")

# Access the training split
train_dataset = dataset["train"]
print(f"Number of examples in training set: {len(train_dataset)}")

# Access the test split
test_dataset = dataset["test"]
print(f"Number of examples in test set: {len(test_dataset)}")

# Example of accessing an image and its label
example = train_dataset[0]
image = example["image"]
label = example["label"]
print(f"Example label: {label} (Class Name: {train_dataset.features['label'].names[label]})")

# You can optionally display the image if you have PIL and matplotlib installed
# import matplotlib.pyplot as plt
# plt.imshow(image)
# plt.title(f"Label: {train_dataset.features['label'].names[label]}")
# plt.axis('off')
# plt.show()
```

## Citation

```bibtex
@misc{fuad2025aqua20benchmarkdatasetunderwater,
      title={AQUA20: A Benchmark Dataset for Underwater Species Classification under Challenging Conditions}, 
      author={Taufikur Rahman Fuad and Sabbir Ahmed and Shahriar Ivan},
      year={2025},
      eprint={2506.17455},
      archivePrefix={arXiv},
      primaryClass={cs.CV},
      url={https://arxiv.org/abs/2506.17455}, 
}
```
