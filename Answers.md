# Answers to Part 3

Add your answers to the questions in Part 3, Step 2 below. 

## Vulernability Remediation:
### Vulnerability 1: 
1. Which package or library are you addressing?
PyYAML 5.1
2. Which CVE is linked to this vulnerability?
2019-20477
3. What remediation steps do you suggest?
I suggest updating pyYAML to a higher version like 5.3 or 6.0+. After updating, the codebase should be updates as well to reflect the changes made. Lastly, updating instances of yaml.load() with `yaml.safe_load` or use a SafeLoader. This ensures that deserialized data or code is not modified without permission and arbitrary command execution is prevented.

### Vulnerability 2:
1. Which vulnerability are you addressing?
Pillow 9.4.0
2. Which CVE is linked to this vulnerability?
CVE-2023-50447
3. What remediation steps do you suggest? 
I suggest updating the Pillow package to a version of 10.2.0 or higher. PIL.ImageMath.eval() function has the potential for arbitrary code execution, in version 10.2.0  the fix for this was introduced. Furthermore, reviewing the source code of the application is recommended to esure that the user input is not passed directly into evaluation methods.


Sources
https://access.redhat.com/security/cve/cve-2019-20477
https://access.redhat.com/security/cve/cve-2023-50447

