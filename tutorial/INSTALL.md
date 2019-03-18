### Local install
    git clone -b euc git@github.com:hawk/lux.git
    export ERL_COMPILER_OPTIONS='[debug_info]'
    cd lux
    autoconf
    ./configure
    make

### Add lux to the path
    export "PATH=$PWD/bin:$PATH"

### Run tests
    make
