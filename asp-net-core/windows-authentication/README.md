*add Microsoft.AspNetCore.Authentication.Negotiate*
```
dotnet add package Microsoft.AspNetCore.Authentication.Negotiate
```

*Add authentication services by invoking AddAuthentication (Microsoft.AspNetCore.Server.IISIntegration namespace) in Program.cs*
```csharp
builder.Services.AddAuthentication(NegotiateDefaults.AuthenticationScheme).AddNegotiate();

builder.Services.AddAuthorization(options =>
{
    options.FallbackPolicy = options.DefaultPolicy;
});

// ...

app.UseAuthentication();
app.UseAuthorization();
```

*Selecting the scheme with the Authorize attribute*
```csharp
[Authorize(AuthenticationSchemes=NegotiateDefaults.AuthenticationScheme)]
public class ValuesController : Controller
{
    // ...
}
```