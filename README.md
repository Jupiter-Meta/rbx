
### Setting Up Rubix-Explorer

1. **Clone the Repository**

   Clone the Rubix-Explorer repository from GitHub using the following link:
   
   ```bash
   git clone https://github.com/Jupiter-Meta/rbx.git
   ```

2. **Prepare IPFS**

   Before proceeding, ensure that you have IPFS installed and running. You can run the IPFS daemon separately. Make sure it's running on the default port `5002`.

3. **Navigate to the Rubix-Explorer Folder**

   Open a PowerShell terminal and navigate to the Rubix-Explorer folder:

   ```bash
   cd rbx
   ```

4. **Setup Node and Create DID**

   Run the following commands to set up a Rubix node and create a DID (Decentralized Identifier):

   ```bash
   ./rubixgoplatform.exe run -p node0 -n 0 -s -port 20000
   ./rubixgoplatform.exe createdid -port 20000
   ```

5. **Setup Quorum**

   Configure a quorum by running the following command. Replace `<did>` with the DID you obtained in step 4:

   ```bash
   ./rubixgoplatform.exe setupquorum -did <did> -port 20000
   ```

6. **Add Quorum to Sender Node**

   To add a quorum to the sender node, run the following command. Replace `<port of the sender node>` with the port of the sender node, and provide the `quorumList.json` file as needed:

   ```bash
   ./rubixgoplatform.exe addquorum -port <port of the sender node> -quorumList quorumList.json
   ```

7. **Generate Test RBT Tokens**

   Generate test RBT tokens with the following command. Replace the DID and specify the number of tokens you want to generate:

   ```bash
   ./rubixgoplatform.exe generatetestrbt -port 20003 -did bafybmia3cujkg6aouqyvdmsfsy3hhjdq3zaayeuzviwn47j5k2qatdaive -numTokens 20
   ```

8. **Create Additional Nodes**

   You can create additional nodes by changing the port number, node number, and other parameters like `-p` and `-n`.

### Addressing IPFS Configuration Errors

#### Error 1 - IPFS Configuration

1. Open IPFS Desktop.

2. Navigate to **Settings**.

3. Under **IPFS CONFIG**, find the "API" field and change it to the following value:

   ```
   "API": "/ip4/127.0.0.1/tcp/5002"
   ```
#### Error 2 - Libp2pStreamMounting
1. Enable "Libp2pStreamMounting" if it's not already enabled.

2. Save your changes and restart the IPFS daemon.

