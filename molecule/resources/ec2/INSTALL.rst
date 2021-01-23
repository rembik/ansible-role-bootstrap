*******
Amazon Web Services driver installation guide
*******

Requirements
============

* AWS CLI
* Genaral python dependencies
* General molecule dependencies (see https://molecule.readthedocs.io/en/latest/installation.html)
* AWS credentials and region (see https://docs.aws.amazon.com/en_us/cli/latest/userguide/cli-configure-files.html)

Install
=======

.. code-block:: bash

    $ sudo pip install boto boto3
    $ sudo pip install --upgrade awscli
    $ sudo pip install molecule-ec2
    $ export AWS_REGION="eu-central-1"
