[![](https://img.shields.io/nuget/v/soenneker.extensions.spans.bytes.svg?style=for-the-badge)](https://www.nuget.org/packages/soenneker.extensions.spans.bytes/)
[![](https://img.shields.io/github/actions/workflow/status/soenneker/soenneker.extensions.spans.bytes/publish-package.yml?style=for-the-badge)](https://github.com/soenneker/soenneker.extensions.spans.bytes/actions/workflows/publish-package.yml)
[![](https://img.shields.io/nuget/dt/soenneker.extensions.spans.bytes.svg?style=for-the-badge)](https://www.nuget.org/packages/soenneker.extensions.spans.bytes/)
[![](https://img.shields.io/github/actions/workflow/status/soenneker/soenneker.extensions.spans.bytes/codeql.yml?label=CodeQL&style=for-the-badge)](https://github.com/soenneker/soenneker.extensions.spans.bytes/actions/workflows/codeql.yml)

# ![](https://user-images.githubusercontent.com/4441470/224455560-91ed3ee7-f510-4041-a8d2-3fc093025112.png) Soenneker.Extensions.Spans.Bytes
Securely clears sensitive bytes held in a `Span<byte>`.

## Installation

```bash
dotnet add package Soenneker.Extensions.Spans.Bytes
```

## Usage

```csharp
using Soenneker.Extensions.Spans.Bytes;

Span<byte> key = stackalloc byte[32];
// use key...
key.SecureZero();
```

`SecureZero()` mutates the supplied span in place and is exactly a convenience call to `CryptographicOperations.ZeroMemory`. Unlike an ordinary `Clear()`, the runtime guarantees the write will not be optimized away. It is appropriate for keys and other secrets once they are no longer needed.
