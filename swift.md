# Swift

## Encode / Decode NSDictionary &lt;-&gt; String

```text
do {
    let jsonData =
    try JSONSerialization.data(withJSONObject: body, options: .prettyPrinted)
    let jsonString = String(bytes: jsonData, encoding: String.Encoding.utf8) ? ? invalidJson
}
catch {
}
```

```text
let jsonString = "{\"isfriend\" : 1,\"displayname\" : \"cchitsiang\",\n  \"enabled\" : \"1\"\n}"
let jsonData = jsonString.data(using: .utf8)
let body = try? JSONSerialization.jsonObject(with: jsonData!, options: .mutableLeaves) as! NSDictionary
```

