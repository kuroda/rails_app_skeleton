Rails App Skeleton
==================


Usage
-----

    mkdir new_app
    git clone git://github.com/kuroda/rails_app_skeleton.git skeleton
    cd skeleton
    git archive --format=tar HEAD | tar -C ../new_app -xf -
    cd ../new_app
    find . -type f -print0 | xargs -0 sed -i 's/skeleton/new_app/g'
    find . -type f -print0 | xargs -0 sed -i 's/Skeleton/NewApp/g'
    rm README.md
    ruby -e "require 'securerandom'; puts %Q{MyApp::Application.config.secret_token = '#{SecureRandom.hex(64)}'}" >> config/initializers/secret_token.rb
