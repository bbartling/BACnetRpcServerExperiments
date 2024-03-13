# bacpypes3RcpServer

Experimental project to make a RPC server for BACnet requests.

```bash
grpc_project/
│
├── rust_client/            # Rust client project root
│   ├── src/
│   │   └── main.rs         # Rust client source code
│   ├── proto/              # Optional: Directory for .proto files (if you prefer organizing them separately)
│   │   └── pingpong.proto  # The .proto file (can be located directly in rust_client or inside a subdirectory like this)
│   ├── Cargo.toml          # Rust project manifest
│   ├── Cargo.lock          # Automatically generated by Cargo, tracks dependencies
│   └── build.rs            # Build script for compiling .proto files
│
└── rpc_server/             # Python server and .proto file location
    ├── server.py
    ├── client.py
    ├── pingpong.proto
    ├── pingpong_pb2.py
    └── pingpong_pb2_grpc.py
...

```

## Install py pacakges
1. `$ python -m pip install grpcio grpcio-tools`

## Setup grpc
1. `$ python -m grpc_tools.protoc -I./proto --python_out=./proto --grpc_python_out=./proto ./proto/pingpong.proto`