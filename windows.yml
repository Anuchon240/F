volumes:
  windows_main_data:
  windows_extra_data:

services:
  windows:
    image: dockurr/windows
    container_name: windows
    environment:
      VERSION: "xp"
      USERNAME: "User"
      PASSWORD: "user@123"
      RAM_SIZE: "4G"
      CPU_CORES: "2"
      DISK_SIZE: "32G"
      DISK2_SIZE: "2G"
    devices:
      - /dev/kvm
      - /dev/net/tun
    cap_add:
      - NET_ADMIN
    ports:
      - "8006:8006"
      - "3389:3389/tcp"
      - "3389:3389/udp"
    volumes:
      - windows_main_data:/data
      - windows_extra_data:/extra
    stop_grace_period: 2m
