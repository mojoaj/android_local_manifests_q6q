# Local manifest: LineageOS 24.0 for the Samsung Galaxy Z Fold6 (q6q)

Unofficial LineageOS port, maintained by [mojoaj](https://github.com/mojoaj).

```sh
repo init -u https://github.com/LineageOS/android.git -b lineage-24.0 --git-lfs
mkdir -p .repo/local_manifests
curl -o .repo/local_manifests/q6q.xml https://raw.githubusercontent.com/mojoaj/android_local_manifests_q6q/q6q-24.0/q6q.xml
repo sync -c -j8
source build/envsetup.sh
lunch lineage_q6q-cp2a-userdebug
m bacon
```

The manifest swaps in forks (branch `q6q-24.0`) of the repositories that carry q6q changes:
frameworks/base, lineage-sdk, device/qcom/sepolicy_vndr/sm8650 (LineageOS) and the
sm8650 device/vendor/kernel/hardware trees (Exynoobs), plus the q6q device and vendor trees.

LineageOS 23.2 (Android 16) is on branch `q6q`.

Release builds are signed with private keys and are not reproducible bit-for-bit; test-keys builds are.
