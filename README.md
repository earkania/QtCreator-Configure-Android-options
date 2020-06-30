# Configuring Android Device options in Qt Creator 4.12.3
First of all you need **Java SE Development Kit 8** and Android SDK. 

You can download Java SE Development Kit For Windows x64 from this [link](https://download.oracle.com/otn-pub/java/jdk/8u251-b08/3d5a2bb8f8d4428bbe94aed7ec7ae784/jdk-8u251-windows-x64.exe) or feel free to use any other source.

For some reason my Qt Creator was not able automatically download Android SDK and I downloaded it from this [link](https://dl.google.com/android/repository/sdk-tools-windows-4333796.zip). I have found this link in file **sdk_definitions.json** which is located at C:\Users\\[User]\AppData\Roaming\QtProject\qtcreator\android\ folder (replace [User] with your account user name). 

When you have downloaded both files install Java SE Development Kit at the location of you choose. I have installed at default location C:\Program Files\Java\jdk1.8.0_251. Then I unzipped sdk tools at the default location suggested in Qt Creator (for me it was C:\Users\[User]\Android\sdk). 

Run Qt Creator and go to Tools -> Options, then select at the left list select Devices and Go to Android tab.

In the Java Settings group at the JDK location text box enter the path where you installed Java SE Development Kit (for me C:\Program Files\Java\jdk1.8.0_251)

In the Android Settings group at the Android SDK location enter the path where you unzipped android SDK (for me C:\Users\[User]\Android\sdk) QT will offer update SDK and you must agree some licence agreements. After that it will begin download updates and installs them. If you done everything correctly you will see avaialable android NDK at the Android NDK list listbox. 

If you wish to add **Open SSL** support then download **Android OpenSSL support project for Qt** from this [link](https://github.com/KDAB/android_openssl). In the Android SDK installation folder create sub folder named android_openssl and unzip downloaded file in this folder. In the Android OpenSSL settings group at OpenSSL .pri location textbox enter the path to the android_openssl folder (for me C:\Users\[User]\Android\sdk\android_openssl). 

When you done everything click OK button and you are setup for Android development in Qt Creator;

Feel free to add any Android Virtual Devices.

Below is a screenshot of my setup:
![Settings](https://github.com/earkania/QtCreator-Configure-Android-options/blob/master/settings.png)
