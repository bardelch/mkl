FROM ubuntu

#https://serverfault.com/questions/949991/how-to-install-tzdata-on-a-ubuntu-docker-image
ENV DEBIAN_FRONTEND="noninteractive" TZ="America/Detroit"

RUN apt-get update && \
	apt-get upgrade -y && \
	apt-get install -y \
		apt-transport-https \
		ca-certificates \
		build-essential \
		vim \
		cmake \
		valgrind \
		gfortran \
		wget

# https://software.intel.com/content/www/us/en/develop/articles/installing-intel-free-libs-and-python-apt-repo.html
RUN cd /root && \
	wget https://apt.repos.intel.com/intel-gpg-keys/GPG-PUB-KEY-INTEL-SW-PRODUCTS-2019.PUB && \
	apt-key add GPG-PUB-KEY-INTEL-SW-PRODUCTS-2019.PUB 
RUN wget https://apt.repos.intel.com/setup/intelproducts.list -O /etc/apt/sources.list.d/intelproducts.list && \
	apt-get update
RUN apt-get install -y \
	intel-mkl-full \
	intel-mkl-doc \
	intel-ipp-2020.3-912 \
	intel-tbb-2020.3-912 \
	intel-daal-2020.3-912 \
	intel-mpi-2019.9-912
