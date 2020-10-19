# mlOps-demo
Data versioning using DVC
  - git is initiated using git init
  - dvc tracking is initiated using dvc init
  - the necessary codes are added (get_data.py, analyze.py)
  - get_data creates a csv dataset file
  - the remote location for storing our files is created using the command dvc remote add -d <remote_folder_name> gdrive://<last_part_of_gdrive_folder_link> refer [this](https://dvc.org/doc/command-reference/remote) for more details
  - dataset is added to dvc (which stores the data in remote(or local) location, here gdrive is used) using dvc add <data_path>
  - follow the instructions given after execution of previous command, the commands to be executed are git add <the_names_of_file_given_by_the dvc_last_command_output>
  - next command is dvc push which pushes the snapshot of the current data to the remote location(authorization is required for the first time)
  - this puts up the first version of your data and the code to the dvc and the git respectively
  - if further changes are made in the data then that particular change can be again pushed into the remote storage
  - git keeps a track of which version of the code works with which version of the dataset, and the dvc keeps a track of all the datasets which can be reproduced as and when required.
