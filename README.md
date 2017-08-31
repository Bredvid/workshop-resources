# Workshop i Google Cloud Engine

For å få en konto til å logge seg inn, 
```bash
ssh bredvid@bastion.bredvid.io
```

Du vil få to nøkler du må lagre i to filer. id_rsa og id_rsa_pub, sammen med et brukernavn

Bruk dette for å logge deg på -

```bash
ssh -i ./id_rsa brukernavn@bastion.bredvid.io
```

---

## Creating an instance
[https://cloud.google.com/sdk/gcloud/reference/compute/instances/create]

bruk følgende config: 
navnet må være unikt. for enkelhetsskyld bruk brukernavnet ditt. 
zone: "us-east1-b" 
machine-type: "f1-micro"
network: "default" 
tags: "workshop
image-project: ubuntu-os-cloud
image-family: "ubuntu-1704"
Om dere liker enannen distro enn ubuntu, kan dere velge en annen fra: [https://cloud.google.com/compute/docs/images]

## connecting to an instance: 

[https://cloud.google.com/sdk/gcloud/reference/compute/ssh]]


For tilgang via ssh ut av boksen kan dere settee: 
metadata: '{"sshKeys":"workshop:{din public nøkkel fra id_rsa.pub} workshop"}'

Du kan da logge på med ssh workshop@navnpåboks


##Deleting an instanceBruk
[https://cloud.google.com/sdk/gcloud/reference/compute/instances/delete]



#Ansible 
Getting started: 
[http://docs.ansible.com/ansible/latest/intro_getting_started.html]

Alle moduler:
[http://docs.ansible.com/ansible/latest/list_of_all_modules.html]

## Nyttige moduler
lag instanser i gce: [http://docs.ansible.com/ansible/latest/gce_module.html]
opprett filer og kataloger: [http://docs.ansible.com/ansible/latest/file_module.html]
legg til i filer: [http://docs.ansible.com/ansible/latest/lineinfile_module.html]
bruk en template for å kopiere ut en fil [http://docs.ansible.com/ansible/latest/template_module.html]
kopiere ut en fil [http://docs.ansible.com/ansible/latest/copy_module.html]
legge til pakker  [http://docs.ansible.com/ansible/latest/apt_module.html]

## Info om ansible

Intro til inventory: http://docs.ansible.com/ansible/latest/intro_inventory.html


