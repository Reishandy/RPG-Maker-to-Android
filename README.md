# RPG Maker to Android APK Guide

A comprehensive guide and Android Studio template for converting RPG Maker MV and MZ games into Android APKs.


## 🛠️ Prerequisites
Before starting, ensure you have the following:
- A computer with **Windows, macOS, or Linux**.
- **Android Studio** installed.
- An RPG Maker **MV or MZ** game ready for deployment.

## 📌 Installation & Setup

### 1️⃣ Install and Set Up Android Studio
---
1. Download the latest version of Android Studio from [here](https://developer.android.com/studio).
   
   ![Download Android Studio](img/1.png)
   
3. Install it and follow the setup wizard (default settings are recommended).

### 2️⃣ Download and Extract the Template
---
1. Get the template from the **latest release** or [download it here](https://github.com/Reishandy/RPG-Maker-to-Android/releases/download/project-fles/RPG-Maker-to-Android-project.zip).
2. Extract the downloaded `.zip` file.
   
   ![Extract Template](img/2.png)

### 3️⃣ Deploy Your Game from RPG Maker
---
- **MV:** Choose `Web Browser` as the deployment platform.
  
  ![MV Deployment](img/3mv.png)
  
- **MZ:** Choose `Web Browser / Android / iOS`.
  
  ![MZ Deployment](img/3mz.png)

### 4️⃣ Place Game Files in the Android Project
---
1. Navigate to the extracted project folder.
2. Go to `RPG-Maker-to-Android-project/app/src/main/assets/www`.
3. Copy and paste the deployed game files into this folder. Ensure `index.html` is directly inside it and **not nested in another `www` folder**.
   
   ![Game Files](img/4.png)

### 5️⃣ Open the Template in Android Studio
---
1. Open **Android Studio** and select `Open an existing project`.
2. Navigate to the extracted template folder and open it.
3. Click `Trust Project` if prompted.
   
   ![Open Project](img/5.png)
   
5. Wait for Gradle to sync (this may take a few minutes).
6. If you see an **Invalid Gradle JDK Configuration Found**, select the latest JDK installed on your system or download a new one.
   
   ![JDK Error](img/5error.png)

### 6️⃣ Change Package Name
---
1. Expand `app > kotlin/java`.
2. Right-click `com.rpgmakergame.rpgmakertemplate` > `Refactor` > `Rename` > `All Directories`.

   ![Change Package Name](img/6.png)

4. Enter your desired package name and confirm.

   ![Rename Package](img/6rename.png)

5. Also change the names in build.gradle.kts (Module)

   ![Rename Gradle](img/6gradle.png)

   then press sycn now at the blue ribbon

   ![Sync now](img/6sync.png)

### 7️⃣ Customize App Name and Icon
---
#### **A. Change App Name**
1. Expand `res > values`.
2. Open `strings.xml`.
3. Edit the `app_name` value.
   
   ![Change App Name](img/7a.png)

#### **B. Change App Icon**
---
1. Expand `res/`.
2. Right-click `mipmap` folder > `New` > `Image Asset`.
   
   ![Change App Icon](img/7b.png)
   
4. Customize the foreground and background images.
   
   ![Generate Icon](img/7bgenerate.png)
   
6. Click `Next` > `Finish`.

### 8️⃣ Generate Signed APK (for Distribution)
---
1. Open `Generate Signed Bundle / APK` from the Build menu.
   
   ![Generate APK](img/8menu.png)

   ![Select APK](img/8menu2.png)
   
3. Select `APK` (or `Android App Bundle` if publishing to Google Play Store).
   
   ![Choose APK](img/8apk.png)
   
5. Create a new keystore:
   - Fill out the form with your keystore details.
     
   ![Create Keystore](img/8key.png)
   
7. Click `Next`, select `Release`, and generate the APK.
   
   ![Build APK](img/8release.png)
   
9. The APK will be available in `RPG-Maker-to-Android-project/app/release/`, or click `Locate` in the notification.
   
   ![APK Generated](img/8done.png)


## 📢 Additional Notes
- If you want to **publish your game on the Play Store**, generate an **App Bundle** instead of an APK.
- If you experience **build errors**, check your **SDK and JDK versions** in Android Studio settings.
- For troubleshooting or additional customization, refer to the [official documentation](https://developer.android.com/studio).

## 📄 License

This project is licensed under the Apache 2.0 License - see the [LICENSE](LICENSE) file for details.

## 🙏 Credits

Created by [Reishandy](https://github.com/Reishandy)

## 🎮 Enjoy Making Your RPG Game on Android!
If this guide helped you, consider giving a ⭐ on [GitHub](https://github.com/Reishandy/RPG-Maker-to-Android)! 🚀
