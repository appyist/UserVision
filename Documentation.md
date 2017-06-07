# UserVision

#### Getting Started

1. To get up and running, download UserVision from https://github.com/appyist/UserVision.git

2. Drag UserVision.framework into your Xcode project.

3. Add **UVAuthEmail** and **UVAuthSecret** key value pairs to your project's info.plist file.

   ![Screen Shot 2017-06-01 at 15.28.27](/Users/emirhanerdogan/Desktop/Screen Shot 2017-06-01 at 15.28.27.png)

> These fields will be provided by UserVision.



#### Usage

1. Import UserVision in your Appdelegate.swift

```swift
import UserVision
```

2. Initialize UserVision in your didFinishLaunchingWithOptions

Parameters:

- ptr -> UIWindow

- type -> RecordType (Optional parameter, default value is screenAudio)

  **screen:** Records only screen without audio.

  **screenAudio:** Records screen and audio at the same time.

```swift
func application(_ application: UIApplication, didFinishLaunchingWithOptions launchOptions: [UIApplicationLaunchOptionsKey: Any]?) -> Bool {
        UserVision.with(&window, type: RecordType.screenAudio)
        return true
    }
```

3. To start recording, use startRecording().

```swift
UserVision.shared.startRecording()
```

4. To stop recording, use stopRecording().

```swift
UserVision.shared.stopRecording()
```