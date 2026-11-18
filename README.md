name: Build IPA
on: [push, workflow_dispatch] jobs: build: runs-on: macos-latest steps:
- uses: actions/checkout@v4
- name: Descomprimir y Compilar run: l
unzip -o . zip -d proyecto cd proyecto
xcodebuild -project ThreeOneOSFive.xcodeproj mkdir -p Payload
cp -r build/Release-iphoneos/.app Payload/ zip -r ThreeOneOSFive.ipa Payload
- name: Subir IPA
ises
1004
<
github.com
...
ame
path: proyecto/ThreeOne0SFive.ipa
