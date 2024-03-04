# How to clone the large repos

## Scenario

- Maintained a repo for very long time with an old computer
- It has lots of large files and long commit history
- Wanted to `git clone` it in a new computer
- Failed because it is too large

## Solution

- git clone --depth=1 <repo_url>

Alternative 2 ways:

- git clone --filter=blob:none <repo_url>
- git clone --filter=tree:0 <repo_url>

## Final Solution

If above solution still won't work, 

- Download all the files
- Create a new repo
- Copy all files to the new repo
- Git push
- Use the new repo instead
