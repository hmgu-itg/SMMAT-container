Bootstrap:docker
From:ubuntu:latest

%setup
	wget -O $SINGULARITY_ROOTFS/usr/bin/step1 "https://raw.githubusercontent.com/hmgu-itg/SMMAT-container/master/step1" && chmod +x $SINGULARITY_ROOTFS/usr/bin/step1

%post
        apt update
        apt install -y libbz2-dev liblzma-dev libcurl4-openssl-dev wget gcc zlib1g-dev build-essential
        wget https://github.com/samtools/htslib/releases/download/1.10.2/htslib-1.10.2.tar.bz2
        tar -xvjf htslib-1.10.2.tar.bz2 && cd htslib-1.10.2 && ./configure && make && make install
        wget https://github.com/samtools/bcftools/releases/download/1.10.2/bcftools-1.10.2.tar.bz2
        tar -xvjf bcftools-1.10.2.tar.bz2 && cd bcftools-1.10.2 && ./configure && make && make install

