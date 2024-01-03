# GO

You can find the UPS Widget Token Generation for GO Lang here.

## Using the Token Generation Library

need to utilize this package.
- First, download TokenGeneration.go from this repository. Add the file to your project.
- Next, install the package by using `go install`.
- Finally, import the package by using
  ```GO
  import {
        go/TokenGeneration
  }
  ```

Once the package is added and installed, you will be able to use the `UPSSDK` class and call the `generateToken` method.

# TokenGeneration Class
## Definition

Provides a package for generating an OAuth token to use with UPS Widgets.
```GO
package TokenGeneration
```
## Parameters

| Definition | Description |
|------------|-------------|
| clientId | Your Client Id found in the UPS Developer portal |
| clientSecret | Your Client Secret found in the UPS Developer portal |
| headers | A `map` of `[string]string` |
| postData | A `map` of `[string]string` |
| queryParams | A `map` of `[string]string` |

## Methods

| Definition | Description |
|------------|-------------|
| GenerateToken(clientId, clientSecret) | Returns a token using only the provided id and secret |
| GenerateToken(clientId, clientSecret, headers) | Returns a token using the provided id, secret, and additional request headers. |
| GenerateToken(clientId, clientSecret, nil, postData) | Returns a token using the provided id, secret, and additional request body properties|
| GenerateToken(clientId, clientSecret, headers, postData) | Returns a token using the provided id, secret, additional request headers, and additional requesty body properties |
| GenerateToken(clientId, clientSecret, headers, postData, queryParams) | Returns a token using the provided id, secret, additional request headers, additional requesty body properties, and additional query parameters |

## Example

```GO
clientId := "YOUR_CLIENT_ID";
clientSecret := "YOUR_CLIENT_SECRET";
headers := make(map[string]string)
headers["HEADER_KEY"] = "HEADER_VALUE"
postData := make(map[string]string)
postData["PROPERTY_NAME"] = "PROPERTY_VALUE"

response, err := TokenGeneration.GenerateToken(clientId, clientSecret, headers, postData, nil)
```
