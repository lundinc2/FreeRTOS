FROM ubuntu:20.10
MAINTAINER Carl Lundin

RUN apt-get update && apt-get install -y \
	build-essential \
	libpcap-dev	\
    python3-pip \
    && pip3 install scons
COPY FreeRTOS /FreeRTOS/
COPY FreeRTOS-Plus /FreeRTOS-Plus/
WORKDIR /FreeRTOS/Demo/Posix_GCC/
RUN scons
CMD ["./build/posix_demo"]
