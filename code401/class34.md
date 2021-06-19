# Read : 34

## API Deployment

### SSH

- SSH, or Secure Shell, is a remote administration protocol that allows users to control and modify their remote servers over the Internet. 

- The service was created as a secure replacement for the unencrypted Telnet and uses cryptographic techniques to ensure that all communication to and from the remote server happens in an encrypted manner. 

- It provides a mechanism for authenticating a remote user, transferring inputs from the client to the host, and relaying the output back to the client.

- The Secure Shell Protocol (SSH) is a cryptographic network protocol for operating network services securely over an unsecured network.

- Typical applications include remote command-line, login, and remote command execution, but any network service can be secured with SSH. 

- There are several ways to use SSH; one is to use automatically generated public-private key pairs to simply encrypt a network connection, and then use password authentication to log on. 

- Another is to use a manually generated public-private key pair to perform the authentication, allowing users or programs to log in without having to specify a password. In this scenario, anyone can produce a matching pair of different keys (public and private). 

- The public key is placed on all computers that must allow access to the owner of the matching private key (the owner keeps the private key secret). 

- While authentication is based on the private key, the key itself is never transferred through the network during authentication. 

- SSH only verifies whether the same person offering the public key also owns the matching private key. 

- In all versions of SSH it is important to verify unknown public keys, i.e. associate the public keys with identities, before accepting them as valid. Accepting an attacker's public key without validation will authorize an unauthorized attacker as a valid user. 


### Django Settings: Best practices

- The Settings file is a small but very important part of any Django project. 
- If you do it wrong, you’ll have a lot of issues during all phases of development. 
- But if you do it right, it will be a good basis for your project that will allow it to grow and scale in the future.

    - Keep settings in environment variables.
    - Write default values for production configuration *(excluding secret keys and tokens)*.
    - Don’t hardcode sensitive settings, and don’t put them in VCS.
    - Split settings into groups: Django, third-party, project.
    - Follow naming conventions for custom *(project)* settings.
    - **Naming Conventions:**
        - Give meaningful names to your settings.
        - Always use the prefix with the project name for your custom (project) settings.
        - Write descriptions for your settings in comments.




##### [Go Back](code_401_reading_notes.md)