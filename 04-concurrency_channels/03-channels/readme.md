## Channels - Concurrency and Channels
Channels are a reference type that provide a safe mechanism to share data between goroutines. Unbuffered channel give a guarantee of delivery that data has passed from one goroutine to the other. Buffered channels allow for data to pass through the channel without such guarantees. Unbuffered channels require both a sending and receiving goroutine to be ready at the same instant before any send or receive operation can complete. Buffered channels don't force goroutines to be ready at the same instant to perform sends and receives.

## Notes

* Unbuffered channels provide a guarentee that data has been exchanged at some instant.
* Buffered channels provide great support for managing goroutines and resources.
* Closed channels can provide a system wide mechanism for notifications.

## Code Review

[Unbuffered channels - Tennis game](example1/example1.go) ([Go Playground](http://play.golang.org/p/7WO_eOJx_G))

[Unbuffered channels - Relay race](example2/example2.go) ([Go Playground](http://play.golang.org/p/5B1MxmDuZI))

[Buffered channels - Manage concurrency](example3/example3.go) ([Go Playground](http://play.golang.org/p/G9Gfy1drox))

[Timer channels and Select](example4/example4.go) ([Go Playground](http://play.golang.org/p/XazqxkgLSS))

## Advanced Code Review

[Semaphores](advanced/semaphore/semaphore.go) ([Go Playground](http://play.golang.org/p/opoZfMNhng))


[Pooling](advanced/pool/pool.go)

## Exercises

### Exercise 1
Write a program where two goroutines pass an integer back and forth ten times. Display when each goroutine receives the integer. Increment the integer with each pass. Once the interger equals ten, terminate the program cleanly.

[Answer](exercises/exercise1/exercise1.go) ([Go Playground](http://play.golang.org/p/3ry3sCIfaC))

### Exercise 2
Write a problem that uses a buffered channel to maintain a buffer of four strings. In main, send the strings 'A', 'B', 'C' and 'D' into the channel. Then create 20 goroutines that receive a string from the channel, display the value and then send the string back into the channel. Once each goroutine is done performing that task, allow the goroutine to terminate.

[Answer](exercises/exercise2/exercise2.go) ([Go Playground](http://play.golang.org/p/B9npiUVveE))

___
[![GoingGo Training](../../00-slides/images/ggt_logo.png)](http://www.goinggotraining.net)
[![Ardan Studios](../../00-slides/images/ardan_logo.png)](http://www.ardanstudios.com)
[![GoingGo Blog](../../00-slides/images/ggb_logo.png)](http://www.goinggo.net)