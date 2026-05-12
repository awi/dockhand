




# On the PVE host
## nd install the necessary QEMU and binfmt support packages
sudo apt-get update
sudo apt-get install -y qemu-user-static binfmt-support

# Restart the service to ensure registration is active
sudo systemctl restart binfmt-support
#Verify on host
cat /proc/sys/fs/binfmt_misc/qemu-aarch64



How to prepare for buildung an image

sudo apt-get update && sudo apt-get install -y qemu-user-static binfmt-support

docker run --privileged --rm tonistiigi/binfmt --install all

# Create and activate a new builder
docker buildx create --name mybuilder --use --bootstrap


