## Project title
.

## Tech/framework used
<b>Built with</b>
- [Tensorflow Object Detection API](https://electron.atom.io)

## Installation

- Clone/download this repository

- Install Python: Instructions how to install Python [here](https://www.python.org/downloads/)

- Install Google API: Follow the 'Before you begin' part only: [here](https://cloud.google.com/vision/docs/quickstart-client-libraries).

Once you have the JSON file, move it to the uml folder. Open main.py and edit this line with the name of your json file:
os.environ['GOOGLE_APPLICATION_CREDENTIALS'] = "./[JSON_FILE_NAME]"

- Install Tensorflow Object Detection API: 
On Windows:
Go to this repository on your machine.
Right click on windows_install.ps1 and select 'Run with Powershell'

On Linux:
```
# go into the directory in your terminal
cd uml

# Clone the TensorFlow Model Garden repository
git clone https://github.com/tensorflow/models.git

# Install some required libraries and tools.
apt-get install protobuf-compiler python-lxml python-pil
pip install --upgrade tensorflow google-cloud-vision Cython pandas tf-slim lvis

# Compile the Protobuf libraries.
cd 'uml/models/research/'
protoc object_detection/protos/*.proto --python_out=.
cp object_detection/packages/tf2/setup.py .
python -m pip install --use-feature=2020-resolver .
```

## How to use
Add the handwritten uml diagrams to uml/images.
From the folder uml, run on the terminal:
```
python3 main.py
```

## License
MIT © [Leticia Piucco Marques]()
