# XMTP React Native Quickstart Guide

This guide will help you get started with XMTP in your React Native project.

## Prerequisites
- Node Package Manager (npm)
- Expo
- React Native

## Installation

To install and set up your React Native project, follow the steps below:

1. Initialize a new React Native project:
    ```bash
    npx react-native init xmtp-react-native-quickstart
    ```
2. Install the latest Expo modules:
    ```bash
    npx install-expo-modules@latest
    ```
3. Install Expo:
    ```bash
    npm install expo
    ```
4. Install the XMTP React Native SDK:
    ```bash
    npm i @xmtp/react-native-sdk
    ```

## Platform-Specific Set Up

### Android

For Android, the minimum SDK version must be set to 22, as required by XMTP.

1. Navigate to the `build.gradle` file located in the Android directory.
2. Update the minSDK to `22`.

### iOS 

For iOS, the minimum version must be set to 16.0 as required by XMTP.

#### Update Podfile

1. Navigate to the `Podfile` located in the iOS directory.
2. Modify the following lines:
    
    ```bash
    # line 5
    platform :ios, '16.0'
    
    # line 39 
    pod 'secp256k1.swift', :modular_headers => true
    ```

#### Update Xcode Project 

1. Open `xmtp-react-native-quickstart.xcodeproj` inside IOS folder
2. Change the main deployment target to `16.0`.

#### Run the Application 

To run the application, execute the following commands in your terminal:

```bash
cd ios
pod install
cd ..
npm run ios
```