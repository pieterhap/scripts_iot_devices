#!/usr/bin/env bash

check_answer() {
  while [[ "$choice" != "YES" && "$choice" !=  "NO" ]]; do
    echo "That was not one of your choices. Please choose YES or NO."
    read -r choice
  done
}

echo "Enter absolute path of the directory you want to copy (use pwd):"
read -r directory

if [ -e $directory ]; then
  echo "Do you want to copy the directory to a remote host? YES or NO"
  read -r choice
  check_answer

  if [[ "$choice" == "YES" ]]; then
    echo "Enter the username of the remote host:"
    read remote_host
    echo "Enter IP Address of the remote host:"
    read ip_remote_host
    echo "Enter absolute path of the destination you want to copy the directory to on the remote host:"
    read destination_remote_host
    echo "Copying the directory to its destination."
    scp -r $directory $remote_host@$ip_remote_host:$destination_remote_host
  else
    echo "Enter absolute path of the destination you want to copy the directory to on the local host:"
    read destination_local_host
    echo "Copying the directory to its destination."
    cp -r $directory $destination_local_host
  fi
else
  echo "This directory does NOT exist."
fi

# scp [[user1@]host1:]<source> [[user2@]host2:]<destination>
