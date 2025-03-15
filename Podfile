platform :ios, '15.0'
use_frameworks!

target 'Feelings' do
  # UI/UX
  pod 'Lottie'              # Animasyonlar için
  pod 'SnapKit'             # Auto Layout için
  pod 'Charts'              # Grafikler için
  
  # Networking
  pod 'Alamofire'          # HTTP istekleri için
  pod 'OpenAISwift'        # OpenAI API entegrasyonu için
  
  # Database
  pod 'RealmSwift'         # Yerel veritabanı için
  
  # Utilities
  pod 'SwiftLint'          # Kod kalitesi için
  pod 'IQKeyboardManager'  # Klavye yönetimi için
  
  # Analytics & Crash Reporting
  pod 'Firebase/Analytics'
  pod 'Firebase/Crashlytics'
  
  # Testing
  target 'FeelingsTests' do
    inherit! :search_paths
    pod 'Quick'
    pod 'Nimble'
  end
  
  # UI Testing
  target 'FeelingsUITests' do
    inherit! :search_paths
  end
end

post_install do |installer|
  installer.pods_project.targets.each do |target|
    target.build_configurations.each do |config|
      config.build_settings['IPHONEOS_DEPLOYMENT_TARGET'] = '15.0'
    end
  end
end