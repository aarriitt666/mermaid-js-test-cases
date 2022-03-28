Test cases
```mermaid
flowchart BT
    A[The First Box]-->B[Lead To Nowhere]
    C[More Baffling Than Ever]-->A
    D(Start to Wonder)
    E(I'm Cool)
    A-->D
    E-->G(E Are You Cool?)
    E<-->A
    F{What About Me?}
    H(Finish Yawning!)
    B<-->H
    F-->|No|D
    F-->|Yes|H
```

```mermaid
sequenceDiagram
    autonumber
    participant Client
    participant OAuthProvider
    participant Server
    Client->>OAuthProvider: Request Access Token
    activate OAuthProvider
    OAuthProvider->>Client: Send Access Token
    deactivate OAuthProvider
    Client->>Server: Request Resources
    activate Server
    Server->>OAuthProvider: Validating Token
    activate OAuthProvider
    OAuthProvider->>Server: Token is valid!
    deactivate OAuthProvider
    Server->>Client: Send Resources
    deactivate Server
```