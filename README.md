# Metaverse Template

A starter Unity project for creating VRChat worlds.

## Requirements

- VRChat Creator Companion (VCC)
- Unity **2022.3.22f1**, the Unity version currently supported by VRChat
- A VRChat account with permission to upload content (only needed to publish)

Use VCC to install and manage the VRChat SDK. This project intentionally does not pin an SDK package version; VCC can install a compatible version and keep it current.

## Getting started

1. Clone this repository.
2. In VCC, choose **Projects → Add Existing Project** and select the cloned folder.
3. Open **Manage Project** in VCC and install the **Worlds** SDK. Install **ClientSim** as well if you want to test worlds in the Unity Editor.
4. Open the project in Unity 2022.3.22f1.
5. Create a scene under `Assets/Scenes`, then add and configure the VRChat Scene Descriptor using the VRChat SDK.
6. Add your scenes and assets to the world, save all Unity-generated `.meta` files, and test with the SDK before uploading.

For Quest or Android builds, install Android Build Support through Unity Hub and follow the current VRChat platform setup instructions.

## Repository layout

- `Assets/` — Unity scenes and project assets.
- `Packages/manifest.json` — Unity package manifest. Manage VRChat packages through VCC.
- `ProjectSettings/ProjectVersion.txt` — pins the supported Unity editor version.
- `Metaverse_Template.scenetemplate` — supplied scene-template metadata.

Unity-generated project files such as `Library/`, build output, and local editor settings are excluded from version control.

## Supplied scene-template metadata

`Metaverse_Template.scenetemplate` references a scene and dependencies by Unity asset GUID. Those referenced assets are not present in this repository, so the metadata cannot currently resolve to a complete scene template. The file is preserved as supplied; it is not the project's active scene. Add the source scene and all referenced assets before relying on that template.

## References

- [VRChat SDK getting started](https://creators.vrchat.com/sdk/)
- [VRChat current supported Unity version](https://creators.vrchat.com/sdk/upgrade/current-unity-version/)
- [VRChat Creator Companion documentation](https://vcc.docs.vrchat.com/)
