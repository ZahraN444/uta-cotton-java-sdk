
# Item

## Structure

`Item`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `UUID` | Required | - | UUID getId() | setId(UUID id) |
| `Name` | `String` | Required | - | String getName() | setName(String name) |
| `Date` | `LocalDate` | Required | - | LocalDate getDate() | setDate(LocalDate date) |
| `DateTime` | `LocalDateTime` | Required | - | LocalDateTime getDateTime() | setDateTime(LocalDateTime dateTime) |
| `Decimal` | `double` | Required | - | double getDecimal() | setDecimal(double decimal) |
| `MLong` | `long` | Required | - | long getMLong() | setMLong(long mLong) |
| `Bool` | `boolean` | Required | - | boolean getBool() | setBool(boolean bool) |
| `CustomEnum` | [`CustomEnum`](../../doc/models/custom-enum.md) | Required | - | CustomEnum getCustomEnum() | setCustomEnum(CustomEnum customEnum) |
| `Status` | [`StatusEnum`](../../doc/models/status-enum.md) | Optional | - | StatusEnum getStatus() | setStatus(StatusEnum status) |
| `JsonObject` | `Object` | Required | A generic JSON object | Object getJsonObject() | setJsonObject(Object jsonObject) |
| `Animal` | `Object` | Required | - | Object getAnimal() | setAnimal(Object animal) |
| `Map` | [`Map<String, Message>`](../../doc/models/message.md) | Required | - | Map<String, Message> getMap() | setMap(Map<String, Message> map) |

## Example (as JSON)

```json
{
  "id": "550e8400-e29b-41d4-a716-446655440000",
  "name": "John Doe",
  "date": "2024-05-24",
  "dateTime": "05/24/2024 12:00:00",
  "decimal": 1234.56,
  "long": 1234567890123,
  "bool": true,
  "CustomEnum": "VALUE3",
  "jsonObject": {
    "key1": "val1",
    "key2": "val2"
  },
  "Animal": {
    "key1": "val1",
    "key2": "val2"
  },
  "Map": {
    "key0": {
      "code": 246,
      "text": "text4"
    },
    "key1": {
      "code": 246,
      "text": "text4"
    },
    "key2": {
      "code": 246,
      "text": "text4"
    }
  },
  "status": "active"
}
```

