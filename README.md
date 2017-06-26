## About
This directory contains a practice of OCR using Microsoft Azure Computer Vision based on https://docs.microsoft.com/en-us/azure/cognitive-services/computer-vision/quickstarts/python#optical-character-recognition-ocr-with-computer-vision-api-using-python-a-nameocr-a.

## Setup
1. Subscription key for Microsoft Azure Computer Vision API
2. Python 2.7 - 3.6

## Run
'''`
$ python ocr.py
'''

## Note
The original file has an output as JSON format:
'''
print (json.dumps(parsed, sort_keys=True, indent=2))
'''
To print out words, I made some changes:
'''
for line in parsed['regions'][0]['lines']:
        for word in line['words']:
            print(json.dumps(word['text'], sort_keys=True, indent=2))
'''

## Result

![fonts_sample_ocrb_medium](https://user-images.githubusercontent.com/12990822/27561220-e6b664d8-5a8c-11e7-83dd-c5d0602b24af.png)

![screen shot 2017-06-26 at 4 04 58 pm](https://user-images.githubusercontent.com/12990822/27561201-d3bf1a50-5a8c-11e7-9456-06b0187351fe.png)
