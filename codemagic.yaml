workflows:
  android-workflow:
    name: Android Debug APK
    instance_type: mac_mini_m1
    scripts:
      - name: Set up local properties
        script: |
          echo "sdk.dir=$ANDROID_SDK_ROOT" > "$CM_BUILD_DIR/build-android-start/local.properties"
      - name: Build APK
        script: |
          cd build-android-start
          ./gradlew assembleDebug
    artifacts:
      - build-android-start/app/build/outputs/apk/debug/*.apk
