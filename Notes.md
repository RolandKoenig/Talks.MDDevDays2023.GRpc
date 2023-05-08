# Links
- From WCF to gRPC: https://learn.microsoft.com/de-de/dotnet/architecture/grpc-for-wcf-developers/why-grpc 
- Proto3 Language guide: https://protobuf.dev/programming-guides/proto3/ 
- Decoder: https://protogen.marcgravell.com/decode
- Code Generator: https://protogen.marcgravell.com/
- Best Practices: https://protobuf.dev/programming-guides/dos-donts/

# Protobuf 'well known types'
- import "google/protobuf/wrappers.proto";
- import "google/protobuf/timestamp.proto";
- Url für timestamp-Typ: https://github.com/protocolbuffers/protobuf/blob/main/src/google/protobuf/timestamp.proto 

# dotnet-grpc load from url
- dotnet tool install -g dotnet-grpc
- dotnet-grpc add-url https://raw.githubusercontent.com/protobuf-net/protobuf-net/main/src/Tools/bcl.proto -o Common/bcl.proto --access Public -s None
- dotnet-grpc refresh
- dotnet-grpc remove https://raw.githubusercontent.com/protobuf-net/protobuf-net/main/src/Tools/bcl.proto

# List all tcp connections for HappyCoding.GRpcCommunication.ServerApp
- ps -a | grep HappyCoding.GRpcCommunication.ServerApp
- netstat -v | grep <ProcessId>
