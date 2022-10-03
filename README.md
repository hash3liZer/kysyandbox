# KYPO Cyber Range Platform Demo Training

A demo to demonstrate the training capabilities of the KYPO Cyber Range Platform.

## Requirements

* Openstack project with default images
* KYPO instance running in the Openstack project
* Account for the KYPO instance with privileges to create and run trainings and sandboxes
* SSH access to the kypo-proxy-jump

## Usage

1. In web browser, on the site for your KYPO instance, go to Sandboxes > Definition and Create a new definition with URL of: this repository > Clone > Clone with SSH and Revision: this repository > last commit SHA
2. In Sandboxes > Pool Create a new pool with the Sandbox Definition (telnet-server-sandbox)
3. Allocate the sandbox (a button in Actions in Pool Overview) and wait until each Allocation Request Stages finishes (click Pool Title and then Allocation Request to see the progress)
4. In Trainings > Definition upload the [training.json](./training.json)
5. In Trainings > Instance create and continue editing a new instance (pick duration of the training, access token prefix and select the Training Definition from step 4.)
6. Assign the pool from step 3. to the training instance
7. Copy the Access Token from the training instance (visible in Training Instance Overview) and use it in Trainings > Run
8. Follow instructions in the run

