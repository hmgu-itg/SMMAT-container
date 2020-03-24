Bootstrap:docker
From:ubuntu:latest

%setup
	apt update
	apt install -y libbz2-dev liblzma-dev libcurl4-openssl-dev
	wget https://github.com/samtools/htslib/releases/download/1.10.2/htslib-1.10.2.tar.bz2
	tar -xvjf htslib-1.10.2.tar.bz2 && cd htslib-1.10.2 && ./configure && make && make install
	wget https://github.com/samtools/bcftools/releases/download/1.10.2/bcftools-1.10.2.tar.bz2
	tar -xvjf bcftools-1.10.2.tar.bz2 && cd bcftools-1.10.2 && ./configure && make && make install
	cp /home/agilly/containers/sing-smmat/step1 $SINGULARITY_ROOTFS/usr/bin
