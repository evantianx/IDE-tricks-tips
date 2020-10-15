### Hide and show Editor tabs

`tab pla no` => toggle `Tab placement | None`


### Zen Mode

`zen` => `Enter Zen Mode`

on this mode, you can navigate files with `L⌘` + `Up`

### SmartType

`R⌘` + `s` to narrow down code completion to what we want

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

### Completion with Tab

Completion with Tab key instead of Enter overwrites the identifier

```go
fmt.Println("hello")
// type Printf before Println and then hit Tab, Println will be replaced
fmt.Printf("hello")
```

### Create Undefined Type

```go
// message struct is not defined
// you can invoke by alt + enter to create a type here
// same for the field
msg := message{
    field1: 1,
    field2: "word"
}
```

### Extend/Shrink selection

`Alt` + `Up` to extend; `Alt` + `Down` to shrink  

### Add selection for Next Occurrence

`Ctrl` + `G` to add selection one by one; `Ctrl` + `Shift` + `G` to cancel selection one by one 

### Navigate files

- `Ctrl` + `Tab` open switcher;
- `⌘` + `E` open recent files;
- `⌘` + `Shift` + `E` open recent locations of current file
