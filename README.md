# Vortex Payments Go SDK

Generated Go SDK for the Vortex Payments public API.

This package is generated from `docs/openapi/vortex-payments-public.openapi.json` by `pnpm run sdk:generate`.
It is MIT-licensed. The public module is `github.com/vortexnyc/payments-go`.

```bash
go get github.com/vortexnyc/payments-go
```

```go
import (
	"context"
	"os"

	vortexpayments "github.com/vortexnyc/payments-go"
)

// Point at the sandbox host for test data; vb_test_ keys are sandbox-only.
cfg := vortexpayments.NewConfiguration()
cfg.Host = "api.sandbox.vortex.nyc"
cfg.Scheme = "https"
cfg.AddDefaultHeader("Authorization", "Bearer "+os.Getenv("VORTEX_API_KEY"))

client := vortexpayments.NewAPIClient(cfg)
ctx := context.Background()

// Use client.PaymentsReadinessAPI.CreateMerchantAccount(ctx) ...
```
