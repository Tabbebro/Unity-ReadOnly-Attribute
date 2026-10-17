# ReadOnly

A small Unity package that adds a [ReadOnly] attribute. Fields marked with it
stay visible in the Inspector but cannot be edited, which is useful for
debug values, runtime state, and references that should not be changed by hand.

## Usage

[SerializeField, ReadOnly] int _health = 10;
[ReadOnly] public float Speed = 

## Notes

- Works with any serializable field, including arrays, Lists, structs & Classes.
- The attribute is in a Runtime assembly, the drawer is in an Editor-only assembly.
- It does not serialize the field. Combine it with [SerializeField] or use a public field.