# Image Processing Script

This script processes images from a specified folder, uploads them to Google Drive, and stores image information in a PostgreSQL database. The goal is to automate the handling of image data, specifically for grains with identified defects.

## Features

* Parses images from a folder and renames them based on the defect type.
* Extracts EXIF data, including timestamps, from images.
* Uploads processed images to a specified Google Drive folder using the Google Drive API.
* Stores image metadata in a PostgreSQL database, including file name, timestamp, EXIF data, and defect information.

## Requirements

* Python 3.x
* argparse, psycopg, googleapiclient, google-auth, PIL (Pillow)

## Setup

* Install the required dependencies using pip:
```
pip install argparse psycopg2-binary google-auth google-api-python-client pillow
```
* Set up your PostgreSQL database with the correct credentials (dbname, user, etc.).
* Obtain a Google Drive API service account and download the keys.json file.
* Replace SERVICE_ACCOUNT_FILE and PARENT_FOLDER_ID in the script with your information.

Usage

Run the script using the following command:
```
python script_name.py <folder_path> --defect <defect_type>
```
* <folder_path>: Path to the folder containing images.
* --defect: (Optional) Specify the defect type of the grains in the images.