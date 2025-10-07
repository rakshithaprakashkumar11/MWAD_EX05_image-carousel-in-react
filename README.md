# MWAD_EX05_image-carousel-in-react
## Date:7-10-2025

## AIM
To create a Image Carousel using React 

## ALGORITHM
### STEP 1 Initial Setup:
Input: A list of images to display in the carousel.

Output: A component displaying the images with navigation controls (e.g., next/previous buttons).

### Step 2 State Management:
Use a state variable (currentIndex) to track the index of the current image displayed.

The carousel starts with the first image, so initialize currentIndex to 0.

### Step 3 Navigation Controls:
Next Image: When the "Next" button is clicked, increment currentIndex.

If currentIndex is at the end of the image list (last image), loop back to the first image using modulo:
currentIndex = (currentIndex + 1) % images.length;

Previous Image: When the "Previous" button is clicked, decrement currentIndex.

If currentIndex is at the beginning (first image), loop back to the last image:
currentIndex = (currentIndex - 1 + images.length) % images.length;

### Step 4 Displaying the Image:
The currentIndex determines which image is displayed.

Using the currentIndex, display the corresponding image from the images list.

### Step 5 Auto-Rotation:
Set an interval to automatically change the image after a set amount of time (e.g., 3 seconds).

Use setInterval to call the nextImage() function at regular intervals.

Clean up the interval when the component unmounts using clearInterval to prevent memory leaks.

## PROGRAM
### App.jsx:
```
import React from 'react';
import FoodDisplay from './components/FoodDisplay';

function App() {
  return (
    <div className="min-h-screen bg-gradient-to-b from-orange-50 to-orange-100 flex items-center justify-center py-12">
      <FoodDisplay />
    </div>
  );
}

export default App;
```

### App.css:
```
@tailwind base;
@tailwind components;
@tailwind utilities;

```
## OUTPUT
![Screenshot 2025-05-17 194536](https://github.com/user-attachments/assets/0c1c7ed8-f436-47c3-8cd5-b2e2882fc81a)
![Screenshot 2025-05-17 194516](https://github.com/user-attachments/assets/411570d3-aeb4-49ab-bdd7-399233b516da)
![Screenshot 2025-05-17 194525](https://github.com/user-attachments/assets/65ac8942-b6e0-4155-acda-1745010210a0)

## RESULT
The program for creating Image Carousel using React is executed successfully.
