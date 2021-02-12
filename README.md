# Multithreading_Questions
this repo contains GCD and Operations Questions

### Question 1 - What will be output of this function?
```swift
func Question1() {
  print("1")
  DispatchQueue.main.async {
    print("2")
    DispatchQueue.main.async {
      print("3")
    }
    DispatchQueue.main.async {
      print("4")
    }
    print("5")
  }
}
```

### Question 2 - What will be output of this function?
```swift
func Question2() {
  print("1")
  DispatchQueue.main.sync {
    print("2")
    DispatchQueue.main.async {
      print("3")
    }
    print("4")
  }
}
```

### Question 3 - What will be output of this function?
```swift
func Question3() {
  print("1")
  DispatchQueue.main.async {
    print("2")
    DispatchQueue.main.sync {
      print("3")
    }
    print("4")
  }
}
```

### Question 4 - What will be output of this function?
```swift
func Question4() {
  print("1")
  DispatchQueue.main.async {
    print("2")
    DispatchQueue.main.async {
      print("3")
    }
    DispatchQueue.main.async {
      print("4")
    }
    DispatchQueue.main.async {
      print("5")
    }
    DispatchQueue.main.sync {
      print("6")
    }
    print("7")
  }
}
```

### Question 5 - What will be output of this function?
```swift
func Question5() {
  print("1")
  DispatchQueue.main.async {
    print("2")
    DispatchQueue.main.async {
      print("3")
    }
    DispatchQueue.main.sync {
      print("4")
    }
    DispatchQueue.main.async {
      print("5")
    }
    DispatchQueue.main.sync {
      print("6")
    }
    print("7")
  }
}
```

Answer sheet-
Answer1: 1 -> 2 -> 5 -> 3 -> 4
Answer2: 1 -> Deadlock
Answer3: 1 -> 2 -> Deadlock
Answer4: 1 -> 2 -> Deadlock
Answer5: 1 -> 2 -> Deadlock
