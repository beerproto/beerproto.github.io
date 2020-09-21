# BeerProto

## Specification Doc

[BeerProto Specification](https://beerproto.github.io/beerproto/)

## About

Written as a pure computer interchange format for language-neutral, platform-neutral, extensible way of serializing structured data for use in communications protocols and data storage.

#### Protocol Buffer
BeerProto follows the structure of BeerJSON and can take advantages of the official code generating plugins for protocol buffers given support for C++, C#, Dart, Go, Java, Python, Ruby, Objective C, PHP and JavaScript as well as third part plugins such as Swift.

You can also use the Proto3 supports for canonical encoding in JSON, making it easier to share data in a human readable way.

#### Notes

Interoperability with BeerJSON can be achieved, but does require the conversion of the enumerators between int32's and strings and handling non nullables properties. To assit with this we provide a command line tool that can convert between BeerProto and BeerJSON.

## Go Reference

[Go Generated Code](reference/go-generated.md)

[Go Doc](https://pkg.go.dev/github.com/beerproto/beerproto_go?tab=doc)
