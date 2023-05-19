# otrace

opentelemtry tracing 

Library to help you setup open telemtry with jeager exporter

## Usage

```
go get -u github.com/NishanthSpShetty/otrace
```

```
import "github.com/NishanthSpShetty/otrace/trace"
```
### Setup provider config

```

config := trace.ProviderConfig{
	JaegerEndpoint: "",
	ServiceName:    "",
	ServiceVersion: "",
	Environment:    "",
	Disabled:       false,
}
  
tp, err := trace.NewProvider(config)
  
if err != nil{
...
}
defer tp.Close(ctx)
```

### tracing using functions exported from trace package
