# Flash-Chat

Chat application where user's can talk with each other, created with firebase's authentication and realtime database to store chat and login information. 

<img src="Flash Chat/Images.xcassets/Screen1.png" width="200" height="400" />

# Getting Started 

After the app is loaded, users will be directed to either the login or register page and then to the chat page. The user can view previous text from other users as well as themselves or they can type a new message to add to the history. 

# Built With

- Swift 
- UiKit
- CocoaPods
    - Firebase
        - FirebaseAuth
        - FirebaseDatabase
    - SVProgressHUD
    - ChameleonFramework

# App Icon Logo

<img src="Flash Chat/Images.xcassets/AppIcon.appiconset/Icon-40@2x.png" width="100" height="100" />

# Wireframe Layout

Storyboard for this project shown below:

<img src="Flash Chat/Images.xcassets/Screen2.png" width="500" height="400" />

# Code-Snippets
The code below is an example of using firebase in Swift when a user logs in. Firebase auth. checks the email and password from the inputs and then checks if the set matches any record in the database. If there is a match then user will be directed to the chat page, otherwise an error will print out. 

```
SVProgressHUD.show()
        
//TODO: Log in the user
Auth.auth().signIn(withEmail: emailTextfield.text!, password: passwordTextfield.text!) { (user, error) in
    
    if error != nil {
        print(error!)
    } else
    {
        print("login success")
        SVProgressHUD.dismiss()
        self.performSegue(withIdentifier: "goToChat", sender: self)
    }
}
```

# Author
* **Muhammad** - https://github.com/mawais54013