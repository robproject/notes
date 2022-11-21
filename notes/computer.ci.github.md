---
id: 1f76dp53tzqozdchv4m5z2c
title: GitHub
desc: ''
updated: 1655493121453
created: 1655492082970
---
# Github Actions

## Artifacts
### Upload
```
  - name: 'Upload Artifact'
    uses: actions/upload-artifact@v3
    with:
      name: my-artifact
      path: my_file.txt
      retention-days: 5
```
### Download
```
- name: Download a single artifact
  uses: actions/download-artifact@v3
  with:
    name: my-artifact

- name: Download all workflow run artifacts
  uses: actions/download-artifact@v3
```