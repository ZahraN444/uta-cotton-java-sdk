
# Tokens Request

## Structure

`TokensRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Scopes` | [`List<OAuthScopeOAuthACGEnum>`](../../doc/models/o-auth-scope-o-auth-acg-enum.md) | Required | List of scopes that apply to the OAuth token<br><br>**Constraints**: *Unique Items Required* | List<OAuthScopeOAuthACGEnum> getScopes() | setScopes(List<OAuthScopeOAuthACGEnum> scopes) |

## Example (as JSON)

```json
{
  "scopes": [
    "file_requests.read",
    "selection",
    "test1"
  ]
}
```

