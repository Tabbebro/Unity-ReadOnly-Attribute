# ReadOnly

A small Unity package that adds a [ReadOnly] attribute. Fields marked with it
stay visible in the Inspector but cannot be edited, which is useful for
debug values, runtime state, and references that should not be changed by hand.

## Installation

### Git URL

1. Open Window > Package Manager.
2. Click the + button and choose "Add package from git URL".
3. Paste the URL and click Add:

   https://github.com/yourname/com.yourname.readonly.git

To install a specific version, append a tag:

   https://github.com/yourname/com.yourname.readonly.git#1.0.0

### manifest.json

Add this line to the dependencies in Packages/manifest.json:

   "com.yourname.readonly": "https://github.com/yourname/com.yourname.readonly.git"

## Usage

[SerializeField, ReadOnly] int _health = 10;
[ReadOnly] public float Speed = 

## Notes

- Works with any serializable field, including arrays, Lists, structs & Classes.
- The attribute is in a Runtime assembly, the drawer is in an Editor-only assembly.
- It does not serialize the field. Combine it with [SerializeField] or use a public field.
