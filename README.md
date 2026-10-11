# ESX Legacy Snippets

Snippet ของ ESX Legacy สำหรับไฟล์ Lua ใน [Zed](https://zed.dev)

Snippet อยู่ใน `snippets/lua.json` และถูกลงทะเบียนจาก `extension.toml`

## ติดตั้ง

1. เปิด Zed แล้วรันคำสั่ง `zed: install dev extension`
2. เลือกโฟลเดอร์ของ repository นี้
3. เปิดไฟล์ `.lua`

ถ้าเคยติดตั้งเวอร์ชันที่เผยแพร่ไว้แล้ว Zed จะใช้ dev extension นี้แทน

## ใช้ snippet

พิมพ์ `prefix` ในไฟล์ Lua แล้วเลือก snippet จากรายการเติมคำ

ตัวอย่าง:

| พิมพ์ | ได้ |
| --- | --- |
| `ESX.RegisterCommand` | คำสั่ง `ESX.RegisterCommand` |
| `ESX:playerloaded` | event `esx:playerLoaded` |
| `ESX.SharedObject` | `exports['es_extended']:getSharedObject()` |
| `xPlayer.addMoney` | `xPlayer.addMoney(money)` |

บาง snippet มี `$0` จุดนั้นคือตำแหน่งเคอร์เซอร์หลังวาง snippet กด Tab เพื่อไปจุดถัดไป

## แก้ snippet

แก้ที่ `snippets/lua.json` แต่ละรายการต้องมีชื่อกับ `body` ฟิลด์ `prefix` ใช้เป็นคำที่พิมพ์เรียก ถ้าไม่ใส่ `prefix` Zed จะใช้ชื่อ snippet แทน

```json
{
  "Get shared object": {
    "prefix": "ESX.SharedObject",
    "body": ["ESX = exports['es_extended']:getSharedObject()", "$0"],
    "description": "ESX shared object"
  }
}
```

เครื่องหมาย `$` ที่ไม่ใช่จุด Tab ต้องเขียนเป็น `\\$`
