# CnCNet Yuri's Revenge Client Package

![logo](https://user-images.githubusercontent.com/6104940/219884309-a1737d96-c140-49ae-b235-456cc2c43d6a.png)

The official CnCNet [Yuri's Revenge](https://cncnet.org/yuris-revenge) package for online.
This package is an add-on to the [XNA CnCNet Client](https://github.com/CnCNet/xna-cncnet-client) by [Rampastring](https://github.com/Rampastring)

### Contributors

* [tomsons26](https://github.com/tomsons26)
* [dkeetonx](https://github.com/dkeetonx)
* [GrantBartlett](https://github.com/GrantBartlett)
* [Martin](https://forums.cncnet.org/profile/32538-ravage/)
* [Kerbiter](https://github.com/Metadorius)
* [Burg](https://github.com/alexp8)
* [devo1929](https://github.com/devo1929)
* [Belonit](https://github.com/Belonit)
* [CCHyper](https://github.com/CCHyper)
* [ [RU]Polye](https://github.com/bhdrks78)
* [CnCRAZER](https://github.com/CnCRAZER)
* [BRichardson1991](https://github.com/brichardson1991)

### Development

**NOTE:** This is NOT the repository necessary for developing the CnCNet client for Yuri's revenge. That is the **XNA CnCNet Client** mentioned above. This is simply a wrapper for it.

To contribute to the XNA client for YR, you must also check out the `xna-cncnet-client` repo mentioned above. Once that repo is checked out, you can copy and paste the `Directory.Build.Game.YR.props` file located into the `resources` folder of the `cncnet-yr-client-package` checkout location to the root of the `xna-cncnet-client` checkout location. This file should automatically copy over all necessary resources from this repository to the output directory of the compiled `xna-cncnet-client` executable. Then, when launched, it should do so with with the Yuri's revenge theme.

You MUST edit the `YRSource` property in the `Directory.Build.Game.YR.props` file if you use it.

### Repository Structure

- `package` - This directory contains the exact file structure that should make up the client package that is delivered to users.
- `resources` - This directory contains any resources to assist in building the package, like other theming elements. For example, this directory contains various `expandspawn09.mix` files for custom crates. These `mix` files can be moved to the `package` directory when we want to change the crate theme.
- `tools` - This directory contains tools that are used to help build the package. It includes tools like:
  - `download-artifacts/download-client.ps1` - A powershell script to automatically download a specific set of binaries of the `xna-cncnet-client`
  - `download-artifacts/download-client-launcher.ps1` - A powershell script to automatically download a specific instance of the client launcher.
  - `inno-setup/inno-setup.ps1` - A powershell script to build the InnoSetup installer
  - `maps-updater/maps-updater.ps1` - A powershell script that is basically a wrapper to run our YRMapsUpdater C# program. This program updates the mpmaps.ini file by scanning for all map changes in the `package/Maps/Yuri's Revenge` directory.

### Deployments

[Documentation](DEPLOYMENTS.md)

## Sponsored by
<a href="https://www.digitalocean.com/?refcode=337544e2ec7b&utm_campaign=Referral_Invite&utm_medium=opensource&utm_source=CnCNet" title="Powered by Digital Ocean" target="_blank">
    <img src="https://opensource.nyc3.cdn.digitaloceanspaces.com/attribution/assets/PoweredByDO/DO_Powered_by_Badge_blue.svg" width="201px" alt="Powered By Digital Ocean" />
</a>
