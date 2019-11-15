# Proxt-Re-Encryption

Proxy Re-Encryption in Cloud Services

![](Proxy%20Renecryption/1.png)

A proxy is, in essence, any provider. In general, the proxy or cloud provider never sees the actual secret message. It can only see encrypted messages and public keys. Private keys are given to individuals and are not revealed. Now the secret message can only be decrypted by the intended recipient, not the proxies. So, the proxy can never see the information. Proxies are Cloud Providers, Members in a Chat Group, Participants in a network, etc. For security reasons, proxies may not always be trusted. So data is encrypted with public keys and stored in an encrypted format especially into the cloud. Here data is safe and (theoretically) only the owner can access it since it is encrypted with owners' public key. Now the problem arises if a third party needs to access the data. There are two ways this can be achieved.

![](Proxy%20Renecryption/4.png)
![](Proxy%20Reencryption/5.png)

Alice wants to send the stored encrypted data to Bob. Alice has to get Bob's public key, decrypt the stored data, re-encrypt it with Bob’s public key and send it to Bob. This requires Alice to decrypt, then re-encrypt it for Bob and works only if there is one Bob. If Alice wants to send the stored data to many third parties, this method doesn't work as it takes a lot of decryptions and re-encryptions.

![](Proxy%20Renecryption/3.png)

Instead, Alice can retrieve Bob’s public key and issue a “re-encryption” key. This key represents the trusted relationship Alice has with Bob. Alice can send this data to the cloud provider and the cloud provider can proceed to re-encrypt the already encrypted data that is stored in the cloud using the re-encryption key. Bob can download this re-encrypted data and decrypt it as well. This is possible because the initial data is encrypted with Bob’s public key.

![](Proxy%20Renecryption/6.png)

In the second scenario, the decryption / re-encryption process is sidestepped and Alice doesn't need to perform this operation on their own devices. Instead, all they need to do is generate a key that should be quick, and pass it to the cloud provider, which at no point can decrypt the original message, making this system very scalable and enables data-sharing apps in a cloud environment.


