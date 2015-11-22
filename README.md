# CCV on Docker

This is [libccv]'s HTTP API ([docs]), containerised.

The image is split in two to accommodate Docker Hub's build process — it does
not seem to like really long build processes, so instead we first install all
necessary packages, then build from sources. Yes, it means we waste some space
as there are packages we could probably delete, but given CCV's size this is
not actually worth it.

The final image is about 1G on disk and a bit less than 600MB transfer. When
started, it takes a bit more than a gigabyte of RAM... idle. Computer Vision
is heavy business.

The port is 3350, as indicated by the Dockerfile.

