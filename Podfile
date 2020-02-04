# Uncomment the next line to define a global platform for your project
platform :ios, '9.0'
install! 'cocoapods', integrate_targets: false

workspace 'FreestarPrebidMobile'

project 'FreestarPrebidMobile.xcodeproj'
project 'Example/PrebidDemo/PrebidDemo.xcodeproj'
project 'tools/PrebidValidator/Dr.Prebid.xcodeproj'

def prebid_demo_pods
  use_frameworks!

  pod 'Google-Mobile-Ads-SDK'
  pod 'mopub-ios-sdk'
end

target 'FreestarPrebidMobile' do
  project 'FreestarPrebidMobile.xcodeproj'

  use_frameworks!
end

target 'FreestarPrebidMobileCore' do
  project 'FreestarPrebidMobile.xcodeproj'

  use_frameworks!

end

target 'PrebidDemoSwift' do
  project 'Example/PrebidDemo/PrebidDemo.xcodeproj'

  prebid_demo_pods

  target 'PrebidDemoTests' do
    inherit! :search_paths
  end
end

target 'PrebidDemoObjectiveC' do
  project 'Example/PrebidDemo/PrebidDemo.xcodeproj'

  prebid_demo_pods
end

target 'Dr.Prebid' do
  project 'tools/PrebidValidator/Dr.Prebid.xcodeproj'

  prebid_demo_pods
end
