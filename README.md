# VLAN Basic Configuration

This project demonstrates the basic configuration of VLANs (Virtual Local Area Networks) using Cisco Packet Tracer. VLANs are used to segment a network into different broadcast domains, which can improve network performance and security.

## Project Overview

In this project, we configure VLANs on a switch to separate network traffic for different departments within an organization. The VLANs configured in this project are:

- VLAN 10: IT
- VLAN 20: HR
- VLAN 30: Finance

## Network Topology

The network topology consists of:

- One switch
- Three PCs, each connected to the switch

Each PC is assigned to a different VLAN.

## Configuration Steps

### 1. Assign VLANs to Ports

First, we need to create each VLAN on the switch.

```bash
Switch> enable
Switch# configure terminal
Switch(config)# vlan 10
Switch(config-vlan)# name IT
Switch(config-vlan)# exit
Switch(config)# vlan 20
Switch(config-vlan)# name HR
Switch(config-vlan)# exit
Switch(config)# vlan 30
Switch(config-vlan)# name Finance
Switch(config-vlan)# exit

Assign Ports to VLANs

Switch(config)# interface fastethernet 0/1
Switch(config-if)# switchport mode access
Switch(config-if)# switchport access vlan 10
Switch(config-if)# exit
Switch(config)# interface fastethernet 0/2
Switch(config-if)# switchport mode access
Switch(config-if)# switchport access vlan 20
Switch(config-if)# exit
Switch(config)# interface fastethernet 0/3
Switch(config-if)# switchport mode access
Switch(config-if)# switchport access vlan 30
Switch(config-if)# exit

Verify VLAN Configuration

Switch# show vlan brief

