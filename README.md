
- [Adding a new SSH key to your GitHub Account](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account)

- [SSH key generation and addition to agent](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)

# Generate key

- Go to your GitHub / user settings / Developer Settings / Personal access tokens / Tokens (classic)

- Click "Generate new token"

- Generate new token (classic)

- Enter a note, duration, and check following scopes :

 [✅] repo, [✅] write:packages, [✅] write:discussion

- Copy and paste your personal access token somewhere safe

``` console
 $ cd ~/Desktop

 $ ssh-keygen -t ed25519 -C "your_email@example.com"

 $ pbcopy < ~/.ssh/id_ed25519.pub

 $ ls -a    

 $ ls .ssh  

 $ ls id_ed25519.pub

 $ git clone git@github.com:scientist-softserv/softserv-website.git
```
