#!/usr/bin/env bash

# How to clone 50 repositories at once?

check_answer() {
  while [[ "$choice" != "YES" && "$choice" !=  "NO" ]]; do
    echo "That was not one of your choices. Please choose YES or NO."
    read -r choice
  done
}

echo "Enter the URL of the repository you want to clone: "
read -r url

repository=$(echo $(echo $url|cut -d '/' -f5)|cut -d '.' -f1)

if [ -e ~/$repository ]; then
  echo "The repository already exists. Do you want to pull the repository? YES or NO"
  read -r choice
  # Call the function
  check_answer
  if [[ "$choice" == "YES" ]]; then
          echo "You chose to pull the repository."
          cd
          cd $repository
          git pull $url
  else
          echo "You chose to NOT pull the repository. See you later!"
  fi
else
  echo "The repository doesn't exist. Do you want to clone the repository? YES or NO"
  read -r choice
  # Call the function
  check_answer
  if [[ "$choice" == "YES" ]]; then
          echo "You chose to clone the repository."
          cd
          git clone $url
  else
          echo "You chose to NOT clone the repository. See you later!"
  fi
fi
