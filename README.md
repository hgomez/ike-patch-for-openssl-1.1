# ike-patch-for-openssl-1.1
Patches so Ike is OpenSSL 1.1+ compatible

## How to use it ?

    # Get latest sources
    wget https://www.shrew.net/download/ike/ike-2.2.1-release.tbz2
    tar xvzjf ike-2.2.1-release.tbz2
    
    # Patch
    cd ike
    patch -p1 <PATH/TO/ike.patch
    
    # Make
    cmake -DCMAKE_INSTALL_PREFIX=/usr -DQTGUI=NO -DETCDIR=/etc -DNATT=YES
    make
    
    # Install
    sudo make install
