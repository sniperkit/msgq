# msgq
Convenience TCP wrapper around [mangos](http://github.com/gdamore/mangos) and [Iris](https://github.com/project-iris/iris) to avoid boilerplate code when generating 
new instances of SP (scalability protocols) patterns and some syntax sugar regarding sender/receiver functions. 
Does not abstract away mangos and iris-go libraries.


## New Instance Functions

```go
func NewBus(url string) (sock mangos.Socket, err error)
```

```go
func NewPair(url string) (sock mangos.Socket, err error)
```

```go
func NewPushPipeline(url string) (sock mangos.Socket, err error)
```

```go
func NewPullPipeline(url string) (sock mangos.Socket, err error)
```

```go
func NewPub(url string) (sock mangos.Socket, err error)
```

```go
func NewSub(url string) (sock mangos.Socket, err error)
```

```go
func NewRequest(url string) (sock mangos.Socket, err error)
```

```go
func NewReply(url string) (sock mangos.Socket, err error)
```

```go
func NewSurveyor(url string) (sock mangos.Socket, err error)
```

```go
func NewRespondent(url string) (sock mangos.Socket, err error)
```

## Sender Functions

**Dial first, then send**

```go
func Dial(sock mangos.Socket, url string) error
```

```go
func Send(sock mangos.Socket, msg []byte) error
```

## Receiver Functions

**Listen first, then receive**

```go
func Listen(sock mangos.Socket, url string) error
```

```go
func Receive(sock mangos.Socket) (msg []byte, err error)
```

## Example

See [https://github.com/ibmendoza/go-examples/tree/master/msgq](https://github.com/ibmendoza/go-examples/tree/master/msgq)

## License

MIT
