# ike-patch-for-openssl-1.1

OpenSSL 1.1 make many internal structures opaques and Ike required some updates [OpenSSL 1.1 backward compatibility guide](https://wiki.openssl.org/index.php/OpenSSL_1.1.0_Changes#Backward_compatibility)

## How to use it ?

    # Get latest sources
    wget https://www.shrew.net/download/ike/ike-2.2.1-release.tbz2
    tar xvjf ike-2.2.1-release.tbz2
    
    # Patch
    cd ike
    patch -p1 <PATH/TO/ike.patch
    
    # Make
    cmake -DCMAKE_INSTALL_PREFIX=/usr -DQTGUI=NO -DETCDIR=/etc -DNATT=YES
    make
    
    # Install
    sudo make install
