# `base58` class

[`src/base58.php`](https://github.com/uplexa/uplexa-php/tree/master/src/base58.php)

A PHP Base58 codec

### Methods

 - [`encode`](#encode)
 - [`decode`](#decode)

#### `encode`

Encode a hexadecimal (Base16) string to Base58

Parameters:

 - `$hex <String>` A hexadecimal (Base16) string to convert to Base58

Return: `<String>`

`"UPX1ffK8ybGjhjQXReRxLDKPRBrsjXEzLcLGuHQZdmCBMd95K6PULopLLafQZf1MCCQoqf8mFEcnvhbP8n5SXtkN4F9Q3jN3Ru"`

#### `decode`

Decode a Base58 string to hexadecimal (Base16)

Parameters:

 - `$hex <String>` A Base58 string to convert to hexadecimal (Base16)

Return: `<String>`

`"0137F8F06C971B168745F562AA107B4D172F336271BC0F9D3B510C14D3460DFB27D8CEBE561E73AC1E11833D5EA40200EB3C82E9C66ACAF1AB1A6BB53C40537C0B7A22160B0E"`
