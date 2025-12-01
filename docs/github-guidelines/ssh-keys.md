---
sidebar_position: 9
---

# SSH Keys

SSH Keys are used by Github as an additional layer of security for any interactions that you make with Github repositories.

While repositories can be accessed using just https; it is recommended that all interactions with a Github repository from cloning and pushing be done over SSH both for the security of projects and as practice since in most industries this is a standard for interacting with remote repositories

## Checking for exisiting SSH keys

If you have already made a SSH key in the past follow one of the links below to find it on your machine based on the OS you are using:

- Mac: [Github Docs For Checking Existing SSH Keys (Mac)](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/checking-for-existing-ssh-keys?platform=mac)
- Windows: [Github Docs For Checking Existing SSH Keys (Windows)](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/checking-for-existing-ssh-keys?platform=windows)
- Linux: [Github Docs For Checking Existing SSH Keys (Linux)](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/checking-for-existing-ssh-keys?platform=linux)

## Creating a new SSH key

If you do not already have a SSH key made then follow one of the links below on how to best create a new SSH key for interacting with Github based on the OS you are using:

- Mac: [Github Docs For Creating SSH Keys (Mac)](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent?platform=mac)
- Windows: [Github Docs For Creating SSH Keys (Windows)](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent?platform=windows)
- Linux: [Github Docs For Creating SSH Keys (Linux)](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent?platform=linux)

## Adding a new SSH key to Github

Once you have access to a SSH key owned by you then you can follow one of the links below on how to add it to your github account based on the OS you are using:

- Mac: [Github Docs For Adding SSH Keys (Mac)](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account?platform=mac)
- Windows: [Github Docs For Adding SSH Keys (Windows)](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account?platform=windows)
- Linux: [Github Docs For Adding SSH Keys (Linux)](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account?platform=linux)

## Using the key

After you have added a SSH key to Github you are able to clone repositories over SSH rather than HTTPS and interact with the Github repository by using your SSH when doing actions such as fetching, pulling, and pushing
- NOTE: When doing any of these actions Git will ask for the passphrase of the key you created to confirm that you are the correct owner of the key so make sure to remember the passphrase well!