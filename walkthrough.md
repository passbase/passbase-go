1. Passbase expects Go version to be go1.15+

```sh
go get github.com/passbase/passbase-go@v1.3.0
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

	identity, _, err := client.IdentityApi.GetIdentityById(ctx, "<uuid>")
	if err != nil {
		panic(err)
	}
	fmt.Println("Identity for ", identity.Id, "->", identity)
}
```
