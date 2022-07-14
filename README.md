# Install gdal

## Install the latest Python and setup a new Python virtualenv

```bash
pkcon install -y git
pkcon install -y python3
pkcon install -y python3-pip
pkcon install -y python3-virtualenv
virtualenv-3 ~/python
source ~/python/bin/activate
echo "source ~/python/bin/activate" | tee -a ~/.bashrc
```

## Install the latest Ansible

```bash
pip install setuptools_rust wheel
pip install --upgrade pip
pip install ansible
```

## Install the gdal ansible role

### Create a directory for the ansible role. 

```bash
install -d ~/.ansible/roles/computate.computate_gdal
```

### Clone the gdal ansible role. 

```bash
git clone git@github.com:computate-org/computate_gdal.git ~/.ansible/roles/computate.computate_gdal
```

## Run the gdal ansible playbook to install the application locally. 

```bash
cd ~/.ansible/roles/computate.computate_gdal
ansible-playbook install.yml
```

