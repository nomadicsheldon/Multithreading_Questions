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

### Question 6 - What will be output of this function?
```swift
func Question6() {
  print("1")
    DispatchQueue.main.sync {
      print("2")
    }
    DispatchQueue.main.async {
      print("3")
    }
    DispatchQueue.main.async {
      print("4")
    }
    DispatchQueue.main.sync {
      print("5")
    }
    print("6")
}
```

### Question 7 - What will be output of this function?
```swift
func Question7() {
  let dispatchLabel = "com.himanshu.test"
  let queue = DispatchQueue(label: dispatchLabel)
  print("1")
  queue.async {
    print("2")
    queue.async {
      print("3")
    }
    queue.async {
      print("4")
    }
    print("5")
  }
}
```

### Question 8 - What will be output of this function?
```swift
func Question8() {
  let dispatchLabel = "com.himanshu.test"
  let queue = DispatchQueue(label: dispatchLabel)
  print("1")
  queue.sync {
    print("2")
    queue.async {
      print("3")
    }
    print("4")
  }
}
```

### Question 9 - What will be output of this function?
```swift
func Question9() {
  let dispatchLabel = "com.himanshu.test"
  let queue = DispatchQueue(label: dispatchLabel)
  print("1")
  queue.async {
    print("2")
    queue.sync {
      print("3")
    }
    print("4")
  }
}
```

### Question 10 - What will be output of this function?
```swift
func Question10() {
  let dispatchLabel = "com.himanshu.test"
  let queue = DispatchQueue(label: dispatchLabel)
  print("1")
  queue.async {
    print("2")
    queue.async {
      print("3")
    }
    queue.async {
      print("4")
    }
    queue.sync {
      print("5")
    }
    print("6")
  }
}
```

### Question 11 - What will be output of this function?
```swift
func Question11() {
  let dispatchLabel = "com.himanshu.test"
  let queue = DispatchQueue(label: dispatchLabel)
  print("1")
  queue.async {
    print("2")
    queue.async {
      print("3")
    }
    queue.sync {
      print("4")
    }
    queue.async {
      print("5")
    }
    queue.sync {
      print("6")
    }
    print("7")
  }
}
```

Answer sheet-
1. Answer1: 1 -> 2 -> 5 -> 3 -> 4
2. Answer2: 1 -> Deadlock
3. Answer3: 1 -> 2 -> Deadlock
4. Answer4: 1 -> 2 -> Deadlock
5. Answer5: 1 -> 2 -> Deadlock
6. Answer6: 1 -> Deadlock
7. Answer7: 1 -> 2 -> 5 -> 3 -> 4
8. Answer8: 1 -> 2 -> 4 -> 3
9. Answer9: 1 -> 2 -> Deadlock
10. Answer10: 1 -> 2 -> Deadlock
11. Answer11: 1 -> 2 -> Deadlock
