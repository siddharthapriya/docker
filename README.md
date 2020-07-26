# docker
Code for running multiple docker images together

Here I will show how one can run instances of Drupal, MOODLE & Opencart simultaneously and then use them for development.

For this purpose ensure that the docker-compose files are transferred into three different directories. The reason behind this is that when one runs the command docker-compose up -d a bridge network is created separately for each of the programs and each can be independently accessed using the bridge IP address created by the program. I copied the three docker-compose.yml files into drupal, moodle, opencart directories respectively.

One can copy the below mentioned code (applicable for running on Ubuntu 20.04) to three separate files named docker-compose.yml files using simple text editor. The reason behind is that the default command docker-compose up -d assumes that it is being invoked to execute contents of docker-compose.yml file. it is possible to run yml files with other names also using (if the file name is test_drupal.yml) docker-compose -f test_drupal.yml up -d . 
