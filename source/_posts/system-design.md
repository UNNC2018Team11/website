---
title: System Design
catalog: true
mathjax: true
tags: Coding
abbrlink: a6362ef3
date: 2021-04-13 23:01:22
---

## Eye Tracking

### The language to realize eye-tracking - Python

There areplenty of benefits regardingusingPythonfor the eye-tracking part. Firstly, Python is easy to understand. Although not all of the team members have learned Python, the team stilldecides to useit since it is really quick to get hang of it andit isvery suitable for human reading. The codes written in Python are simple and allowdevelopersto focus on problem-solving instead of understanding the language itself. The pseudo-code-likenature of Python largely increases the efficiency of communication and codingbetween the team members. Also, Python has one of the richest and most powerful class librariesamongthe scripting languages, which covers most of the application scenarios such as fileI/O, GUI,network programming, database access andtext manipulation.Providedthese usefulresources, itbecomes practicalto fully implementan eye-tracking systemmerely throughthis language.The arguments given aboveare the main reasons why the teamhaschosenPython.

### The application to perform Python - OpenCV

Thisprojectis supposedto build an eye-tracking system, sorecognizinghuman faces and eyesbecomes a crucial issue. OpenCV(Open Source Computer Vision Library) is suitablefor this purposebecause it contains more than 500 functionsthat could be utilized toimplement general algorithms for graphics processing and computer vision. Italsohas a Python interface and supports Windows, Linux, Android, and Mac OS.Thanks to these advantages, the team can executethe codesondifferentoperatingsystems. With the toolsprovided,group members can easilyaccessthe datarelated tothe shape of human eyes,and even extracttheoutline of users'pupil from the whole eyefigure.Therefore,this library would contribute a lottothisproject.

## Simulation software - AnyLogic

AnyLogic is completely Java-based so that it can take advantage of the rich Java sources, can achieve a variety of Java functions and effects. Becausethe teamhaslearned knowledge of Java and Object-Oriented, understanding how to use this software is not difficult, though it is a little different from Java. Additionally, the visual development environment supports module drag-and-drop operations, which increase flexibility. Apart from that, due to AnyLogic professional version, models can be exported as standalone Java programs. Therefore, the models can be started by running the JAR files.

## Front End Architecture

### Frontend

For the front end part of this application, Electron is extensively used as a basic container that holds all  HTML, CSS, and Javascript codes inside a Chromium core. Thanks to Electron, developers could utilize modern web technologies for an easier interface design and easier native application development, instead of learning some old-fashioned GUI toolkit or sophisticated APIs of operating systems(Natalia, 2018). Inside this Electron environment, Vue (a Javascript framework) is used to implement the key business logic of the frontend including page navigation and information display. In addition, an open-source library, Echarts, is embedded in the Vue component to visualize the eye-tracking data in a heatmap, and IndexedDB (a transactional database inside Chromium) functions as local storage which synchronizes users' eye-tracking data between the application and LeanCloud (a Backend-as-a-Service platform with database and file storage functionalities). In general, this application follows the typical design pattern of MVVM (Model-View-ViewModel) and SPA (Single Page Application).

Natalia, T. (2018) 'Building a Desktop App with Vue: Electron',*DEV Community*, 11 September. Available at:[https://dev.to/n_tepluhina/building-a-desktop-app-with-vue-electron-3pl](https://dev.to/n_tepluhina/building-a-desktop-app-with-vue-electron-3pl?fileGuid=VTKRTvXXVRgtcvDy)(Accessed: 26 March 2021).

### Electron

JavaScript used to be known as the language for building websites and web applications especially with some of its frameworks such as React, Vue, and Angular but over time, it became possible for JavaScript to run outside the browser with the emergence of[Node.js](https://en.wikipedia.org/wiki/Node.js?fileGuid=VTKRTvXXVRgtcvDy), an open-source, cross-platform, JavaScript runtime environment that executes JavaScript code outside a web browser. This has led to the ability to use JavaScript for a whole lot more than just web applications, and one of which is building desktop applications using Electron.js.

![图片](https://uploader.shimo.im/f/1UjuzKWHVWeodgFo.png!thumbnail?fileGuid=VTKRTvXXVRgtcvDy)

Electron enables developers to create desktop applications with pure JavaScript by providing a runtime with rich native (operating system) APIs. It can be seen as a variant of the Node.js runtime that is focused on desktop applications instead of web servers. Usually, an Electron-based application is comprised of two distinct processes: the main process and the renderer process(Timi, 2020).

Timi, O. (2020) 'Building Desktop Apps With Electron And Vue',*Smashing Magazine*, 21 July. Available at:[https://www.smashingmagazine.com/2020/07/desktop-apps-electron-vue-javascript/](https://www.smashingmagazine.com/2020/07/desktop-apps-electron-vue-javascript/?fileGuid=VTKRTvXXVRgtcvDy)(Accessed: 26 March 2021).

![图片](https://uploader.shimo.im/f/Cf5Fj1u4bfVMDORl.jpeg!thumbnail?fileGuid=VTKRTvXXVRgtcvDy)

The main process is where the application will handle various system-level activities, like life-cycle events (starting up, preparing to quit, actually quitting, switching between the foreground and background). Particularly, in this project, the main process is what is used to bootstrap the application.

The main process also has another responsibility, which is to spawn any render processes. It is these processes that would display the UI of the application. Each of these renderer processes will load the content and execute it within its own thread. In addition, Electron also includes an interprocess communication (IPC) system to allow events and data to be passed back and forth between the main and any renderer process(Chris and Leif, 2017).

Chris, G. and Leif, W. (2017)*Electron: From Beginner to Pro: Learn to Build Cross Platform Desktop Applications using Github's Electron.*Available at:[https://www.apress.com/cn/book/9781484228258](https://www.apress.com/cn/book/9781484228258?fileGuid=VTKRTvXXVRgtcvDy)(Download: 27 March 2021).

Nonetheless, some disadvantages exist regarding the usage of Electron. Powered by this framework, the deployed app is comparatively larger than normal native applications because it bundles inside itself a complete copy of the powerful Chrome browser(Andy, 2018). It might be around 70M which could expand to 200M on a disk when installed. Also, due to the memory usage of Chromium and the single-thread feature of Node.js, performance remains a serious issue for Electron-based applications, especially for CPU-bound applications. However, what to be noted is that the users of the Electron app do not need Chrome to be installed on machines — Electron's Chromium is self-contained and secretly hide inside the deployed app.

Andy, B. (2018) 'Building a deployable Python-Electron App',*Medium*, 3 October. Available at:[https://medium.com/@abulka/electron-python-4e8c807bfa5e](https://medium.com/@abulka/electron-python-4e8c807bfa5e?fileGuid=VTKRTvXXVRgtcvDy)(Accessed: 26 March 2021).

### Vuetify

Vuetify is a complete UI framework built on top of Vue.js. Unlike other frameworks, Vuetify is designed from the ground up to be easy to learn and rewarding to master with hundreds of carefully crafted components from the[Material Design specification](https://material.io/?fileGuid=VTKRTvXXVRgtcvDy), which is a mature UI/UX design guideline in the frontend area. To ease the extra burden of interface design, Vuetify is applied to this application to make it more user-friendly and accessible.

### IndexedDB

IndexedDB is a low-level API for client-side storage of significant amounts of structured data inside a browser. While Web Storage is useful for storing smaller amounts of data, it is less useful for storing larger amounts of structured data. IndexedDB provides an efficient solution for the application to persistently store the eye-tracking data at a small cost.

![图片](https://uploader.shimo.im/f/IEp7Iy0Psm4d1cdG.png!thumbnail?fileGuid=VTKRTvXXVRgtcvDy)

### IPC

Inter-process communication (IPC) specifically refers to the mechanisms an operating system provides to allow different, local and remote processes to communicate with each other(Ahmed, 2020). Typically, applications that use IPC can be categorized into clients (frontend) or servers (simulation and eye-tracking systems), where the client requests data and the server responds to the client's requests. In the project, the Node.js modules in Electron would spawn the process of simulations in Java and display the eye-tracking data via reading the CSV file generated by Python codes. Afterwards, users could decide whether to upload local watching records to LeanCloud storage through HTTP requests.

Ahmed, B. (2020) 'Connecting Python 3 and Electron/Node.JS: Building Modern Desktop Apps',*Code Project*, 28 April. Available at:[https://www.codeproject.com/Articles/5266469/Connecting-Python-3-and-Electron-Node-JS-Building](https://www.codeproject.com/Articles/5266469/Connecting-Python-3-and-Electron-Node-JS-Building?fileGuid=VTKRTvXXVRgtcvDy)(Accessed: 26 March 2021).

## Code Hierarchy

### Eye Tracking

When users choose to start playing the simulation, the eye-tracking program would begin to run. The responsibility of the eye-tracking system is to track users' eye movements and speculate the gazing point. The following content will give a brief description of steps of how to detect pupils and find the gazing point.

**Step 1: Using a function get_frontal_face_detector from dlib to detect face.**

Dlib is a modern C++ toolbox that contains machine learning algorithms and tools for creating complex software in C++ to solve practical problems, such as tracking eyes. Dlib's open source license allows everyone to use it for free, and many sample programs are provided so that the team can learn how these new functions work, and how do they affect the results. These are very useful for building the project. Besides, it provides better face detection and feature point positioning algorithm than OpenCV, which is a good supplement.

**Step 2: Using a trained model from dlib to locate 68 facial landmarks.**

"shape_predictor_68_face_landmarks.dat" is a trained model provided by dlib toolbox. It could help to detect human face accurately, and also find the location of eyes.

**Step 3: Using a threshold to binarize the frame based on a threshold value.**

The idea of thresholding is to further-simplify visual data for analysis. Every pixel above the threshold value would be converted to 255 (white), on the other hand, those under would be converted to 0 (black). Thus, this function helps the team to find the best suitable binary frame by changing the threshold value.

**Step 4: Choosing the landmarks around the eyes and capture a frame that only containing an eye.**


![图片](https://uploader.shimo.im/f/3nPcQbnkxTRgfJJ2.png!thumbnail?fileGuid=VTKRTvXXVRgtcvDy)


**Step 5: Finding contours to detect the position of the iris, and then get the coordinates of the centre of the iris.**

![图片](https://uploader.shimo.im/f/6NYWprMhlH0pSEtF.png!thumbnail?fileGuid=VTKRTvXXVRgtcvDy)

![图片](https://uploader.shimo.im/f/wDgvXWBlR2LNIumR.png!thumbnail?fileGuid=VTKRTvXXVRgtcvDy)

**Step 6: Calculating the gazing point.**

The team uses a mathematic method that uses the distance between camera and user, camera height, and other information as parameters. The x and y coordinates of all the gazing points would be stored in the "coor.csv" file.

**Step 7: Calculating the automatically generated score**

The program would read the x and y coordinates from the "coor.csv" file and calculate standard deviation, maximum value, and other values. The automatically generated score will be calculated according to these values. Besides, the mark will be stored in the "mark.csv" file.

**Step 8: Generate the gazing point distribution map**

The whole map is divided into 24x10 grids. Initially, the locating number of all the grids is zero, and these numbers are stored in a 2-dimension array. When a point is located in a specific grid, the value is stored in the corresponding position in the array. In other words, the larger the value is, the more frequent user watching in this area. The array will be stored in the "count.csv" file.


## Integration

In this project, there are three different parts which are the frontend part, simulation part and eye-tracking part respectively. In order to run these three parts simultaneously, multithreading and multiprocessing are required for the project. Once the application starts, the frontend part need one process to run. When users click the "start" button of one simulation, the Java class file "Main.class" will be executed immediately by the batch script file and then one main process will run. The main process then will start one thread called "SimulationLauncher". This thread will start the batch file process and another thread called "PythonLauncher" simultaneously. At the same time, the batch file process starts another child process running simulation and the "PythonLauncher" thread starts the eye-tracking process. Consequently, all three parts are running collectively. In addition, the developer has limited time that simulations can play, which means that the simulation process will be terminated automatically and the batch file process will quit at the end, too. After that, the eye-tracking process will also be terminated. Finally, three processes would quit successfully. Following these three child processes, "SimulationLauncher" and "PythonLauncher" will also quit afterwards, and finally, the main process will exit. Therefore, after one simulation ends playing, the program is supposed to have merely one process (frontend part) running. In general, if users are not watching simulations, only one process would exist; otherwise, the program contains several threads and processes simultaneously.


![图片](https://uploader.shimo.im/f/uWg1bPvrJygnQpqm.jpg!thumbnail?fileGuid=VTKRTvXXVRgtcvDy)


