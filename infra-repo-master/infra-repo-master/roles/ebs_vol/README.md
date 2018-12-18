Responsible for attaching ebs volume attachment.

## Procedure :

  Create a YAML file in task directory under the name host.

## Example :

  Create a block per volume like below -


    - ec2_vol:
      instance: <instance id>
      id: <volume id>
      device_name: </dev/sd[f-z]
      delete_on_termination: no

 N.B: device_name should be uniq per block

## Version: 

  4-dec-2018   : 0.1
