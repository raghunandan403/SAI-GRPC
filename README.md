# SAI-GRPC
Existing code is a copy of SAI @ https://github.com/opencomputeproject/SAI
the code mentioned above generates a .thrift apis using pearl and toolkit template.
We have modified the existing code and made it to generate a .proto.

This code will be merged to the https://github.com/opencomputeproject/SAI once we have take care of generating the .thrift and .proto based on the target given by the user.


Building the .proto file:
- go to SAI/meta
- run ./gensaigrpc.pl
- Following logs will be seen:
Building SAI meta XML...
make: Entering directory '/root/ragha/dash/DASH-GRPC/DASH/dash-pipeline/SAI/SAI/meta'
make: 'xml' is up to date.
make: Leaving directory '/root/ragha/dash/DASH-GRPC/DASH/dash-pipeline/SAI/SAI/meta'
Parsing...
Generating sai.grpc...
Generating gRPC files...

- At the end, sai.proto will be generated.

Adding/Updating new header files:
- go to : SAI/inc
- Add or modify any existing files.
- go back to SAI/meta
- run ./gensaigrpc.pl
