# Automatic-License-Plate-Recognition-ANPR-
This project aims to detect license plates from car images and transform the detected image into texts.

## Scope
1. to detect Thai plate license
2. to read Thai alphabet and number on different background color (white, red, and yellow)
3. to collect timestamp of car coming in and out

## Application
The license plate detection can be used in places where the record of registration number and the vehicle's province of registration are needed. It can be placed not only just in parking lots in shopping malls, office buildings, or airports but also in no parking area to efficiently detect cars that violate regulations.

## Process
### Step 1: Collect data
- Collect 10 pictures of cars with license plates
- License plates are vary in background color, background pattern, letters, and province of registration 

### Step 2: License Plate Detection
- Use pre-train model to detect the license plate in the picture
- Crop the license plates from the picture by using OpenCV

### Step 3:Image Pre-Processing
- Cropped image
- Convert to greyscale image
- Resize the picture to the correct ratio
- Crop and seperate the pictures into 2 parts: registration number and the vehicle's province of registration
- Apply biliteral filter (a non-linear, edge-preserving, and noise-reducing smoothing filter for images)
- Convert to binary image (black and white)

### Step 4: Optical Character Recognition
- Use OCR to transform the letters in the image into text
- Compare 2 text recognition engine: Tesseract and Cloud Vision API

### Step 5: Test Prepocessing
- remove all the irrelavent letter and vowels
- map the extracted text to province name  

### Step 6: Record Timestamp
- Collect time (in and out), license number and province and put them in dataframe

## Ref
https://ksingh7.medium.com/part-i-using-a-pre-trained-keras-model-for-license-plate-detection-7687739af758
