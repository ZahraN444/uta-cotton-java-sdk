
# Multiple Arrays Request

## Structure

`MultipleArraysRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Array1` | `List<String>` | Required | An array containing items of type string | List<String> getArray1() | setArray1(List<String> array1) |
| `Array2` | `List<Integer>` | Optional | An array containing items of type integer | List<Integer> getArray2() | setArray2(List<Integer> array2) |

## Example (as JSON)

```json
{
  "Array1": [
    "Array19",
    "Array10"
  ],
  "Array2": [
    99,
    98,
    97
  ]
}
```

