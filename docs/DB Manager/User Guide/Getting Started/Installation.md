# Installation

# **Account Creation:** 

Before initiating the installation process, you must create an account on our service platform. Follow the link provided to register: [Create a new account](https://db-manager.bridge2.digital/auth/register).

# **Server Side Configuration**

## Preparing environment

Ensure that all the necessary software is installed before proceeding with the installation.

**Requirements**:

* Docker
* curl
* lsof


1. To install Docker, refer to the official documentation: [Docker Installation Guide](https://docs.docker.com/engine/install/).
2. For curl and lsof installation, execute the following commands based on your operating system:

   ```bash
   ## For debian
   sudo apt update && sudo apt install curl lsof
   
   ## For alpine
   sudo apk add curl lsof
   ```


3. The next step involves installing the DBvisor Agent. Execute the following command:

   ```bash
   ## For alpine
   curl http://db-manager-cli.bridge2.digital/download/dbvisor-agent-install | sh
   
   ## For debian
   curl http://db-manager-cli.bridge2.digital/download/dbvisor-agent-install | bash
   source ~/.bashrc
   ```


:::tip
**Important Note:** During the installation, you will be prompted for Docker installation. It is strongly recommended to use Docker. Non-Docker installation requires additional configurations on your end

:::

## Configurations


1. Add new server:

   ```bash
   dbvisor-agent app:server:add
   ```
2. Enter your email, password and workspace code.
3. Enter server name

After you added new server you can setup new Database. Go to [https://outline.bridge.digital./../DBVisor%20Agent/Database%20Management.md](https://outline.bridge.digital./../DBVisor%20Agent/Database%20Management.md/edit) to get more information how to add and manage your databases.


4. Also you can configure access to 

# Client side

The main requirements for this tool is PHP 8. It can be installed using following command:

```bash
sudo apt update && apt install php
```

Execute following command to install client side version.

```bash
curl http://db-manager-cli.bridge2.digital/download/install | bash
```

After it installed on locally you have to log in and enter public key provided by your administrator (person who has access to dbvisor agent / to the server):

* [How to generate keypair](https://outline.bridge.digital./../DBVisor%20Agent/Generate%20key-pairs.md)


* [How to save locally public key](https://outline.bridge.digital./../DBVisor%20Client/Save%20public%20key.md/edit)