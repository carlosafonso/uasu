# URO: Upload as Read-Only

`uro` is a simple but convenient CLI tool that allows you to upload files to cloud-based object storage platforms and generate a signed URL which can be used to safely share them with others.

`uro` currently supports Google Cloud Storage, with plans to support additional object storage services in the future.

## Installation

```bash
# Clone this repo
git clone https://github.com/carlosafonso/uro
cd uro

# Create a Python virtual env
python3 -m venv .venv

# Install deps
pip install -r requirements.txt
```

## Usage

You must have a Google Cloud service account with the `Storage Object Viewer` role, and a JSON key file present in your local environment.

Then you can invoke `uro` as follows:

```bash
./uro.py -b <GCS_BUCKET_NAME> -k <PATH_TO_JSON_KEY_FILE> <PATH_TO_FILE_TO_UPLOAD>
```
