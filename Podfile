platform :ios, '10.0'
use_frameworks!
inhibit_all_warnings!

target 'SPPApp' do
    pod 'CHTCollectionViewWaterfallLayout', '~> 0.9.0'
    pod 'RealmSwift', '~> 3.10.0'
    pod 'SDWebImage', '~> 3.8'
    pod 'AsyncSwift', '~> 2.0'
    pod 'Alamofire', '~> 4.5'
    pod 'Fabric', '~> 1.7'
    pod 'Crashlytics', '~> 3.10'
    pod 'SwiftyJSON', '~> 3.1'
    pod 'Socket.IO-Client-Swift', '~> 11.1.0'
    pod 'EstimoteSDK', '~> 4.8'
    pod 'Device', '~> 3.0'
    pod 'SevenSwitch', '~> 2.0'
    pod 'FBSDKCoreKit', '~> 4.26'
    pod 'FBSDKShareKit', '~> 4.26'
    pod 'FBSDKLoginKit', '~> 4.26'
    pod 'PagingView', :git => 'https://github.com/breezy-hr/PagingView.git', :commit => 'cbf49d2d4e'  # Swift 4 fixes on this fork
    pod 'BFPaperButton', '~> 2.1'
    pod 'LicensesKit', '~> 1.2.1'
    pod 'RxSwift',    '~> 3.0'
    pod 'RxCocoa',    '~> 3.0'
    pod 'RxBlocking', '~> 3.0'
    pod 'iCarousel', '~> 1.8'
    pod 'SwiftEventBus', '~> 2.1'
    pod 'Sentry', :git => 'https://github.com/getsentry/sentry-cocoa.git', :subspecs => ['Core', 'KSCrash'], :tag => '3.7.1'
end

# A few Pods still require Swift 3, but don't specify a Swift
# version in their spec, so we override below.
post_install do |installer|
    installer.pods_project.targets.each do |target|
        if ["SevenSwitch", "RxCocoa", "RxSwift", "RxBlocking", "LicensesKit", "Socket.IO-Client-Swift"].include? target.name
            target.build_configurations.each do |config|
                config.build_settings['SWIFT_VERSION'] = '3.0'
            end
        end
    end
end
