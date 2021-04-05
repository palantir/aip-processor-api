AIP Processor API
=================
AI Inference Platform (AIP) consumes real-time media streams and executes AI-based 
worker-services (called _processors_) to enrich the media streams before propagating
the media streams onwards to other consumers. This repository holds an open, 
[protobuf](https://developers.google.com/protocol-buffers) and [gRPC](https://grpc.io/) 
based API definition that processors implement to receive and reply with enrichments.

Compatible processors implement two gRPC services:
1. [configuration service](/aip-processor-api/src/main/proto/configuration-service.proto): 
   processors identify the kind and version of enrichment they perform
2. processor service ([v1](/aip-processor-api/src/main/proto/processing-service-v1.proto) and 
   [v2](/aip-processor-api/src/main/proto/processing-service-v2.proto)): versioned processor 
   implementations for receiving media frames and metadata and returning enrichments, such 
   as AI inferences, georegistration, or computing tracks from prior inferences

Questions and Feedback
----------------------
Please contact us at aip-questions@palantir.com with any questions or feedback.

License
-------
This repository is licensed under the Apache 2.0 License (https://www.apache.org/licenses/LICENSE-2.0).

