# Three Stories about Error Handling in Swift

This is a repository for the talk "Three Stories about Error Handling in Swift" by @koher in try! Swift Tokyo 2016.

- [Slides](slides.pdf)
- [Video](talk.mp4)

This talk is a parody of "[Steve Jobs' 2005 Stanford Commencement Address](https://www.youtube.com/watch?v=UF8uR6Z6KLc)".

## The First Story: Meeting the Optionals

## The Second Story: Success or Failure

## The Third Story: `try`

It refered to relationships between `throws/try` and `async/await`. It also proposed the syntax of `async/await` suitable for Swift.

```swift
func asyncGetInt(...) async -> Int {     // async
  ...
}

func printSum() async {                  // async
  let a: Int = await asyncGetInt(...)    // await
  let b: Int = await asyncGetInt(...)    // await
  print(a + b)
}
```

```swift
func failableGetInt(...) throws -> Int { // throws
  ...
}

func printSum() throws {                 // throws
  let a: Int = try failableGetInt(...)   // try
  let b: Int = try failableGetInt(...)   // try
  print(a + b)
}
```
