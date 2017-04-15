# SilverProtobuffer

Google Protocol Buffer v2.6 API auto packer 

## Project contains:

- java-android
	- Http API Request Android Framework
	- Demo of silver ProtoBuffer usage
- objc-ios
	- Http API Request iOS Framework
	- Demo of silver ProtoBuffer usage
- python-packer
	- API packer python script
	- Input Container
	- Output Demo
- server-sample 
	- A server sample code based on Spring Boot Framework that can be used for the demos above

## How to use it:

- Step 1: Prepared the .json file which contains the API spec definition and the related .proto files which contains the protobuf messages that API spec needs and put all of them into /python-packer/input.
- Step 2: Execute the python main.py and generate the code you need. If found some errors, please fix them and try again.
- Step 3: Import the iOS or Android SDK files into your project.
- Step 4: Put the generated code into your project.
- Step 5: Done! just try call the method in your code to request data from an API you defined.

## Notes:

- iOS SDK
	- The requester part was based on AFNetworking, but AFNetworking only support sending the NSDictionary as parameters, so I modified some code of it to support sending the serialized protobuf binary data.
- Android SDK
	- Based on AsyncHttp, because AsyncHttp didn't support cache, so currently didn't add the cache related feature.
- For the packer
	- There have some code to remove and add the "objc_class_prefix". Because there Google Protobuf 2 complier didn't support iOS prefix but in the Google Protobuf 3 support it.
	- Need to install both protobuf and protobuf@2.6 in brew. Because the .java files generated under the brew protobuf 3.x environment can't be integrated into protobuf 2.x projects, so there are some code do the link and unlink.
	- Now didn't support the "import" in .proto file so need to fix some build break in the generated files.
	
## Versions

Apr.2017

- Release the iOS framework


## About 
Email: silver6wings@gmail.com
By Junchao/silver6wings



