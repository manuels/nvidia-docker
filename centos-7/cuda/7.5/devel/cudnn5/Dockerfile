FROM cuda:7.5-devel

ENV CUDNN_VERSION 5
LABEL com.nvidia.cudnn.version="5"

ENV CUDNN_DOWNLOAD_SUM c4739a00608c3b66a004a74fc8e721848f9112c5cb15f730c1be4964b3a23b3a

RUN curl -fsSL http://developer.download.nvidia.com/compute/redist/cudnn/v5/cudnn-7.5-linux-x64-v5.0-ga.tgz -O && \
    echo "$CUDNN_DOWNLOAD_SUM  cudnn-7.5-linux-x64-v5.0-ga.tgz" | sha256sum -c --strict - && \
    tar -xzf cudnn-7.5-linux-x64-v5.0-ga.tgz -C /usr/local && \
    rm cudnn-7.5-linux-x64-v5.0-ga.tgz && \
    ldconfig
