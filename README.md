# ReqIF Import sample App

This sample app is proposing to user how to import ReqIF document inside ARAS Innovator. The importer is creating Requirements and capture Requirement content in either/or Requirement Engineering (RE) / Technical Documentation Foundation (TDF aka: TD "TechDoc").

The prime Import is for RE where Requirement are living but as a demonstrator, a copy/modification of the importer method is allowing to create the same result in TD for the ones looking at using TD. 

Importer supports 2 formats:
- reqif
- reqifz (zip with other referenced files)


It's a sample application proposing a framework to import ReqIF content into ARAS, so feel free to inspire your needs from the main methods where placeholders are present. Main methods are:
- RE (Button) -> reqif_importFile (Javascript) -> reqif_parseFile (Server)
- TD (Button) -> reqif_importFile_TDF (Javascript) -> reqif_parseFile_TDF (Server)

<span style="background-color: #FFFF00">DISCLAIMER:</span> We have tested this sample importer with few ReqIF outputs from Requirement engineering authoring tool, there is no guarantee that your ReqIf files will work directly with the default mapping. If your reqif files doesn't import, please check modify the mapping into the parser method to fit with the model of your File. By default the unique identifier is **ReqIF.ChapterName**

## History

Release | Notes
--------|--------
[14.0.25.1](https://github.com/ArasLabs/ReqIF-Import-sample-app/releases/tag/14.0.25.1) | First release.

#### Supported Aras Versions

Project | Aras
--------|------
[14.0.25.1](https://github.com/ArasLabs/ReqIF-Import-sample-app/releases/tag/14.0.25.1) | R25,R26,R27,R28,R29,R30

## Installation

#### Important!
**Always back up your code tree and database before applying an import package or code tree patch!**

### Pre-requisites

1. Aras Innovator installed (version 25 till 30)
2. [Aras Update](http://www.aras.com/support/downloads/) installed (version 1.18 or later)
1. Requirement Engineering/RE (version 14.0.1) installed (possible with Aras Update)
1. Technical Documentation/TD (version 14.0.1) installed (possible with Aras Update)
3. ReqIF Import Sample App package

### Install Steps

<!-- TODO: Add screenshot(s) -->

1. Run Aras Update.
2. Select **Local** in the sidebar.
3. Click **Add package reference** and select the ReqIF Import Sample App installation package.
4. Select the newly added package from the list and click **Install**.
5. Select the components you want to install and click **Next**.
    * Aras Innovator Code Tree Updates
    * Aras Innovator Database Updates
6. Choose **Detailed Logging** and click **Next**.
7. Enter the required parameters for the target Aras Innovator instance. Which parameters are required varies based on which components you have selected to install.
    * When selecting the install path for your Innovator instance, be sure to select the Innovator subfolder. 
    * Example: If your Innovator instance is installed in `C:\Program Files (x86)\Aras\R25`, select `C:\Program Files (x86)\Aras\R25\Innovator`.
8. Click **Install** to begin installing the package.
9. When the package finishes installing, close Aras Update.

## Usage

For information on using the sample application, view [the documentation for RE](./Documentation/User_Guide_RE.md) or for [TD](./Documentation/User_Guide_TD.md).

## Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request

For more information on contributing to this project, another Aras Labs project, or any Aras Community project, shoot us an email at araslabs@aras.com.

## Credits

Sample application created by Aras Development.

## License

Aras Labs projects are published to Github under the MIT license. See the [LICENSE file](./LICENSE.md) for license rights and limitations.