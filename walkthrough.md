1. Passbase expects Go version to be go1.15+

```sh
go get github.com/passbase/passbase-go@v1.0.2
```

2. Import `passbase` into your app

```go
package main

import (
	"context"
    "fmt"

	passbase "github.com/passbase/passbase-go"
)

func main() {
	client := passbase.NewAPIClient(passbase.NewConfiguration())
	ctx := context.WithValue(context.Background(), passbase.ContextAPIKey, passbase.APIKey{
		Key: "{{YOUR_SECRET_API_KEY}}",
    })

	settings, _, err := client.ProjectApi.GetSettings(ctx)
	if err != nil {
		panic(err)
	}
	fmt.Println("Setting for ", settings.Slug, "->", settings)
}
```
