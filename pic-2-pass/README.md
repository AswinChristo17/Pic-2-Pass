Hand Detection and Screenshot Capture!

This project demonstrates a Python application that uses computer vision to detect hands, capture screenshots, and process face images for passport-size photo creation. The project relies on libraries like OpenCV, CVZone, PyAutoGUI, and Matplotlib.

Features

Hand Detection: Uses the CVZone HandTrackingModule to detect hands from the webcam.

Screenshot Capture: Takes a screenshot whenever all five fingers are raised and displays the screenshot using Matplotlib.

Face Detection and Passport Photo Generation: Processes face images to fit passport-size dimensions with customizable DPI.

Auto Exit: Exits the program if no hand is detected for a specified time period.

Key Variables

Hand Detection and Screenshot Capture

detectionCon: Confidence level for hand detection (default: 0.7).

maxHands: Maximum number of hands to detect (default: 1).

last_hand_detection_time: Tracks the time since the last hand was detected.

Passport Photo Dimensions

passport_width_inches: Width of the passport photo in inches (default: 3.5 inches).

passport_height_inches: Height of the passport photo in inches (default: 4.8 inches).

dpi: Dots per inch for passport photo resolution (default: 300 DPI).

Functionality

Hand Detection:

Detects the hand and checks if all fingers are raised.

Captures a screenshot and saves it as opencv_frame_<number>.png.

Displays the screenshot using Matplotlib.

Face Detection and Cropping:

Adds a border around the detected face.

Crops and resizes the face to fit passport photo dimensions.

Auto Exit:

Prints a message and exits if no hand is detected for more than 6 seconds.

Code Details

Screenshot Capture

Takes a screenshot when all fingers are raised.

Displays the captured screenshot using Matplotlib.

Passport Photo Processing

Calculates the required pixel dimensions based on the desired inches and DPI.

Expands the detected face region, resizes it, and fits it into passport dimensions.

Key Bindings

Press q to quit the program manually.

Example Output

Hand Detection and Screenshot Capture

When a hand is detected with all fingers raised:

Screenshot taken

A screenshot image will be saved and displayed.

Face Detection and Passport Photo Generation

After processing the face:

Displays the resized passport photo.

Customization

You can adjust the following parameters in the code:

Hand detection confidence: Modify the detectionCon value for stricter or more lenient hand detection.

Auto-exit time: Change the time limit in the elapsed_time check to adjust the auto-exit duration.

Passport dimensions: Update passport_width_inches, passport_height_inches, or dpi to change the passport photo size or resolution.

Future Enhancements

Add more gestures for triggering other events.

Integrate face detection directly with a pre-trained model for improved accuracy.

Add support for saving multiple images in different formats (e.g., JPEG, BMP)
