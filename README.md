# React Native JSON Tokens JS


React Native library for signing, decoding, and verifying JSON Web Tokens (JWTs)

### Installation

```
npm install react-native-jsontokens
```

### Signing Tokens

```js
import { TokenSigner } from 'react-native-jsontokens'

const rawPrivateKey = '278a5de700e29faae8e40e366ec5012b5ec63d36ec77e8a2417154cc1d25383f'
const tokenPayload = {"iat": 1440713414.85}
const token = new TokenSigner('ES256k', rawPrivateKey).sign(tokenPayload)
```

### Creating Unsecured Tokens

```js
import { createUnsecuredToken } from 'react-native-jsontokens'

const createUnsecuredToken(tokenPayload)
```

### Decoding Tokens

```js
import { decodeToken } = from 'react-native-jsontokens'
const tokenData = decodeToken(token)
```

### Verifying Tokens

```js
import { TokenVerifier } from 'react-native-jsontokens'
const rawPublicKey = '03fdd57adec3d438ea237fe46b33ee1e016eda6b585c3e27ea66686c2ea5358479'
const verified = new TokenVerifier('ES256k', rawPublicKey).verify(token)
