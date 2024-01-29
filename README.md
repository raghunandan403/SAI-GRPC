# SAI-GRPC code version
Existing code is a copy of SAI @ https://github.com/opencomputeproject/SAI
- This repo generates a .thrift apis using pearl and toolkit template.

# What this repo is:
We have modified the existing SAI code (SAI @ https://github.com/opencomputeproject/SAI) and made it to generate a .proto.

# Will this code be merged
This code will be merged to the https://github.com/opencomputeproject/SAI once we have take care of generating the .thrift and .proto based on the target given by the user.
Final version will look like: .**/genrpc thrift or ./genrpc proto**


# Building the .proto file:
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

# Adding/Updating new header files:
- go to : SAI/inc
- Add or modify any existing files.
- go back to SAI/meta
- run ./gensaigrpc.pl
