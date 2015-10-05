# go-loggly

  Loggly client for Go.

  View the auto-generated [docs](http://godoc.org/github.com/segmentio/go-loggly).

## Installation

    $ go get github.com/segmentio/go-loggly

## Usage

```go

	package main
	
	import github.com/segmentio/go-loggly
	
	const logglyToken    = "insert-your-token-here"
	const logglyAccount  = "logglySubDomainAccountNameHere"
	const logglyUser     = "logglyUsername"
	const logglyPassword = "logglyP@$$w0rdH3r3"
	
	func main(){
	
		log := loggly.New( logglyToken, logglyAccount, logglyUser, logglyPassword )
		
		err := log.Alert("Hello, Loggly!")
		
		if err != nil {
			fmt.Println(err) // OHNOES!
		} else {
			fmt.Println("That seems to have gone well...")
		}
		
	}

```

## Debug

 Enable verbose debugging output using the __DEBUG__ environment variable, for exmaple `DEBUG=loggly`.

## License

MIT
