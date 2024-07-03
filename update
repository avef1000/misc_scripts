#!/bin/bash

# Define color codes
RED='\033[0;31m'
GREEN='\033[0;32m'
YELLOW='\033[1;33m'
BLUE='\033[0;34m'
NC='\033[0m' # No Color

echo -e "${BLUE}########################################################################${NC}"
echo -e "${GREEN}#                           System Upgrade${NC}"
echo -e "${GREEN}#                       Initramfs/Kernel Upgrade${NC}"
echo -e "${GREEN}#                         Bootloader Upgrade${NC}"
echo -e "${BLUE}#                       +++++++++++++++++++++++++${NC}"
echo -e "${YELLOW}#                  Script Written by Avraham Freeman${NC}"
echo -e "${BLUE}########################################################################${NC}"
sleep 3

# Function to display the menu and read choice
display_menu() {
    echo -e "${BLUE}======= Linux Upgrade Script ========${NC}"
    echo -e "${GREEN}1. Regular Upgrade${NC}"
    echo -e "${GREEN}2. Dist-Upgrade${NC}"
    echo -e "${GREEN}3. Full-Upgrade${NC}"
    echo -e "${GREEN}4. Install Metapackages (kali-tweaks)${NC}"
    echo -e "${GREEN}5. Exit${NC}"
    echo -e "${BLUE}=====================================${NC}"
    read -p "Enter your choice: " choice
    case $choice in
        1) regular_upgrade ;;
        2) dist_upgrade ;;
        3) full_upgrade ;;
        4) install_metapackages ;;
        5) exit 0 ;;
        *) echo -e "${RED}Invalid choice, please select a valid option${NC}"
           display_menu ;;
    esac
}

# Function to perform regular upgrade
regular_upgrade() {
    echo -e "${YELLOW}Starting system update${NC}"
    sleep 1
    echo -e "${YELLOW}Please grant root access for updates${NC}"
    sudo apt update
    echo -e "${GREEN}System is updated${NC}"
    sleep 1
    echo -e "${YELLOW}Initializing stage 2${NC}"
    sleep 1
    echo -e "${YELLOW}Upgrading and patching system${NC}"
    sudo apt upgrade -y
    echo -e "${GREEN}System upgraded successfully${NC}"
    sleep 1
    echo -e "${YELLOW}Upgrading kernel, please wait${NC}"
    sudo update-initramfs -u
    echo -e "${GREEN}Kernel updated successfully${NC}"
    sleep 1
    echo -e "${YELLOW}Initializing stage 3${NC}"
    echo ".    }"
    echo " .   }"
    echo "  .  }"
    echo "   . }"
    echo "    .}"
    echo -e "${YELLOW}Scanning GRUB bootloader${NC}"
    echo "3"
    sleep 1
    echo " 2"
    sleep 1
    echo "  1"
    sudo update-grub
    echo -e "${GREEN}Bootloader is upgraded and up to date${NC}"
    echo -e "${YELLOW}Script by Avraham Freeman, cashapp=blackwidow987${NC}"
}

# Function to perform dist-upgrade
dist_upgrade() {
    echo -e "${YELLOW}Starting system update${NC}"
    sleep 1
    echo -e "${YELLOW}Please grant root access for updates${NC}"
    sudo apt update
    echo -e "${GREEN}System is updated${NC}"
    sleep 1
    echo -e "${YELLOW}Initializing dist-upgrade${NC}"
    sudo apt dist-upgrade -y
    echo -e "${GREEN}System dist-upgraded successfully${NC}"
    sleep 1
    echo -e "${YELLOW}Upgrading kernel, please wait${NC}"
    sudo update-initramfs -u
    echo -e "${GREEN}Kernel updated successfully${NC}"
    sleep 1
    echo -e "${YELLOW}Scanning GRUB bootloader${NC}"
    sudo update-grub
    echo -e "${GREEN}Bootloader is upgraded and up to date${NC}"
    echo -e "${YELLOW}Script by Avraham Freeman, cashapp=blackwidow987${NC}"
}

# Function to perform full-upgrade
full_upgrade() {
    echo -e "${YELLOW}Starting system update${NC}"
    sleep 1
    echo -e "${YELLOW}Please grant root access for updates${NC}"
    sudo apt update
    echo -e "${GREEN}System is updated${NC}"
    sleep 1
    echo -e "${YELLOW}Initializing full-upgrade${NC}"
    sudo apt full-upgrade -y
    echo -e "${GREEN}System full-upgraded successfully${NC}"
    sleep 1
    echo -e "${YELLOW}Upgrading kernel, please wait${NC}"
    sudo update-initramfs -u
    echo -e "${GREEN}Kernel updated successfully${NC}"
    sleep 1
    echo -e "${YELLOW}Scanning GRUB bootloader${NC}"
    sudo update-grub
    echo -e "${GREEN}Bootloader is upgraded and up to date${NC}"
    echo -e "${YELLOW}Script by Avraham Freeman, cashapp=blackwidow987${NC}"
}

# Function to install metapackages using kali-tweaks
install_metapackages() {
    echo -e "${YELLOW}Please grant root access for installing metapackages${NC}"
    sudo kali-tweaks
    echo -e "${GREEN}Metapackages installed successfully${NC}"
}

# Main execution starts here
display_menu
             
