# Language Specifications

## Syntax

### Variables
Support only immutable variables.

- Declaration variable: `let <Variable name> = <Value>;`

### Functions
Function arguments are all copying.

- Declaration function: `fn <Function name> <argument_1>: <type_1> <argument_2>: <type_2> ... -> <Return type> => <Function body>;`
- Another way of declaration function: `fn <Function name> <argument_1>: <type_1> <argument_2>: <type_2> ...;
                                        <Function name> <argument_1> <argument_2> => <Function body>;`

- Declaration variable/function without input: `let <Variable/Function name> = <Value/Function body>;`
- Call function: `<Function name>(<argument_1>, <argument_2>, ...)`

### Control Flow
Both can return value.

- If branch: `if <Conditions> => <True branch>; else if <Conditions> => <True branch>; else => <False branch>;`
- Match branch: `match <Value> {
            <Pattern_1> => <Process>;
            <Pattern_2> => <Process>;
            ...
            _ => <Default process>;
          };`

### Data Types
- Primitive types: `i32`, `i64`, `f32`, `f64`, `bool`, `string`, `tuple: (i32, string)`

### Comments
- Single line comment: `// This is a comment`
- Multi line comments: `/* This is a comment
                        This is too a comment*/`

### Others
Block can decide valid of variable.
- Block: `{}`

## Explanation
- Functions must have input and output.
- Functions with no input are defined as variables.
- Variables and functions are immutable by default.
