# Creating Alerts 

### There are 3 key steps needed to create an Alert :

1. Create an alert
1. Add an action (Button)
1. Display the alert

---

### Creating an alert with a single button :

```swift
class ViewController: UIViewController {

    @IBAction func showAlertButtonTapped(_ sender: UIButton) {

        // create the alert
        let alert = UIAlertController(title: "Your Title", message: "This is your message.", preferredStyle: .alert)

        // add an action (button)
        alert.addAction(UIAlertAction(title: "OK", style: .default, handler: nil))

        // show the alert
        self.present(alert, animated: true, completion: nil)
    }
}
```

### Creating an alert with two buttons :

```swift
class ViewController: UIViewController {

    @IBAction func showAlertButtonTapped(_ sender: UIButton) {

        // create the alert
        let alert = UIAlertController(title: "Your Title", message: "Alerts with two buttons", preferredStyle: .alert)

        // add the actions (buttons)
        alert.addAction(UIAlertAction(title: "Continue", style: .default, handler: nil))
        alert.addAction(UIAlertAction(title: "Cancel", style: .cancel, handler: nil))

        // show the alert
        self.present(alert, animated: true, completion: nil)
    }
}
```

### Creating an alert with three buttons :

```swift
class ViewController: UIViewController {

    @IBAction func showAlertButtonTapped(_ sender: UIButton) {

        // create the alert
        let alert = UIAlertController(title: "Notice", message: "Are you sure you need three buttons in an alert?", preferredStyle: UIAlertController.Style.alert)

        // add the actions (buttons)
        alert.addAction(UIAlertAction(title: "Yes", style: .default, handler: nil))
        alert.addAction(UIAlertAction(title: "Cancel", style: .cancel, handler: nil))
        alert.addAction(UIAlertAction(title: "Try something else", style: .destructive, handler: nil))

        // show the alert
        self.present(alert, animated: true, completion: nil)
    }
}
```
