# Modified Whatsapp-API
<p align='center'>
  <img src="https://files.catbox.moe/7c3c55.jpeg" width="172">
</p>

--- 

## Usage
```json
"depencies": {
  "@whiskeysockets/baileys": "github:yifan-source/fixbail"
}
```
## Import
```javascript
const {
  default:makeWASocket,
  // Other Options 
} = require('@whiskeysockets/baileys');
```

---
# How To Connect To Whatsapp
## With QR Code
```javascript
const {
  default: makeWASocket
} = require('@whiskeysockets/baileys');

const YifanModss = makeWASocket({
  browser: ['Ubuntu', 'Chrome', '20.00.1'],
  printQRInTerminal: true
})
```

## Connect With Number
```javascript
const {
  default: makeWASocket,
  fetchLatestWAWebVersion
} = require('@whiskeysockets/baileys');

const YifanModss = makeWASocket({
  browser: ['Ubuntu', 'Chrome', '20.00.1'],
  printQRInTerminal: false,
  version: fetchLatestWAWebVersion()
  // Other options
});

const number = "628{numberCountry}";
const code = await YifanModss.requestPairingCode(number.trim) /* Use : (number, "YIFANTZY") for custom-pairing */

console.log("this pairing code : " + code)
```

# Sending messages

## send orderMessage
```javascript
const fs = require('fs');
const Y!fanImg = fs.readFileSync('./y!fanImage');

await YifanModss.sendMessage(m.chat, {
  thumbnail: Y!fanImg,
  message: "YifanModss; this image from Y!fanImg = FileSync('y!fanImage')",
  orderTitle: "YifanModss - KynaX",
  totalAmount1000: 72502,
  totalCurrencyCode: "IDR"
}, { quoted:m })
```

## send pollResultSnapshotMessage
```javascript
await YifanModss.sendMessage(m.chat, {
  pollResultMessage: {
    name: "YifanModss - KynaX",
    options: [
      {
        optionName: "Y!fan with KynaX"
      },
      {
        optionName: "KynaX with Y!fan"
      }
    ],
    newsletter: {
      newsletterName: "KynaX Invictus || Information",
      newsletterJid: "909@newsletter"
    }
  }
})
```

## send productMessage
```javascript
await YifanModss.relayMessage(m.chat, {
  productMessage {
    title: "YifanModss; titleMessage",
    description: "lapar",
    thumbnail: { url: "./y!fanImage" },
    productId: "EXAMPLE_TOKEN",
    retailerId: "EXAMPLE_RETAILER_ID",
    url: "https://youtube.com/@yifanoffc",
    body: "\n",
    footer: "YifanModss",
    buttons: [
      {
        name: "cta_url",
        buttonParamsJson: "{\"display_text\":\"Youtube YifanModss\",\"url\":\"https://youtube.com/YifanModss\"}"
      }
    ],
    priceAmount1000: 72502,
    currencyCode: "IDR"
  }
})
```
