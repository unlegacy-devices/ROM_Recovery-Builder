# How to build Custom ROM, Recovery
- Supported Custom ROM, Recovery versions:

| Custom ROM, Recovery | Workflows | File Name | Status | Note |
| :------------------- | :-------: | :-------: | :----: | :--: |
| CorvusOS |  |  |  | (Coming soon) |
| LineageOS |  |  |  | (Coming soon) |
| Evolution X |  |  |  | (Coming soon) |
| TeamWin Recovery Project | [Actions](https://github.com/VThang51/Recovery-Builder-Workflows/actions/workflows/TWRP.yml) | [TWRP.yml](.github/workflows/TWRP.yml) | Finished  |  |
| OrangeFox Recovery Project | [Actions](https://github.com/VThang51/Recovery-Builder-Workflows/actions/workflows/OFRP.yml) | [OFRP.yml](.github/workflows/OFRP.yml) | Fixing bugs |  |
| PitchBlack Recovery Project | [Actions](https://github.com/VThang51/Recovery-Builder-Workflows/actions/workflows/PBRP.yml) | [PBRP.yml](.github/workflows/PBRP.yml) | Finished |  |
| SkyHawk Recovery Project | [Actions](https://github.com/VThang51/Recovery-Builder-Workflows/actions/workflows/SHRP.yml) | [SHRP.yml](.github/workflows/SHRP.yml) | Finished |  |
| RedWolf Recovery Project | [Actions](https://github.com/VThang51/Recovery-Builder-Workflows/actions/workflows/RWRP.yml) | [RWRP.yml](.github/workflows/RWRP.yml) | Fixing Bug |  |
| (There will be more in the future) |  |  |  |  |

- DON'T FORGET TO READ THE NOTES
## General Instructions
- 1, Let's move to the `Actions` tab
- 2, Choose your Custom Recovery
```bash
OrangeFox-RP Builder (Fixing Bug)
PitchBlack-RP Builder
RedWolf-RP Builder (Fixing Bug)
SkyHawk-RP Builder
TeamWin-RP Builder
```
- 3, Click `Run Workflow` then fill in the necessary information according to the instructions in the following table

| Workflow Dispatch | Description | Example | Illustration | Note |
| :---------------- | :---------- | :-----: | :----------: | :--: |
| Manifest Type | [omni](https://github.com/minimal-manifest-twrp/platform_manifest_twrp_omni), [aosp](https://github.com/minimal-manifest-twrp/platform_manifest_twrp_aosp), [lineageos](https://github.com/minimal-manifest-twrp/platform_manifest_twrp_lineageos) | `aosp` | ![](https://raw.githubusercontent.com/VThang51/ROM_Recovery-Builder-Workflows/main/sh/Guide.png) |  |
| Manifest Branch | Branch of Minimal Manifest (twrp-4.4-deprecated, . . . , twrp-12.1, twrp-14.1) | `twrp-12.1` |  |  |
| Device Tree URL | URL GitHub of Device Tree | https://github.com/VThang51/android_device_samsung_a13 |  | Make sure the Repository is set as `Public` |
| Device Tree Branch | Branch of Device Tree | `master` | ![](https://raw.githubusercontent.com/VThang51/ROM_Recovery-Builder-Workflows/main/sh/Guide1.png) |  |
| Brand | Phone manufacturer | `samsung` | You can find it in the `BoardConfig.mk` file ![](https://raw.githubusercontent.com/VThang51/ROM_Recovery-Builder-Workflows/main/sh/Guide2.png) |  |
| Device Code | Device Code is recorded in the Device tree | `a13x` | You can find it in the `BoardConfig.mk` file ![](https://raw.githubusercontent.com/VThang51/ROM_Recovery-Builder-Workflows/main/sh/Guide2.png) |  |
| Makefile Type | Look in your Device tree `<omni/twrp>_a13x.mk` | `twrp` | ![](https://raw.githubusercontent.com/VThang51/ROM_Recovery-Builder-Workflows/main/sh/Guide3.png) |  |
| Add "export" | Add `export` command if needed | `export XXXXX=1 && export YYYYY=true && export ZZZZZ=1` | Adding `export ALLOW_MISSING_DEPENDENCIES=true` was not necessary since I added it to the Workflow (Don't forget to add `&&`) |  |
| Build Target | location of stock recovery on the device | `recovery` |  |  |

# Note
- If you intend to develop this project, please clone this repository or submit a pull request.
- Thank you!!! 
- Contact me at [Telegram](https://t.me/VThang51), [Facebook (Messenger)](https://m.me/thang.nguyenviet.05112007), [Email](mailto:vietthang0511.2@gmail.com)
