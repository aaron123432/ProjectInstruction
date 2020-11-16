# Overall ---  Restaurant Management System

Restaurant Management System is a duo platform software that can run on both Windows and the Android phone. For Windows platform, this system is mainly designed to help restaurant managers to check the inventory, arrange employee shifts, and handle customer’s questions or complaints. For Android, the app is used to check the delivery status of the customer’s order in real time. Both platforms have the same functionalities, but it is more commonly used by each group of people, it is not limited. Customers can use Windows versions of software to check their delivery orders, and the restaurant staff can use Android phones to perform the same daily tasks as needed.

This project is a two way communication between server and the software. Those two platforms are isolated. They are not directly connected but they are indirectly connected through a server. Due to the structure of this design, both platforms can synchronize the data in real time. Such as the delivery checking system, employee management system, and reservation system etc. Each functionality is running as an independent instance to interact with the server and update the data in the server to perform the real time transactions.

The server has a database running and with port forwarding technology. Each port  is open for access to the database from Android app or Windows software. So, there won’t be any interaction from software and the android app directly. The database is designed to store and update the data only. So the server is going to handle only the http request from both Android app and Windows software. 

Both Android app and Windows software are the access point to the database by port forwarding as well. Users don't need to join the same network to access the database due to the port forwarding technology. There is no authentication needed by the user, everything is preconfigured. Because of the nature of the structure, both software and application are only going to send the http request to the server and wait for the server's response. So, the software or application will display the information that is sent back from the server.
# Release Note
## October 18,2020
### Android App:

For the first demo, we finished the first version of sign in and sign up form. Now, users can register and log in using our software.
### Windows Software:
For the first demo, we finished the first version of sign in and sign up form. Now, users can register and log in using our software.

## October 31,2020
### New Features

#### Android App:

##### 1. Add four fragments for both employee and user Activity, UserInfoFragment,LogOutFragment, GoogleMapFragment, and HomeFragment.（Aaron & Winson)

a. UserInfoFragment allow user/employee to update their account informations, 

b. LogOutFragment allow user/employee to logout their account

c. GoogleMapFragment allow user/employee to track their order location

d. HomeFragment will display any orders that user placed or employee received


#### Windows Software:

##### 1. Add a new form,staff information form. (Zidong Wang)

a. This form is only visible to the owner  

 b. The owner can create, edit, and delete staff information here

##### 2. Add a new form,stock form.  (Zidong Wang)

a. This form is visible to the owner and employee. 
  
 b. The user can create, edit, and delete food material here. 

 c. The user can filter and manipulate a particular item.

 d. The user can check the safety stock
 
 ##### 3. Added to sign up process/forms.  (Dominic Taraska)
 
 a. More user info fields 
 
  b. Differentiation of employee/admin accounts 
  
  c. Account identifier (id) 
  
 
 ##### 4. Added authority checking for accounts.  (Dominic Taraska)
 
 a. A given account has an associated privilege that will determine what they can view
 
 b. Some minor integration with this for the 'Home' forms and 'Stock' forms 

##### 5. added Main page   (Sarah Noshin)

a. created  varaitions of main page form based on user acesss and permission
 
b. created navigation bar for user to access different part of the app
### Bug Fixes

#### Android App:

· GoogleMap is currently not working and Home fragment will not display anything because there is no order info in database.

· Fix the server issues that aws isn't running backend program correctly and keep shutting it down and every time reboot just constantly change its ip address(Aaron & Winson)

#### Windows Software:
· Fixed some issues that caused registration failures (Zidong Wang)


## November 16,2020
### Android App:

a.User will be able to see the order history after sign in

b.Delivery person(Employee) will see the their delivery history, coming order or currently delivery order status


#### Windows Software:

#### 1. Added 2D view form (Dominic)

a. User is presented with 2D view when 'Open' button on main menu is clicked 

b. As of right now, this 2D view provides nagivation to 5 information forms: Staff info, Orders info, Stock info, Reservation info, and Menu/Order taking

#### 2. Added Menu form: 4 menus and my cart (Sarah)
a. user is presented with the option to select from 4 different menu's and use my cart to order menu items

b. user can go in my cart tab to click start order

c. user can add menu items by choosing from 16 menu items and clicking on each one to add to order

d. user can hit refresh on my cart to see order

e. to search order : type in search bar and hit search button to filter item name, cost, description

f. to add an item : type in the empty input fields, hit add button 

g. to clear fields : hit clear button

h. to update an item : double click item on data grid view table, add button turns to update button, that menu item info will appear in input fields, adjust field information, hit update button

i. to delete an item : hit delete

j. to get total price : hit total 

k. as of right now there is a finish order button but it is not functional.

# Installation guide

## Android App:

Download the APK package to your android device from the downloads link and unzip the file to get the apk file. to install the app to your device, simplely drag the apk file to your device. After installation, you will need to open the app to access the login section of the app. Once you successfully login to the app, you will be either redirect to the user page or the employee page based on your account role. Also, you can create a account by clicking the sign up button, and then enter the informations to the form and click the submit, and then go to login page to login to your account. If testing with virtual phone, first go to https://developer.android.com/studio to download android studio and install it to your PC. Open Android Studio, on the top-right cornor, click on AVD Manager, to create a new virtual device. Click the create new device button, and choose Phone on the Category and choose any device model you would like and click next. After each Release Version, it shows the API Level of the system image, make sure choose API Level 29 or above version System image and click next and finish. After you created your android device , click run button to turn on your device and then drag the apk file you downloaded from the download link above. You should be successfully installed the app. (Making sure if you are first time using android studio, go to device setting and turn on the location permission for the app, otherwise sometimes the program will crash).

Downloads:

https://github.com/aaron123432/ProjectInstruction/blob/main/app-debug.apk

Recommanded device

1.Emulator from Android Studio(API level 29 or above)

2.Android device with version 10 or higher

## Windows Software:

Download the Installer on your Windows PC and open the file to install the software on your machine. First page will be the sign in page and you can either sign in or click sign up button to create a new account. 

Downloads: 

https://github.com/aaron123432/ProjectInstruction/blob/main/SetupDemo3.msi


# Testing Instruction

## Android App:

If run the app in Android Studio:

1.The home page contains two parts.(sign in and sign up)

2.Log in: input your username and password to log in. If you don't have an account, just click sign up button to create an account.

3.Sign up: input all the required field and click submit button. note(it can only sign up for user account on mobile app)

4.Home Fragment: after sign in to the app, the home fragment will display order history, but since there is no data in the database, so nothing will display at the screen.

5.UserInfo Fragment: on the top-left cornor, there is a menu bar, user can go to any fragment just by clicking the menu, and user can change the data in the field and click the 
submit button to update the info.

6.GoogleMap Fragment: on the menu bar, user can click the GoogleMap, and a google map will display on the screen.
If run the app in the physical Android phone:

Click the download link above, and install the apk file to your phone.

For user sign in:

tester can sign up a user account and log in with the account tester just created.

For employee sign in:

since sign up function will set account type to be customer by default, so use the account provided below to test.

username: 12345678

Password: 5678

## Windows Software:
### Log in and sign up
After finishing the installation, a file named "Restaurant Management System" will appear on the desktop.
1. The welcome page contains two parts. (sign in and sign up)
2. Log in: input your username and password to log in. If you don't have an account, please click  "Don't have an account?Click here" to sign up.
3. Sign up: input the username, email address, password and confirm password to finish the registration. Notice that the username you put may exist, you need to try another one. The password and confirm password need to match. 
4.  click sign up button to finish registration
5. We provide two user identities for testing.

a. owner

username: admin

password: 123

The owner can access both the stock and staff information page.

b. employee

username: employee

password: 123

### Stock form: food material information and the inventory

1.On the main page, you can see the stock button. Click it to display the stock form. 

2.In the stock form, you can add a new food martial information in the upper left corner. 

3.You can filter and search for some information by some specific condition, you can use one or more conditions to filter. 

4.The safe stock button which at the upper right corner will change the quantity to red if the quantity is less than safe stock. 

5. You can edit and delete some item's information in the grid.

### Staff information form: 
1. On the main page, you can see the staff button in the upper right corner. Click it to display the staff form.

2. On the left, it is a tree which includes all staff's name and their position. 

3. you can click their name and display their detailed information. 

4. At the top-left corner, there are three buttons there, you can click them to add new staff information and edit specific staff information (Note that, you should select a person and click the edit button). 

5. You need to input their information in the textbox on the right side of the form. 

6. You need to click save to complete the add or modify operation

7. You can delete a user's information by clicking the delete button at the right bottom. 


# Link of the source code

## Android App:
https://github.com/winsonwen/restaurant-management-system-frontend-android/tree/delivery-branch

## Windows Software:
https://github.com/DTaraska11/RestaurantManager/tree/master
