### Getting started
- npx react-native init xmtp-react-native-quickstart
- npx install-expo-modules@latest
- npm install expo
- npm i @xmtp/react-native-sdk

Then navigate to the `build.gradle` file inside the android director and update the minSDK to 22 which is required for XMTP
Then navigate to the `Podfile` in the ios directory and update the min version to 16 which is required for for XMTP
add 


### Build props (doesnt work)
npm i expo-build-properties
https://docs.expo.dev/versions/latest/sdk/build-properties/

```
"expo": {
    "plugins": [
      [
        "expo-build-properties",
        {
          "android": {
            "compileSdkVersion": 31,
            "targetSdkVersion": 31,
            "buildToolsVersion": "31.0.0"
          },
          "ios": {
            "deploymentTarget": "13.0"
          }
        }
      ]
    ]
  }
```

### Pod file
line 5

platform :ios, '16.0'

line 39
pod 'secp256k1.swift', :modular_headers => true