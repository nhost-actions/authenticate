# install-nhost-cli

Github action to authenticate with the Nhost cloud.

## Usage

You can use this action after installing the CLI to authenticate with Nhost Cloud platform:


```yaml
    - name: Install Nhost CLI
      id: install-nhost-cli
      uses: nhost-actions/install-nhost-cli@v1

    - name: Authenticate with Nhost
      uses: nhost-actions/authenticate@v1
      with:
        pat: ${{ secrets.NHOST_PAT }}
```

## Creating a PAT

You can create a Personal Access Token in the Nhost dashboard like this:

1. Head to https://app.nhost.io/account
2. Find the "Personal Access Tokens" section
3. Click on "+ Create Personal Access Token"
4. Give it a descriptive name and set the expiration date.
5. Click on "Create"
6. Copy the token. Keep in mind you won't be able to see it again.

Now you can head to your github repository's settings -> Secrets and Variables -> Actions -> New Repository Secret and enter your secret.

For more information about using secrets on github head to their [documentation](https://docs.github.com/en/actions/security-guides/encrypted-secrets)
