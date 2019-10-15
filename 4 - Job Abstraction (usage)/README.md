# 4. Job Abstraction (usage)

## Steps

* Write a vexbot job (`jobs/vexbot.go`), equivalent to (`jobs/hexbot.go`)
* Start both jobs in the main
  * Use the `go` keyword to start a new goroutine
  * Create a channel and pass it to the jobs
  * Wait on the channel until both jobs have send a message
  * Use a type assertion switch/case to print what job the received `JobResult` came from

## New concepts

| Concept | Go | Python |
|---|---|---|
| Synchronizing threaded execution | The `go` keyword and channels [🔗](https://tour.golang.org/concurrency/2) | Possible to implement with a combination of [threads](https://docs.python.org/3.7/library/threading.html) and a [queue](https://docs.python.org/3/library/queue.html) |
| Infinite loop | `for` without arguments [🔗](https://tour.golang.org/flowcontrol/1) | `while True` [🔗](https://www.learnpython.org/en/Loops) |
| Single condition loop | `for` with one argument [🔗](https://tour.golang.org/flowcontrol/1) | `while` [🔗](https://www.learnpython.org/en/Loops) |
| C-style for loop | `for` with three arguments [🔗](https://tour.golang.org/flowcontrol/1) | `for` [🔗](https://www.learnpython.org/en/Loops) |
| Type assertion | `.(type)` [🔗](https://tour.golang.org/methods/15) | `isinstance` [🔗](https://docs.python.org/3.7/library/functions.html#isinstance) |
