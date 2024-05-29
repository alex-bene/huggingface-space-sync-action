# Sync With Hugging Face Space
This action creates seperate README.md file with a YAML header prepended for Hugging Face 🤗 Space and syncs your updates with the space repo.

A repo using this action can be found [here](https://github.com/alex-bene/BianqueNet).

## Usage
```yaml
- uses: alex-bene/huggingface-space-sync-action@v0.1
  with:
    # The github repo you are syncing from. Required.
    github_repo_id: ''
    # The branch of your github repo you want to sync from. Defaults to 'main'. Optional.
    github_branch: 'main'
    # The yaml headers file to use, e.g., hf_space_metadata.yml (will be prepended to your README.md in the HF space). Required.
    yaml_header_path: ''
    # The Hugging Face repo id you want to sync to. (ex. 'username/reponame'). Required.
    huggingface_repo_id: ''
    # Hugging Face token with write access and corresponding username. Required.
    # Here, we provide a token that we called `HF_TOKEN` when we added the secret to our GitHub repo.
    hf_username: ''
    hf_token: ${{ secrets.HF_TOKEN }}
```

## License
The scripts and documentation in this project are released under the [MIT License](LICENSE).