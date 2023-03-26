---
layout: post
title: How to set up Flutter for VS Code
description: Bring to the table win-win survival strategies to ensure proactive domination. At the end of the day, going forward, a new normal that. Capitalize on low hanging fruit to identify a ballpark value activity to beta test. Override the digital divide with additional.
date: 2022-12-09 15:01:35 +0530
image: '/images/how-to-setup-flutter-for-vs-code.jpg'
image_caption: 'Photo by [Stephen SIMON](https://twitter.com/codewithsimon)'
tags: [flutter,vsCode]
---

Flutter is a popular open-source mobile application development framework. It allows developers to build high-performance mobile applications for both Android and iOS platforms. Setting up Flutter in Visual Studio Code is a straightforward process. In this article, we’ll guide you through the installation and setup process.

Before we begin, make sure you have installed Visual Studio Code on your machine. You can download it from the official website: **[https://code.visualstudio.com/](https://code.visualstudio.com/)**.

1. Install Flutter SDK
The first step is to download and install the Flutter SDK. You can download it from the official Flutter website: **[https://flutter.dev/docs/get-started/install](https://flutter.dev/docs/get-started/install)**. Follow the instructions based on your operating system.
2. Set up Environment Variables
After installing the Flutter SDK, you need to set up environment variables on your machine. This step is crucial as it helps to access the Flutter SDK from anywhere in the system.

##### For Windows users:

- Open the Start Menu and search for "Environment Variables."
- Click on "Edit the system environment variables."
- Click on the "Environment Variables" button.
- Under "System Variables," click on "New."
- Enter the following details:
    - Variable name: FLUTTER_HOME
    - Variable value: [your_flutter_sdk_path]
- Click on "OK" to save the changes.

##### For Mac and Linux users:

- Open your terminal.
- Enter the following command:
    
    export PATH=$PATH:[your_flutter_sdk_path]/flutter/bin
    

Note: Replace "[your_flutter_sdk_path]" with the path where you have installed the Flutter SDK.

1. Install Flutter and Dart Extensions in Visual Studio Code
Open Visual Studio Code and click on the "Extensions" icon in the left panel. Search for "Flutter" and "Dart" extensions and install them.
2. Create a New Flutter Project
To create a new Flutter project, follow these steps:
- Open Visual Studio Code and click on "View" > "Command Palette".
- Search for "Flutter: New Project" and click on it.
- Enter the project name and location where you want to save it.
- Wait for a few minutes while Visual Studio Code sets up the project.
1. Run the Flutter Application
To run the Flutter application, follow these steps:
- Open the project folder in Visual Studio Code.
- Open the "lib/main.dart" file.
- Click on the "Run" button in the top menu bar.
- Select the device where you want to run the application.
- Wait for a few minutes while the application builds and runs.

Congratulations 👏 You have successfully set up Flutter in Visual Studio Code and created your first Flutter application. You can now start building your own high-performance mobile applications using Flutter.