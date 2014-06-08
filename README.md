** this is a work in progress **

mezzanine base configured for fabric deployment to aws ec2

ami id: `ubuntu-trusty-14.04-amd64-server-20140416.1 (ami-6ac2a85a)`

### Usage:

    mkdir mezzanine-base
    cd mezzanine-base
    virtualenv env
    . env/bin/activate
    git clone https://github.com/orInge/mezzanine-base.git project
    cd project
    pip install fabric
    pip install -r requirements.txt

    # change settings for your setup
    ...todo

    fab all
