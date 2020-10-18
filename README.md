# Overall ---  Restaurant Management System

Restaurant Management System is a duo platform software that can run on both Windows and the Android phone. For Windows platform, this system is mainly designed to help restaurant managers to check the inventory, arrange employee shifts, and handle customer’s questions or complaints. For Android, the app is used to check the delivery status of the customer’s order in real time. Both platforms have the same functionalities, but it is more commonly used by each group of people, it is not limited. Customers can use Windows versions of software to check their delivery orders, and the restaurant staff can use Android phones to perform the same daily tasks as needed.

This project is a two way communication between server and the software. Those two platforms are isolated. They are not directly connected but they are indirectly connected through a server. Due to the structure of this design, both platforms can synchronize the data in real time. Such as the delivery checking system, employee management system, and reservation system etc. Each functionality is running as an independent instance to interact with the server and update the data in the server to perform the real time transactions.

The server has a database running and with port forwarding technology. Each port  is open for access to the database from Android app or Windows software. So, there won’t be any interaction from software and the android app directly. The database is designed to store and update the data only. So the server is going to handle only the http request from both Android app and Windows software. 
Both Android app and Windows software are the access point to the database by port forwarding as well. Users don't need to join the same network to access the database due to the port forwarding technology. There is no authentication needed by the user, everything is preconfigured. Because of the nature of the structure, both software and application are only going to send the http request to the server and wait for the server's response. So, the software or application will display the information that is sent back from the server.
# What is new

## Andoird App:
For the first demo, we finished the first version of sign in and sign up form. Now, users can register and log in using our software.

## Windows Software:
For the first demo, we finished the first version of sign in and sign up form. Now, users can register and log in using our software.

# Installation guide

## Andoird App:

Download the APK package to your android device from the downloads link and unzip the file to get the apk file. to install the app to your device, simplely drag the apk file to your device. After installation, you will need to open the app to access the login section of the app. Once you successfully login to the app, you will be either redirect to the user page or the employee page based on your account role. Also, you can create a account by clicking the sign up button, and then enter the informations to the form and click the submit, and then go to login page to login to your account.

Downloads:

https://github.com/aaron123432/ProjectInstruction/raw/main/Android%20part.zip

Recommanded device

1.Emulator from Android Studio(API level 29 or above)

2.Android device with version 10 or higher

## Windows Software:

Download the Installer on your Windows PC and open the file to install the software on your machine. First page will be the sign in page and you can either sign in or click sign up button to create a new account. 

Downloads: 

https://github.com/aaron123432/ProjectInstruction/raw/main/Restaurant_Demo1.msi


# How to use

## Andoird App:

If run the app in Android Studio:

First go to https://developer.android.com/studio to download android studio and install it to your PC. Open Android Studio, on the top-right cornor, click on AVD Manager, to create a new virtual device. Click the create new device button, and choose Phone on the Category and choose any device model you would like and click next. After each Release Version, it shows the API Level of the system image, make sure choose API Level 29 or above version System image and click next and finish. After you created your android device , click run button to turn on your device and then drag the apk file you downloaded from the download link above. You should be successfully installed the app.

If run the app in the physical Android phone:

Click the download link above, and install the apk file to your phone.
## Windows Software:
After finishing the installation, a file named "Restaurant Demo" will appear on the desktop.
1. The welcome page contains two parts. (sign in and sign up)
2. Sign in: input your username and password to log in. If you don't have an account, please click  "Don't have an account?Click here" to sign up.
3. Sign up: input the username, email address, password and confirm password to finish the registration. Notice that the username you put may exist, you need to try another one. The password and confirm password need to match. 
4.  click sign up button to finish registration


# Link of the source code

## Andoird App:
https://github.com/winsonwen/restaurant-management-system-frontend-android/tree/delivery-branch

## Windows Software:
https://github.com/DTaraska11/RestaurantManager/tree/sarah
