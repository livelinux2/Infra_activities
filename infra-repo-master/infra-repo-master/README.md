This repository contains ansible playbooks, roles and cloudformation templates for the infrastructure Edifixio maintains

## Repository Structure

This repo follows below repo structure-

> * root folders contains server playbooks like <hostname>.yml.
> *  server playbooks includes roles to implement changes.
> * playbook, roles contains only infrastructural configs and not any applicative data.

## Guideline for updating repository

>
>  * Don't create separate directory structure e.g. NWR-PROD
>  * Instead put your roles inside the role directory and use/improve other peoples roles.
>  * roles you write must be generic so that it can be reused for other clients or hosts.
>  * One role should only serve one objective. e.g. don't put apache installation and php within same role, instead create two roles with names like php7 and apache. Push apache part in apache role and php7 part on  php7 role.
>  * Root directory should only contains yml files named after the server. e.g. edfxadmx115.yml this <hostname>.yml file should have same generic structure so that it would help in readability.
>  * When you are about to write some role look up ansible galaxy or Edifixio Git Repos. If something is already written and it contains GPL/MIT license then you can download, modify, test and push it to git.
>  * Please write README.md for each role with contents like Author, Source, Usage and example. It would help others to use your role for their activity.
>  * Repo should not contains and Sensitive information like private keys, passwords etc. It should be served via ansible vaults

## How to invoke the playbook -

> Download the repo from the git. Create a host playbook and include required roles. Update the inventory, hosts file. and execute the command like below -

    ansible-playbook edfxeuw1aadmx04.yml -i inventory/hosts

## To check syntax

   ansible-playbook edfxeuw1aadmx04.yml -i inventory/hosts --syntax-check

## To invoke commands in verbose mode -

    ansible-playbook edfxeuw1aadmx04.yml -i inventory/hosts -vvv
