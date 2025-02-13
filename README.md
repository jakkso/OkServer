# OkServer!
_OkServer!_, or _OkS!_ for short, is a Go-based HTTP web server aimed to be lightweight, clean, and straightforward.
<img src="OkS.svg" width="300px" />

## Development
    git clone https://github.com/OkSProject/OkServer.git
    cd OkServer
    cp deployment/example.env .env
    make run

## Installation
    make && sudo make install

This copies the asset directory to `/opt/okserver`, along with the example env file and
creates a system user `okserver` to run the service. 

### `systemD`
If you wish to use `systemD`, see included service file, make any desired changes 
and install it.

    sudo cp deployment/okserver.service /etc/systemd/system/
    sudo systemctl daemon-reload
    sudo systemctl enable okserver.service
    sudo systemctl start okserver.service

## Configuration
Configuration is done via environmental variables.

| Name | Default Value |
| --- | --- |
| `OKSERVER_LOG_DIR` | `./log/` |
| `OKSERVER_ASSET_DIR` | `./www/html/` |
| `OKSERVER_PORT` | `8080` |

## To be worked on...
- Serve PHP, Python, and Go files.
- Ability to manage use/manage database(s).
- Ability to create .conf files for individual sites.

## Credits
_OkServer!_ and the _OkS!_ Project were started by Cole Rathbun (@cbrbygones), and is licensed under GPLv3 for anyone to use, modify, and redistribute.
