# Not too sure about the title, but a few interesting notes below

# Generating an SSH key and adding it to the SSH agent in order to ...

## Generate key

- Go to your GitHub / user settings / Developer Settings / Personal access tokens / Tokens (classic)

- Click "Generate new token"

- Generate new token (classic)

- Enter a note, duration, and check following scopes :

 [✅] repo, [✅] write:packages, [✅] write:discussion

- Copy and paste your personal access token somewhere safe


``` console
 $ cd ~/Desktop

 $ ssh-keygen -t ed25519 -C "your_email@example.com"

 // Remember to change the e-mail to your GitHub associated e-mail address

 $ > Enter a file in which to save the key (/Users/YOU/.ssh/id_ALGORITHM: [Press enter]

 // When this shows up press enter

 $ > Enter passphrase (empty for no passphrase): [Type a passphrase]
 $ > Enter same passphrase again: [Type passphrase again]

 // When this shows up also press enter, you can leave it blank

 // When the key fingerprint, your e-mail, and the key randomart image show up, copy paste it somewhere safe

 $ pbcopy < ~/.ssh/id_ed25519.pub

 $ ls -a    

 $ ls .ssh  

 $ ls id_ed25519.pub

 $ code .ssh

 // With VS code open,
 // navigate to the .pub key file
 // copy and paste contents somewhere safe
 
```

## Adding SSH key to SSH agent

- Navigate to Your GitHub profile settings / SSH and GPG keys (it's on the left)
- Click New SSH key
- Give it a title
- Key type: Authentication Key
- Copy and paste your keyfingerprint,  e-mail, and key randomart image into 'Key'
- Click 'Add SSH Key'
- If it asks you to reply "yes", "no", or "fingerprint", say "yes"

## Clone  Repo

- Navigate to SoftServ [GitHub Repo](https://github.com/scientist-softserv/softserv-website)

- Click code, select SSH, click copy link

``` console
 $ git clone git@github.com:scientist-softserv/softserv-website.git

 // When prompted, say "yes"

 $ cd softserv-website
```

## Possibly helpful links

- [Adding a new SSH key to your GitHub Account](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account)

- [SSH key generation and addition to SSH agent](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)
