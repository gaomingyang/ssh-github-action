# ssh-github-action

this is a github action ,help to ssh server by key.

## Usage
```
steps:
    - id: ssh-server
    uses: gaomingyang/ssh-github-action@main
    with:
        SSH_USER: ${{ secrets.SSH_USER }}
        SSH_HOST: ${{ secrets.SSH_HOST }}
        SSH_PORT: ${{ secrets.SSH_PORT }}
        SSH_KEY: ${{ secrets.SSH_KEY }}

    - name: run commands on server
    run: |
    ssh ${{ steps.ssh-server.outputs.SERVER_NAME }} ls

```