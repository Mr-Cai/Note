[!] Unable to add a source with url `https://cdn.cocoapods.org/` named `trunk`.
You can try adding it manually in `/Users/caikaige/.cocoapods/repos` or via `pod repo add`.

> cd ~/.cocoapods/repos 
> git clone https://github.com/CocoaPods/Specs.git master

platform :ios, '9.0'
source 'https://github.com/CocoaPods/Specs.git'




GDTMobSample-Swift[42563:47939249] [Client] Synchronous remote object proxy returned error: Error Domain=NSCocoaErrorDomain Code=4099 "The connection to service on pid 0 named com.apple.commcenter.coretelephony.xpc was invalidated."

xcrun simctl spawn booted log config --mode "level:off"  --subsystem com.apple.CoreTelephony
