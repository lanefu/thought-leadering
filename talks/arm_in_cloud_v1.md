# 

## architecture hunting snippets
```bash
sed -i 's/amd64/${ARCHITECTURE}/g' *.sh

find ./GIT/ -name "*amd64*"
```
```powershell
(Get-ChildItem -Path .\ -Recurse -Filter "*.sh" -File) | ForEach-Object { (Get-Content $_.FullName) -replace 'amd64', "${env:ARCHITECTURE}" | Set-Content $_.FullName }
(Get-ChildItem -Path .\GIT\ -Recurse -Filter "*amd64*" -File).FullName
```

## CI snippets

### github actions

[Rpardini's opensearch-minimal-multiarch](https://github.com/rpardini/opensearch-minimal-multiarch/blob/main/.github/workflows/main-latest.yml)



## Resources
### misc
[Cool governemnt Presentation Evaluating Cavium Thunder X2 for HPC uses](https://www.osti.gov/servlets/purl/1640906)


### Performance

#### Deep Insights from Liz Fong-Jones and Honeycomb.io
https://www.honeycomb.io/blog/present-future-arm-aws-graviton-honeycomb


#### Benchmarks from Ampere and Jeff Wittich
[Honestly just follow his Twitter](https://twitter.com/jwittich)


### Noisy Neighbor
[Straight from Intel about managing noisy neigbhor problem in K8s](https://www.intel.com/content/www/us/en/developer/articles/technical/noisy-neighbors-problem-in-kubernetes.html)
[Ampere Blog about SMT in the cloud](https://amperecomputing.com/blogs/looking-beyond-smt-in-the-cloud)

