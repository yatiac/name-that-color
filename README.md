![npm](https://img.shields.io/npm/v/@yatiac/name-that-color)
![npm](https://img.shields.io/npm/dw/@yatiac/name-that-color)
# ntc (name that color)

npm package for library `name that color` created by Chirag Mehta (http://chir.ag/projects/name-that-color). Credits go to him.
# Install
```
npm install @yatiac/name-that-color
```
# Usage
Receives any hex color code
### Approximate color:
```javascript
const ntc = require('@yatiac/name-that-color');

console.log(ntc('#9fa632'));
```

Result: 
```json
{ 
    "exactMatch": false, 
    "colorName": "Sushi", 
    "closestColor": "87AB39" 
}
```

###  With exact match:
```javascript
const ntc = require('@yatiac/name-that-color');

console.log(ntc('#000000'));
```

Result:
```json
{ 
    "exactMatch": true, 
    "colorName": "Black", 
    "closestColor": "#000000" 
}
```
### Invalid color code:
```javascript
const ntc = require('@yatiac/name-that-color');

console.log(ntc('#yatiac'));
```
Result:
```json
{
  "closestColor": "#000000",
  "colorName": "Invalid Color: #9FA6S32",
  "exactMatch": false
}
```
