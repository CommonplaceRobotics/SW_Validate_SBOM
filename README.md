# SW_Validate_SBOM
Github Action for validating SBOMs

This action is intended to be used for CPR internal purposes. Use by anyone else is at your own risk, consider this repository not stable.

Use it as follows:

```
- name: Validate SBOM with company policies
  uses: CommonplaceRobotics/Action_Validate_SBOM@v1
  with:
	sbom: sbom_rpi.cdx.json
    policies: sbom_policies.yml	
```

With the following parameters:
* sbom: name of the SBOM file to validate
* policies: sbomqs policy file (company defaults are used if not defined)

The following checks are done:
* CRA compliance (BSI TR-03183-2 v2)
* License compliance
* Warning for dangerous licenses
* SBOM completeness
