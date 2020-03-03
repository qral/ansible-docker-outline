# Info

1. clone repo
2. create ansible user on server
3. have public key for this user
4. Edit hosts (IP address/hostname, port, public key)

Run:

    $ ansible-galaxy install -r requirements.yml
    $ ansible-playbook install_docker_and_outline.yml

Output:

    PLAY [ultravps] 
    TASK [geerlingguy.docker : Install Docker.] 
    ok: [ultravps]
    ...
    PLAY [ultravps] 
    TASK [Outline bash installation script] 
    changed: [ultravps]
    TASK [debug]
    ok: [ultravps] => {
        "msg": [
            [
                "> Verifying that Docker is installed .......... OK",
                "> Verifying that Docker daemon is running ..... OK",
                "> Creating persistent state dir ............... OK",
                "> Generating secret key ....................... OK",
                "> Generating TLS certificate .................. OK",
                "> Generating SHA-256 certificate fingerprint .. OK",
                "> Writing config .............................. OK",
                "> Starting Shadowbox .......................... OK",
                "> Starting Watchtower ......................... OK",
                "> Waiting for Outline server to be healthy .... OK",
                "> Creating first user ......................... OK",
                "> Adding API URL to config .................... OK",
                "> Checking host firewall ...................... OK",
                "",
                "CONGRATULATIONS! Your Outline server is up and running.",
                ""
                ...
                ...
            ],
            "--- COPY LINES BELOW to Outline Manager ---",
            {
                "apiUrl": "https://xx.yy.zzz.qq:12345/sdfasdfasdfasdfdf_AAAA",
                "certSha256": "CF2342342CF23423423CF23423423CF23423423CF2342"
            }
        ]
    }




Copy **{ "apiUrl" .... }** to Outline Manager (with curly braces)..
