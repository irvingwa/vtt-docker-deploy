# Foundry VTT Docker Deployment

This repository aims to help speed up the deployment of Foundry VTT so you can get rolling faster. This compose will utilizes Traefik, and DuckDns to route to the foundry container.

## Pre-Installation

You must setup Port Forwarding for port 80 and port 443 on your router to the IP you are running this installation on.

You must have a domain from DuckDNS (its free) [DuckDNS](https://www.duckdns.org/domains)

You must have Docker and Docker-Compose installed on your system

## Installation

Clone or download this repository into the location where you would like to run foundry.

## Usage

Rename the sample.env file to just be .env
```
FOUNDRY_PASSWORD=myfoundrypassword # This is your password to login to foundry
FOUNDRY_USERNAME=myfoundryuser # This is your username to login to foundry
FOUNDRY_ADMIN_KEY=adminpos # This is the admin password to access your games
HOST_NAME=myhostname.duckdns.org # This is the hostname you created on DuckDNS
SUB_DOMAIN=myhostname # This is the hostname you created on DuckDNS but shorter
DUCK_TOKEN=myduckdnstoken # This is the token at the top of your DuckDNS page
TIME_ZONE=America/Chicago # This is the Time Zone your server is in
EMAIL=myemail@email.com # This is your email
VTT_DATA_LOC=./vtt # This is any folder where you want your VTT Config/Data saved outside of the container
```

Then it's just running the following from the same directory the docker-compose.yml is in.

```
docker-compose up
```



## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
[MIT](https://choosealicense.com/licenses/mit/)