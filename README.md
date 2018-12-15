# Vortex OS
## Official devices application

Devices repository: https://github.com/vortex-devices

Before you open a pull request to add your device into our list of official devices, you should know a few simple things:

### 1. To turn into a maintainer of Vortex OS:

1.2 - You must have a way to check your builds, on your own way, having the device, or send the builds for someone test. Completely blind and/or untested builds aren't allowed.

1.3 - Appliers that comproved have the device, will have the preference on taking the maintainship.

1.4 - You must have knowledge of git.

1.5 - You must do an unofficial build and make the device stable for daily usage before applying.

1.6 - You should have your device sources open for us take a look.

1.7 - You mustn't be a placeholder of another maintainer that was removed. The pull request that are considered of that kind won't be accepted.

### 2. Maintainers conduct notes:

2.1 - The maintainers mustn't do any unofficial modifications.

2.2 - The maintainers should upload theirs trees on https://github.com/vortex-devices

2.3 - The maintainers should test every update before upload in our OTA.

2.4 - The maintainers must keep the authorship of Git commits on everything that they'll make a change, even it's your device tree, kernel or ROM sources. Lots of git commit --amend and force-pushes are acceptable.

2.5 - Relationships fights can be done in PM on Telegram or XDA. 

2.6 - The maintainers also need to add 'export CUSTOM_BUILD_TYPE=OFFICIAL' in their build environment so OTA app will be included.

### 3. Changelog
For each new version, you need to upload the changelog to this repository in the device specific folder.

The changelog file name must match the **.zip** file name and should end with **.txt**
Eg: **.zip** is **Essential_platina-8.1.0-20180207-0418-OFFICIAL.zip**, changelog file name should be **Essential_platina-8.1.0-20180207-0418-OFFICIAL.txt**

### 5. Over-the-air (OTA) updates
Our system is automatic, you should not worry about updating some script, just upload the new build to the FTP server and send a pull request with the changelog and also edit your device JSON file (**builds/your_device_codename.json**) in this repository.

Eg: Moto G 2013 is called **falcon**, so the device JSON file is **builds/falcon.json**

**Note:** New builds can take up to 30 minutes to appear on the site and in the OTA application.

### 6. JSON params

##### devices.json
| Param | Description | Required |
|--|--|--|
| name | Device name | Yes |
| brand | Device manufacturer | Yes |
| codename | Device codename, eg: falcon | Yes |
| version_code | Version code, lowercase, eg: oreo | Yes |
| version_name | Version name, will be shown on download portal, eg: Oreo | Yes |
| maintainer_name | Your name | Yes |
| maintainer_url | Your personal URL, eg: https://github.com/jhenrique09/ or https://forum.xda-developers.com/member.php?u=6519039 | No  |
| xda_thread | XDA thread URL, eg: https://forum.xda-developers.com/g5-plus/development/rom-pixel-experience-t3704064 | No |

##### builds/your_device_codename.json
| Param | Description | Required |
|--|--|--|
| filename | Build file (.zip) name | Yes |
| filesize | Build file (.zip) size (in bytes) | Yes |
| filehash | Build file (.zip) md5 hash | Yes |
| datetime | Build file (.zip) time | Yes |
| id | Build file (.zip)  hash | Yes |

