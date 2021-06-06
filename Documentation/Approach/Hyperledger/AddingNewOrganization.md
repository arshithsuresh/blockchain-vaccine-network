## How to Add A new organization to A Network
Breif Description on how to add a new Organanization to the Network  
  
### Create Cyrpto Materials using cryptogen or CA's  
Create the crypto material for the organization using the `cryptogen generate` command that comes with the hyperledger fabric tools. Make sure you have added the `fabric-samples\bin\` to your PATH, or else it might throw an error.  
`cryptogen generate --config=org-crypto.yaml --output="../organizations"`  
  
  This command will generate a folder in your organizations' folder, named `org.example.com` or the name specified in the *org-crypto.yaml* file.

Folder structure will look like this  
<details>
<summary>Folder Strcucture</summary>
<p>
  
```c#
 org3.example.com
    ├── ca
    │   ├── ca.org3.example.com-cert.pem
    │   └── priv_sk
    ├── msp
    │   ├── admincerts
    │   ├── cacerts
    │   │   └── ca.org3.example.com-cert.pem
    │   ├── config.yaml
    │   └── tlscacerts
    │       └── tlsca.org3.example.com-cert.pem
    ├── peers
    │   └── peer0.org3.example.com
    │       ├── msp
    │       │   ├── admincerts
    │       │   ├── cacerts
    │       │   │   └── ca.org3.example.com-cert.pem
    │       │   ├── config.yaml
    │       │   ├── keystore
    │       │   │   └── priv_sk
    │       │   ├── signcerts
    │       │   │   └── peer0.org3.example.com-cert.pem
    │       │   └── tlscacerts
    │       │       └── tlsca.org3.example.com-cert.pem
    │       └── tls
    │           ├── ca.crt
    │           ├── server.crt
    │           └── server.key
    ├── tlsca
    │   ├── priv_sk
    │   └── tlsca.org3.example.com-cert.pem
    └── users
        ├── Admin@org3.example.com
        │   ├── msp
        │   │   ├── admincerts
        │   │   ├── cacerts
        │   │   │   └── ca.org3.example.com-cert.pem
        │   │   ├── config.yaml
        │   │   ├── keystore
        │   │   │   └── priv_sk
        │   │   ├── signcerts
        │   │   │   └── Admin@org3.example.com-cert.pem
        │   │   └── tlscacerts
        │   │       └── tlsca.org3.example.com-cert.pem
        │   └── tls
        │       ├── ca.crt
        │       ├── client.crt
        │       └── client.key
        └── User1@org3.example.com
            ├── msp
            │   ├── admincerts
            │   ├── cacerts
            │   │   └── ca.org3.example.com-cert.pem
            │   ├── config.yaml
            │   ├── keystore
            │   │   └── priv_sk
            │   ├── signcerts
            │   │   └── User1@org3.example.com-cert.pem
            │   └── tlscacerts
            │       └── tlsca.org3.example.com-cert.pem
            └── tls
                ├── ca.crt
                ├── client.crt
                └── client.key
```

</p>
</details> 

