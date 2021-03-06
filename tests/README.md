# Ansible Role tests

Tests in this role are based on Jeff Geerling's fantastic work. See the following page for more information:

https://www.jeffgeerling.com/blog/2018/how-i-test-ansible-configuration-on-7-different-oses-docker


To run the test playbook(s) in this directory:

  1. Install and start Docker.
  2. Download the test shim (see .travis.yml file for the URL) into `tests/test.sh`:
    - `wget -O tests/test.sh https://gist.githubusercontent.com/geerlingguy/73ef1e5ee45d8694570f334be385e181/raw/`
  3. Make the test shim executable: `chmod +x tests/test.sh`.
  4. Run (from the role root directory) `distro=[distro] playbook=[playbook] ./tests/test.sh`

If you don't want the container to be automatically deleted after the test playbook is run, add the following 
environment variables: `cleanup=false container_id=$(date +%s)`

eg. `sudo distro=ubuntu1804 playbook=test.yml cleanup=false container_id=$(date +%s) ./tests/test.sh`
