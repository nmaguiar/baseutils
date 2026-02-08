````yaml
╭ stdout   
├ stderr  : [vuln] Vulnerability scanning is enabled
│           2026-02-08T07:24:53Z	INFO	[secret] Secret scanning is enabled
│           2026-02-08T07:24:53Z	INFO	[secret] If your scanning is slow, please try '--scanners vuln' to
│           disable secret scanning
│           2026-02-08T07:24:53Z	INFO	[secret] 
├ exitcode: 1 
╰ cmd     : docker run --pull always --rm -v trivy-db:/root/.cache/trivy aquasec/trivy -f json  image
            nmaguiar/baseutils:deb 
````
