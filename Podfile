project 'RxCC.xcodeproj'

# Uncomment this line to define a global platform for your project
# platform :ios, '9.0'
def net_pods
    pod 'Alamofire'
    pod 'RxAlamofire'
end

def model_pods
    pod 'ObjectMapper'
end

def ease_pods
    pod 'Hyphenate_CN'
    #pod 'Hyphenate'
    pod 'EaseUI', :git => 'https://github.com/easemob/easeui-ios-hyphenate-cocoapods.git'
end

def rongclound_pods
    pod 'RongCloudIM/IMLib', '~> 2.8.3'
    pod 'RongCloudIM/IMKit', '~> 2.8.3' 
end

target 'RxCC' do
  # Comment this line if you're not using Swift and don't want to use dynamic frameworks
  
  use_frameworks!

  # Pods for RxCC
    pod 'RxSwift', '~>3.1.0'
    pod 'RxCocoa'
    pod 'RxDataSources'
    net_pods
    model_pods
    rongclound_pods
    pod 'MJRefresh'
    pod 'Spring', :git => 'https://github.com/MengTo/Spring.git', :branch => 'swift3'
    pod 'SnapKit', '~> 3.1.2'
    pod 'AlamofireImage', '~> 3.1'
    post_install do |installer|
        installer.pods_project.targets.each do |target|
            target.build_configurations.each do |config|
                config.build_settings['SWIFT_VERSION'] = '3.0'
            end
        end
        
    end

  target 'RxCCTests' do
    inherit! :search_paths
    # Pods for testing
  end

  target 'RxCCUITests' do
    inherit! :search_paths
    # Pods for testing
  end

end
