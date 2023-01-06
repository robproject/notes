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