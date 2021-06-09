The API is designed to control the your station from a script running on your computer. You can control all the parameters of your station and even get data from the API.

> :warning: We are still developing and testing this feature so the definitions are subject to changes. Please comply with the restrictions of each endpoint while we are improving the services.

## Authentication
All the API endpoints share the same authentication through a Bearer Token that can be provided by the telegram bot using the command: ` - `

Although public endpoints will answer wothout athentication, the number of allowed querys is higher for authenticated users, so we recomend using always authentication.

## Endpoitns

Each endpoint gives access to a different resource of the TinyGS system. Along with each endpoint url we provide the allowed methods. The base url for the API is ` --`.

### Station tx
**Url:** ` -- `

**Methods:** POST

**Responses:** 

 - 200 Transmission OK.
 - 428 tx disabled by config.

**Description:** Commands your station to transmit the given frame. The allow tx flag must be enabled on the firmware or the transmission will be prevented by hardware. The payload must be given in base64 format.

