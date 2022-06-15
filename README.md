# ts-to-zod-array-optional-nullable

To reproduce the bug:

1. Clone the repo
2. `yarn install`
3. `yarn run example`

Expected output:
```
✖ Validating generated types
 »   Error: 'Example' is not compatible with 'exampleSchema':
 »   Argument of type 'Example' is not assignable to parameter of type '{ field?: (string | null)[] | undefined; }'.
 »     Types of property 'field' are incompatible.
 »       Type '(string | null)[] | null | undefined' is not assignable to type '(string | null)[] | undefined'.
 »         Type 'null' is not assignable to type '(string | null)[] | undefined'.
```
