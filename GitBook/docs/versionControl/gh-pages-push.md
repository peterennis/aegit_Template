# Pushing Gitbook to VSTS repository gh-pages branch

- In [Hosting Gitbook on Github Pages](/documentation/host-gitbook-on-github.md) there is a guide on pushing a subfolder onto gh-pages branch in github repostory.

- We do this because when we build the local gitbook, the static website is built in _book subfolder, which we want to push to gh-pages branch to be hosted on github pages.

- We do this by creating a script in package.json:

    `"docs:publish": "npm run docs:build && cd _book && git init && git commit --allow-empty -m \" Update docs\" && git checkout -b gh-pages && git add . && git commit -am \" Update docs\" && git push git@github.com:<username>/<repo> gh-pages --force"`

    which consists of these commands:

    ```
    $ npm run docs:build
    $ cd _book
    $ git init
    $ git commit --allow-empty -m "Update docs"
    $ git checkout -b gh-pages
    $ git add .
    $ git commit -am "Update docs"
    $ git push git@github.com:<username>/<repo> gh-pages --force
    ```

### To do the same for our VSTS repo, we simply add a docs:publishVSTS command with SSH directing to the gh-pages branch in VSTS

- First add local ssh key to the appropriate VSTS repostory

    > Your ssh key can be accessed in `C:\Users\<username>\.ssh\id_rsa`

    ![](./img/ssh-key.png)

- Add your ssh key to VSTS

    > 1. ![](./img/security.png)
    > 2. ![](./img/ssh-keys.png)


- Replace ssh address in docs:publish command with ssh address of VSTS

    The VSTS ssh address can be optained in clone repo option:
    ![](./img/ssh-address.png)

- My final command looks like this:

    `"docs:publishVSTS": "npm run docs:build && cd _book && git init && git commit --allow-empty -m \" Update docs\" && git checkout -b gh-pages && git add . && git commit -am \" Update docs\" && git push rdadev@vs-ssh.visualstudio.com:22/_ssh/DFAQ gh-pages --force"`