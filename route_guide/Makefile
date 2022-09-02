protoc:
	protoc --proto_path=routeguide routeguide/*.proto --go_out=plugins=grpc:routeguide

init:
	go mod init grpcbasic
	go mod tidy

clean:
	rm go.sum go.mod routeguide/route_guide.pb.go