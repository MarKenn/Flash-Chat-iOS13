platform :ios, '13.0'
inhibit_all_warnings!

target 'Flash Chat iOS13' do
  use_frameworks!

  # Pods for Flash Chat iOS13
  pod 'Firebase/Auth', '~> 8.4.0'
  pod 'Firebase/Firestore', '~> 8.4.0'
  
end

post_install do |installer|
  installer.pods_project.targets.each do |target|
    target.build_configurations.each do |config|
      if config.build_settings['IPHONEOS_DEPLOYMENT_TARGET'].to_f < 9.0
        config.build_settings['IPHONEOS_DEPLOYMENT_TARGET'] = '9.0'
      end
    end
  end
end
