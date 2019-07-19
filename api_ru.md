# Pixelstick API
Общение происходит через WebSocket в формате JSON. Каждый пакет имеет следующую структуру:
```
{
  "id": :id,
  "payload": :payload
}
```
Где:
- **id:** ID пакета
- **payload:** полезная нагрузка



## Server -> Client (0 - 127)


### Images
- **ID:** 0
- **Payload type:** array

#### Example
```
{
  "id": 0,
  "payload": ["test_color.bmp", "test_position.bmp"]
}
```


### Current image
- **ID:** 1
- **Payload type:** string

#### Example
```
{
  "id": 1,
  "payload": "test_color.bmp"
}
```


### Brightness
- **ID:** 2
- **Payload type:** integer
- **Payload range:** 0 - 255

#### Example
```
{
  "id": 2,
  "payload": 150
}
```


### Speed
- **ID:** 3
- **Payload type:** integer
- **Payload range:** 1 - 100

#### Example
```
{
  "id": 3,
  "payload": 11
}
```


### Gamma correction
- **ID:** 4
- **Payload type:** boolean

#### Example
```
{
  "id": 4,
  "payload": true
}
```


### Repeat
- **ID:** 5
- **Payload type:** boolean

#### Example
```
{
  "id": 5,
  "payload": false
}
```



## Client -> Server (127 - 255)


### Set image
- **ID:** 127
- **Payload type:** string

#### Example
```
{
  "id": 127,
  "payload": "test_color.bmp"
}
```


### Brightness
- **ID:** 128
- **Payload type:** integer
- **Payload range:** 0 - 255

#### Example
```
{
  "id": 128,
  "payload": 150
}
```


### Speed
- **ID:** 129
- **Payload type:** integer
- **Payload range:** 1 - 100

#### Example
```
{
  "id": 129,
  "payload": 11
}
```


### Gamma correction
- **ID:** 130
- **Payload type:** boolean

#### Example
```
{
  "id": 130,
  "payload": true
}
```


### Repeat
- **ID:** 131
- **Payload type:** boolean

#### Example
```
{
  "id": 131,
  "payload": false
}
```