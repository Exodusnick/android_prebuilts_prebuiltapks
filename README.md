# Deprecated

The recommended way to add microG to LineageOS builds now is the [android_vendor_partner_gms](https://github.com/lineageos4microg/android_vendor_partner_gms) repo.

This repository will no longer be updated.

# Prebuilt APKs

This is a collection of FOSS APKs, coupled with the respective Android.mk for an
easy integration in the Android build system.
These are just the official unmodified prebuilt binaries, signed by the
corresponding developers, except for:
 * com.google.android.maps, as the JAR and the XML have been extracted from the ZIP on the [microG's GitHub release page](https://github.com/microg/android_frameworks_mapsv1/releases)
 * additional_repos.xml, as it is just the nonstandard FDroid repository XML file

To include them in your build just add their name in CUSTOM_PACKAGES (for
example in vendor/lineage/config/common_mobile.mk).

The included APKs are:
 * FDroid packages (binaries sourced from [here](https://f-droid.org/packages/org.fdroid.fdroid/) and [here](https://f-droid.org/packages/org.fdroid.fdroid.privileged/))
   * FDroid: a catalogue of FOSS (Free and Open Source Software) applications for the Android platform
   * FDroid Privileged Extension: a FDroid extension to ease the installation/removal of apps
   * LocalGsmNlpBackend: UnifiedNlp backend that uses local GSM data to resolve user location
   * NominatimNlpBackend: UnifiedNlp (no GAPPS) backend that uses MapQuest's Nominatim service (based on OpenStreetMap) for geocoding
   * additional_repos.xml: a configuration file to include the [microG](https://microg.org/fdroid.html), [Bromite](https://www.bromite.org/fdroid), and [IzzyOnDroid](https://apt.izzysoft.de/fdroid/repo) FDroid repositories in the ROM (requires FDroid >= 1.5)
 * microG packages (binaries sourced from [here](https://microg.org/download.html) and [here](https://github.com/microg/android_frameworks_mapsv1))
   * GmsCore: the main component of microG, a FOSS reimplementation of the Google Play Services (requires GsfProxy and FakeStore for full functionality)
   * GsfProxy: a GmsCore proxy for legacy GCM compatibility
   * FakeStore: an empty package that mocks the existence of the Google Play Store
   * com.google.android.maps: legacy microG's mapsv1 reimplementation
 * AuroraOSS packages (binaries sourced from [here](https://gitlab.com/AuroraOSS))
   * AuroraDroid: an alternate to the FDroid app store
   * AuroraStore: an alternate to Google's Play Store
   * AuroraServices: a system / root application that integrates with the Aurora line of products
 * GrapheneOS packages (binaries sourced from [here](https://github.com/GrapheneOS/PdfViewer/releases))
   * PdfViewer: a Simple Android PDF viewer based on pdf.js and content providers
