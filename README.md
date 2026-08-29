[![](https://img.shields.io/nuget/v/soenneker.extensions.spans.bytes.svg?style=for-the-badge)](https://www.nuget.org/packages/soenneker.extensions.spans.bytes/)
[![](https://img.shields.io/github/actions/workflow/status/soenneker/soenneker.extensions.spans.bytes/publish-package.yml?style=for-the-badge)](https://github.com/soenneker/soenneker.extensions.spans.bytes/actions/workflows/publish-package.yml)
[![](https://img.shields.io/nuget/dt/soenneker.extensions.spans.bytes.svg?style=for-the-badge)](https://www.nuget.org/packages/soenneker.extensions.spans.bytes/)
[![](https://img.shields.io/github/actions/workflow/status/soenneker/soenneker.extensions.spans.bytes/codeql.yml?label=CodeQL&style=for-the-badge)](https://github.com/soenneker/soenneker.extensions.spans.bytes/actions/workflows/codeql.yml)

# ![](https://user-images.githubusercontent.com/4441470/224455560-91ed3ee7-f510-4041-a8d2-3fc093025112.png) Soenneker.Extensions.Spans.Bytes
Various helpful byte span extension methods.

## Installation

```bash
dotnet add package Soenneker.Extensions.Spans.Bytes
```

## Quick start

```csharp
using Soenneker.Extensions.Spans.Bytes;

// Given an existing Span<byte> named span:
span.SecureZero();
```

## Common operations

- `SecureZero()` - Overwrites the contents of the specified span with zeros in a manner designed to prevent the data from being recovered from memory. Equivalent to `CryptographicOperations.ZeroMemory(Spanbyte)`.
