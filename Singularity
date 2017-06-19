bootstrap:docker
From:ubuntu:xenial

%post

apt-get update && apt-get install -y --no-install-recommends \
        build-essential \
        curl \
        libfreetype6-dev \
        libpng12-dev \
        libzmq3-dev \
        module-init-tools \
        openjdk-8-jdk \
        pkg-config \
        python \
        python-dev \
        python-numpy \
        rsync \
        unzip \
        vim \
        wget \

apt-get clean 
rm -rf /var/lib/apt/lists/*

# use CA certs from CVMFS
mkdir -p /etc/grid-security
ln -f -s /cvmfs/oasis.opensciencegrid.org/mis/certificates /etc/grid-security/certificates

# required directories
mkdir -p /cvmfs

# build info
echo "Timestamp:" `date --utc` | tee /image-build-info.txt


