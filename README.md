# tf-project
Terraform Project Starter

## Summary
Open Source Terraform Project Boilerplate handcrafted by the Practitioners at Gadgetry.io

* Company: Gadgetry, LLC
* Web: http://gadgetry.io

## Getting Started



## Project Structure

    /project                         # Terraform Project

        /files                       # Project Files, Scripts, etc 
            functions.sh             # Wrapper Functions
            ...

        /modules                     # Locally Sourced Modules (Organized by Provider)
            /aws                     # Examples include aws, chef, github, rancher, etc.
            /chef
            /github
            /rancher
            ...
            
        /workspaces                  # Workspaces (Organized by Environment)
            /ops                     # Operations Environment
                /app_hubot           # Stacks implement Modules/Resources per Workspace
                /app_jenkins
                /app_sonar
                /ecs_cluster
                /network             
                /openvpn             
                /security
                ...    
            /dev                     # Development Environment
                /app_stack1          # Stacks can/will differ across Workspaces
                /app_stack2          #
                /app_stack3          # This modular approach will help provide flexibility
                /app_stack4          # while improving your ability to manage drift across
                /network             # workspaces and module versions
                /network_peering
                ...

            /tst                     # Testing Environment

            /stg                     # Staging Environment

            /prd                     # Production Environment
        
        terraform.sh                 # Terraform Wrapper (Consistent Workflow)

