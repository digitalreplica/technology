is:: [[software]]
from:: [[linux]]

# Notes
Curl is a linux command to interact with web servers

## Common usages
* Download file `curl -O url`
* Verbose `curl -v`
* PUT `curl -v -X PUT`
* Adding Headers and data
  * `curl -v -H “Content-Type: application/json” -X PUT –data “@data.json”`
* Ignore self-sign certificate warning
  * `curl -k url`
  * `curl --insecure url`
* compressed page `curl --compressed`
* no status `curl -s`
