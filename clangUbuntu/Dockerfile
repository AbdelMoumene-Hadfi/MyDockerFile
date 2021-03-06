FROM ubuntu:20.04
RUN apt-get update && apt-get install -y xz-utils curl && rm -rf /var/lib/apt/lists/*
RUN curl -SL https://github.com/llvm/llvm-project/releases/download/llvmorg-11.0.0/clang+llvm-11.0.0-x86_64-linux-gnu-ubuntu-20.04.tar.xz | tar -xJC . && \
mv clang+llvm-11.0.0-x86_64-linux-gnu-ubuntu-20.04 clang_11 && echo export PATH=/clang_11/bin:$PATH >> ~/.bashrc && echo export LD_LIBRARY_PATH=/clang_11/lib:$LD_LIBRARY_PATH >> ~/.bashrc

CMD [ “/bin/bash” ]
