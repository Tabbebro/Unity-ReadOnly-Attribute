# ReadOnly Attribute

Unity package that adds a `[ReadOnly]` attribute. Fields marked with it stay visible in the Inspector but cannot be edited. Useful for debug values, runtime state, and references that should not be changed by hand.

## Features

- Shows any serialized field as non-editable in the Inspector
- Works with arrays, lists, and structs
- Combines with `[SerializeField]` for private fields
- Editor drawer is isolated in an Editor-only assembly, so builds are unaffected

## Requirements

- Unity 2022.1 or newer
- Git installed and available on your PATH (required by the Package Manager for git URLs)

## Installation

### Package Manager (recommended)

1. Open `Window > Package Manager`.
2. Click `+` > `Add package from git URL...`.
3. Paste the repository URL and click `Add`:
```
https://github.com/Tabbebro/Unity-ReadOnly-Attribute.git
```

## Usage

Add `[ReadOnly]` to a field. The attribute does not serialize the field, so combine it with `[SerializeField]` for private fields:

```csharp
using UnityEngine;

public class Player : MonoBehaviour
{
    // Serialized and shown greyed out in the Inspector
    [SerializeField, ReadOnly] int _health = 10;
}
```

## Uninstalling

Open `Window > Package Manager`, select ReadOnly, and click `Remove`. Remove any `[ReadOnly]` usages from your scripts first, or they will fail to compile.
