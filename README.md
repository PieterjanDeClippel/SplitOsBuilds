# Split OS Builds in Visual Studio
## About

With this setup, you can open your solution in Visual Studio for Windows and a Linux/Debian DevContainer side-by-side.
The temporary files are split out and don't interfere with each other

<img width="620" height="551" alt="afbeelding" src="https://github.com/user-attachments/assets/55a6644e-53d5-497c-993a-1afdfed8050a" />

If you still see any `bin` or `obj` folders in your projects, do the following:
- Close Visual Studio
- Remove all `bin` and `obj` folders. Also remove the `.vs` folder. You may use [this tool](https://github.com/MintPlayer/MintPlayer.Dotnet.Tools/tree/master/Helpers/RemoveObjBin) to make it easier), or run `git clean -fdx` to remove all untracked files at once.
- Remove your existing DevContainer and corresponding docker-image through Docker Desktop
- Reopen the solution in Visual Studio
- Reopen the folder in VS Code and start the DevContainer

## Result

The build files should now show up under a `tmp-build` folder, as shown in the image above.
Because of that the files no longer produce conflicting, non-existing paths

<img width="3149" height="894" alt="afbeelding" src="https://github.com/user-attachments/assets/c4591292-5f99-4a23-b7e1-743a8b78dbd3" />
