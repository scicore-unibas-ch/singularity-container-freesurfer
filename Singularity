Bootstrap: docker
From: centos:7

%post

    # bring up to date
    yum -y update

    # install the dependencies
    yum -y install epel-release
    yum install -y \
    bc \
    git \
    wget \
    tcsh \
    libblas \
    liblapack \
    zlib1g \
    libxmu \
    libxi \
    libxt \
    libx11 \
    libglu1-mesa

    # Uncompress FreeSurfer tarball to /usr/local/
    wget -c https://surfer.nmr.mgh.harvard.edu/pub/dist/freesurfer/6.0.0/freesurfer-Linux-centos6_x86_64-stable-pub-v6.0.0.tar.gz -O - | \
    tar -xz -C /usr/local/

%environment
    export FREESURFER_HOME=/usr/local/freesurfer
    source $FREESURFER_HOME/SetUpFreeSurfer.sh
