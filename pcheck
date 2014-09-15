#!/bin/sh

. ./pcheck.conf
. ./pcheck_data
. ./pcheck_functions


PROGRAM=$(basename $0)
VERSION=0.5



# Checks if any command line arguments issued...

if [ $# -gt 0 ]; then

  case "$1" in
  
    -d|--details) current_values_summary ;;
    
    she|hda|laptop_mode|pcie|sata|device_pm|cpu|usb|wifi) report_named_component "$1" ;;
  
    -h|--help) usage ;;
    
    -c|--components) list_components ;;
  
     *) usage ;;
     
  esac
  
# ...otherwise report power status

else
  report_power_status
fi

