
## Mezzanine configured for fabric deployment to AWS EC2 

AMI ID: `ubuntu-trusty-14.04-amd64-server-20140416.1 (ami-6ac2a85a)`

### Setup:

    mkdir mezzanine-base
    cd mezzanine-base

    virtualenv env
    . env/bin/activate
    pip install fabric 

    git clone https://github.com/orInge/mezzanine-base.git project
    cd project
    pip install -r requirements.txt

    # settings.py
    # change ALLOWED_HOSTS[0] to your ec2 instance public DNS
    # example:
    ALLOWED_HOSTS=['ec2-XX-XXX-XXX-XX.us-west-2.compute.amazonaws.com']

    # change TIME_ZONE

    # FABRIC settings:
    # change SSH_KEY_PATH to point to your key
    # example: 
    "SSH_KEY_PATH": "~/.ec2/my-key-pair.pem",


### Deploy to EC2:

    fab all

### Create DB

    python manage.py createdb
