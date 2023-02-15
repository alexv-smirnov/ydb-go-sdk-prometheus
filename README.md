# metrics

metrics package helps to create ydb-go-sdk traces with monitoring over prometheus 

## Usage
```go
import (
    "github.com/ydb-platform/ydb-go-sdk/v3"
    ydbPrometheus "github.com/ydb-platform/ydb-go-sdk-prometheus"
)

...
    // init prometheus registry
	registry := prometheus.NewRegistry()

	db, err := ydb.Open(ctx,
		os.Getenv("YDB_CONNECTION_STRING"),
		ydbPrometheus.WithTraces(registry),
	)

```
