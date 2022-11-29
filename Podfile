target 'MathSolver' do
    pod 'iosMath', '~> 0.7.2'
end
target 'MathSolverTests' do
    pod 'MathSolver', :path => './'
end

post_install do |installer|
  installer.pods_project.targets.each do |target|
    if target.respond_to?(:product_type) and target.product_type == "com.apple.product-type.bundle"
      target.build_configurations.each do |config|
        config.build_settings['CODE_SIGNING_ALLOWED'] = 'NO'
      end
    end
  end
end
