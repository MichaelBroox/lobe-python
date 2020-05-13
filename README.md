# lobe-python

## Install
Clone this repo, then go to the repo root directory and call:
```python setup.py install```

## Usage
```
from lobe import ImageModel

model = ImageModel.load('path/to/exported/model')

# Predict from an image file
result = model.predict_from_file('path/to/file.jpg')

# Predict from an image url
result = model.predict_from_url('http://path/to/file.jpg')

# Predict from Pillow image
from PIL import Image
img = Image.open('path/to/file.jpg')
result = model.predict(img)

# Print top prediction
print(result.prediction)

# Print all classes
for label, prop in result.labels:
    print(f"{label}: {prop*100}%")

```