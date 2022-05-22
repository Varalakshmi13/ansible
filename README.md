# ansible

Ansible configuration file :  https://raw.githubusercontent.com/ansible/ansible/stable-2.11/examples/ansible.cfg

## Inventory 
Inventory is text file, Then entries in the inventory can be an IP address or DNS Name. 


# 
XML 

<courseName>DevOps</courseName>
<trainerName>Raghu K</trainerName>
<trainees>
    abc@gmail.com,
    xyz@gmail.com
</trainees>
<timing>
    <morning>6AM</morning>
    <evening>10PM</evening>
</timings>

JSON 

{
 "courseName": "DevOps",
 "trainerName": "RaghuK",
 "trainees": [
    "abc@gmail.com",
    "xyz@gmail.com"
  ],
 "timing": {
    "morning": "6AM",
    "evening": "10PM"
 }

}

YAML
courseName: DevOps
trainerName: RaghuK
trainees:
  - abc@gmail.com
  - xyz@gmail.com 
timing:
  morning: 6AM 
  evening: 10PM 


### 
MARKUP Languages will have data as 
KEY - VALUE (Regular key value)
KEY - MULTIPLE VALUES (List) (ex: trainees)
KEY - KEY - VALUE (MAP, DICT) (ex: timing)
