# Release Checklist

Use this before publishing a new release.

## 1. Build Check

- [ ] Project builds without errors
- [ ] DLL loads in KSP
- [ ] Menu opens with `F8`
- [ ] No debug-only test code is accidentally left enabled
- [ ] Version number is updated, if the project has one

## 2. Install Package Check

Expected release package layout:

```text
JebediahsTotallySafeConsole/
└── Plugins/
    └── JebediahsTotallySafeConsole.dll
```

- [ ] Folder name is correct
- [ ] DLL is inside `Plugins`
- [ ] No `.pdb`, `.cs`, `.sln`, `.csproj`, `bin`, or `obj` files are inside the release zip unless intentionally included
- [ ] Zip extracts cleanly

## 3. Gameplay Test

- [ ] Tested from the main menu into a save
- [ ] Tested in flight
- [ ] Tested on launch pad or runway
- [ ] Readiness tools do not crash
- [ ] Black box tools do not crash
- [ ] Visual reset works after using visual tools
- [ ] Game closes normally after testing

## 4. Documentation Check

- [ ] README install instructions still match the release package
- [ ] CHANGELOG has the new version notes
- [ ] Known issues are listed
- [ ] License is included

## 5. Publish

- [ ] Create a GitHub release
- [ ] Upload the release zip
- [ ] Add clear release notes
- [ ] Mention supported KSP version, if known
- [ ] Mention that users should back up saves
