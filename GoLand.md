### Hide and show Editor tabs

`tab pla no` => toggle `Tab placement | None`


### Zen Mode

`zen` => `Enter Zen Mode`

on this mode, you can navigate files with `L⌘` + `Up`

### SmartType

`R⌘` + `s` to keep code completion close to what we want

### Postfix Completion

- use `.var` after methods to deal with return value

  ```go
  func sendMessage(msg string) (int, error) {
      return fmt.Println(msg)
  }

  sendMessage("hello world").var  
  // type .var and then tab => GoLand will help us to produce below
  message, err := sendMessage("hello world")
  ```
- use `err.nn` & `err.panic` to deal with error

  ```go
  // type err.nn
  if err != nil {
      // type err.panic 
      panic(err)
  }
  ```
 
### Method-like Completion

This helps us quickly find functions that match their first parameter to the type we invoke it for

```go
msg := "hello world"

msg = msg.
// type . then type twice basic code completion ⌘ + space

msg = fmt.Printf(msg)
```
