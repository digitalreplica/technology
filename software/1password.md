is:: [[software]]
equals:: https://1password.com/personal

# Notes

## Environment variables
- https://developer.1password.com/docs/cli/secrets-environment-variables
	- Install the [CLI](https://developer.1password.com/docs/cli/get-started)
	- Find the url to the password item and field, like `op://<vault-name>/<item-name>[/<section-name>]/<field-name>`
		- Do a `op item get {name} --format json` to return op urls for every field
	- Using environment variables
		- Export an environment variable using the op url
			- Example: `export GITHUB_TOKEN=op://development/GitHub/credentials/personal_token`
		- Run your command with op run
			- Example: `op run -- my_command`
	- Using environment file
		- Create a file ending in `.env` with environment variables set. Example
		```
		AWS_ACCESS_KEY_ID="op://development/aws/Access Keys/access_key_id"
		AWS_SECRET_ACCESS_KEY="op://development/aws/Access Keys/secret_access_key"
		```
	  - Run your command using op run
		  - Example: `op run --env-file="./prod.env" -- aws`
