# Paed Dose

An offline paediatric dose index for Android.

- **Drugs:** enter a child's weight and read the dose per kg, the maximum dose, and the volume for common formulations. Newborn mode takes gestational age and age in days.
- **IV fluids:** maintenance rate, shock bolus, and severe dehydration (Plan C) volumes.
- **Saved drugs and notes:** stay on the phone only.

Doses come from open sources (WHO, NICE, Royal Children's Hospital Melbourne, Australian Neonatal Medicines Formulary, NHS Scotland, Perth Children's Hospital, MSF). This is a starter list. Check every dose against your hospital formulary, BNFC or WHO before prescribing. Malnutrition guidance is not included yet.

## Get the app
1. Open the **Releases** page of this repo on your phone.
2. Download `PaedDose.apk` from the **latest** release and install it. Allow "Install anyway" if Play Protect asks.

## How it is built
The project lives in `paed-dose-app.zip`. The workflow in `.github/workflows/build-apk.yml` unpacks the zip, builds the APK, and publishes it to the **latest** release. It runs on every push to `main`.

## Update the app
Upload a new `paed-dose-app.zip` with the same name (**Add file, Upload files**) and commit. A new APK builds in a few minutes and installs over the old one, keeping saved notes.

## Signing
`paeddose.jks` inside the zip is a fixed key for sideloading only, not for the Play Store. If the repo is public, anyone can read it, so keep the repo private if you can.
