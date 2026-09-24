# Vortex Payments Go SDK

Generated Go SDK for the Vortex Payments public API.

This package is generated from `docs/openapi/vortex-public.openapi.json` by `pnpm run sdk:generate`.
It is MIT-licensed. The public module is `github.com/vortexnyc/vortex-go`.

```bash
go get github.com/vortexnyc/vortex-go
```

```go
import (
	"context"
	"os"

	vortex "github.com/vortexnyc/vortex-go"
)

// Point at the sandbox host for test data; vp_test_ keys are sandbox-only.
cfg := vortex.NewConfiguration()
cfg.Host = "api.sandbox.vortex.nyc"
cfg.Scheme = "https"
cfg.AddDefaultHeader("Authorization", "Bearer "+os.Getenv("VORTEX_API_KEY"))

client := vortex.NewAPIClient(cfg)
ctx := context.Background()

// Use client.PaymentsReadinessAPI.CreateMerchantAccount(ctx) ...
```
