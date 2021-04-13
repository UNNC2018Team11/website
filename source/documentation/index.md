---
layout: post
title: Documentation
abbrlink: c0abe2ce
---

# Eye Tracking for Simulation Assessment

Eye tracking is the process of measuring either the point of gaze
(where the user is looking) or the motion of an eye relative to the
head (Daniel,2004). In this project, users will watch simulations on
the software. Combined with the functions of eye recognition and
fixation point positioning, the researcher analyzes the user's eye
movement trajectory and derives relevant information to obtain the
different concerns of users for different simulations.

Team's Blog: https://18757670961.github.io/

---

## Prerequisite

### Note:

* **If you find the number of points in the heatmap is quite small, it mignt be the result of bad light condition. Please change a place where your face coud be clearly identified, because eye tracking accuracy is largely affected by light condition.**
* **When you are using this application, please make sure ONLY your whole face is in front of the camera.**

### Hardware
- The recommended computer configurations: 
  - CPU: Intel i7/ AMD Ryzen7 4800H or above
  - GPU: NVIDIA 2060 or above
  - Hard disk: 512GB or above
  - RAM: 8G or above 
  - Webcam: 720P or above


 **You may have problem in 'npm install' if you cannot reach these configurations. Please contact us if you cannot run successfully.**
### Software

* This App is proven to run successfully under **Windows 10** environment. However, other operating systems such as Linux, macOS haven't been proven to support this App. Please contact us before running this App if you are a user of those operating.

- Node.js 12.x and above (https://nodejs.org/en/)
- Java SE8 and above
- Python 3.8 and above

---

## Frontend

### Project Structure

```
src
|
├─App.vue
│  background.js    // main process (entrance)
│  main.js          // renderer process (Vue initialization)
│
├─assets
│      clmtrackr.js
│      logo.png
│      rally.js     // theme configuration
│      tailwind.css
│
├─components
│      Card.vue
│      Drawer.vue
│      FloatButton.vue
│      GaugeChart.vue
│      Heatmap.vue
│      LoginForm.vue
│      Logout.vue
│      Navbar.vue
│      RegisterForm.vue
│      TopBar.vue
│
├─plugins
│      vuetify.js   // UI framework configuration
│
├─router
│      index.js
│
├─store
│  │  index.js
│  │
│  └─modules
│          Counter.js
│          index.js
│
├─utils
│      commonUtil.js
│      indexedDB.js     // local storage
│      storeUtil.js
│      upload.js        // record uploading API
│
└─views
        About.vue
        EyeTracking.vue
        Guide.vue
        Home.vue
        Records.vue
        Simulation.vue
        Visualization.vue
```

### NPM Source Setup

```
npm config set registry https://registry.npm.taobao.org/

npm config set ELECTRON_MIRROR http://npm.taobao.org/mirrors/electron/

npm config set SASS_BINARY_SITE='https://npm.taobao.org/mirrors/node-sass'
```

### Project Setup

```
npm cache clean -f

npm install
```

### Compiles and Hot-reloads for development

```
npm run electron:serve
```

### Compiles and Minifies for production

```
npm run electron:build
```

### Lints and Fixes Files

```
npm run lint
```

### Customize Configuration

See [Configuration Reference](https://cli.vuejs.org/config/).

---

## Backend

### Project Structure

```
|-- simulation
    |-- example.py   // the main function
    |-- gaze_tracking
        |-- calibration.py
        |-- eye.py   // detect eyes
        |-- gaze_tracking.py   
        |-- pupil.py   // detect pupil
        |-- trained_models   // a trained model provided by dlib
            |-- shape_predictor_68_face_landmarks.dat

```

### Install Python Dependencies (NumPy, OpenCV, Dlib):

```
pip install -r python_requirements.txt
```

**We use cv2.VideoCapture(0) to call the laptop camera in this version.**

If you want to call **external camera**, please change **simulation/example.py (line 11)** into 
```
webcam = cv2.VideoCapture(1)
```

---

## Test

### Unit Test
```
src/simulation/test_exm.py
```
If you want to run the unit tests, please run the following command first
```
pip install pytest
```
### Component Test by Junit
```
src/simulation/PythonLauncherTest.java
src/simulation/SimulationLauncherTest.java
```
**Please DO NOT run these 2 testing files directly.**

If you want to run these tests, please open the files given above in the Intellij IDEA or Eclipse with Junit imported.

To import Junit package, you can use the 'junit-4.9.jar' provided in the 'simulation' folder, or you can let the IDE automatically import **Junit4** for you (please refer to the instructions of the IDE you are using)

---

## Others
If you want to maintain our code, please refer to [Maintenance Manual](./doc/Team11_maintenance_manual.pdf)

```
doc/Team11_maintenance_manual.pdf
```