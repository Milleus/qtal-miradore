# Miradore

## Table of Contents

- [Home](#home)
  - [Dashboard](#dashboard)
  - [Reports](#reports) (To explore)
  - [Map](#map)
  - [Setup guide](#setup-guide)
- [Enrollment](#enrollment)
  - [Android Enterprise](#android-enterprise)
  - [Enroll device](#enroll-device)
  - [Enrollment log](#enrollment-log)
- [Management](#management)
  - [Devices](#devices)
  - [Configuration profiles](#configuration-profiles)
  - [Applications](#applications)
  - [Files and certificates](#files-and-certificates)
  - [Business policies](#business-policies)
  - [Patches](#patches) (To explore)
  - [Action log](#action-log)
- [Company](#company)
  - [Users](#users)
  - [Attributes](#attributes)
  - [Retired devices](#retired-devices) (To explore)
- [System](#system)
  - [Permissions](#permissions)
  - [Infrastructure diagram](#infrastructure-diagram)
  - [Subscription](#subscription)

## Home

### Dashboard

Analytics charts. Customisable widgets.

<img src="./docs/home-dashboard-edit.png?raw=true" width="100%" alt="dashboard edit"/>

### Reports

*(Have not figured out how to use this yet, seems like a way to generate reports.)*

### Map

View all devices on a map. Clicking on location pin brings you to the device info page.

<img src="./docs/home-map-view.png?raw=true" width="100%" alt="map view"/>

### Setup guide

Basic step by step guides to teach you how to enroll device, secure device, etc.

<img src="./docs/home-setup-guide-view.png?raw=true" width="100%" alt="setup guide view"/>
<img src="./docs/home-setup-guide-example.png?raw=true" width="100%" alt="setup guide example"/>

## Enrollment

### Android Enterprise

I don't really know what's the difference between this and their normal "Enroll device". But apparently on this page you can change some basic settings, factory reset the device, scan the QR code to enroll the device.

It might be for enrollment of the device that is also on [Samsung Knox Mobile Enrollment (KME)](https://www.miradore.com/knowledge/android/samsung-knox-mobile-enrollment/).

<img src="./docs/enrollment-android-enterprise-edit.png?raw=true" width="100%" alt="android enterprise edit"/>

### Enroll device

Straightforward enrollment. Select OS, select user (email), factory reset device and scan QR code. A user can have multiple devices tagged to him/her.

<img src="./docs/enrollment-enroll-device-step-1.png?raw=true" width="100%" alt="enroll device step 1"/>
<img src="./docs/enrollment-enroll-device-step-2.png?raw=true" width="100%" alt="enroll device step 2"/>
<img src="./docs/enrollment-enroll-device-step-3.png?raw=true" width="100%" alt="enroll device step 3"/>
<img src="./docs/enrollment-enroll-device-step-4.png?raw=true" width="100%" alt="enroll device step 4"/>

### Enrollment log

Audit trial logs for enrolling device, whether it a QR code is queued, expired, successfully enrolled, etc.

<img src="./docs/enrollment-enrollment-log-view.png?raw=true" width="100%" alt="enrollment log view"/>

## Management

### Devices

List of devices enrolled. Some of the actions that you can do are:
- Sync now
- Reboot device
- Shutdown device
- Update client
- Software update
- Send message
- Deploy (either configuration profile, application, file or certificate)
- Unenroll device
- Retire device
- Lock device
- Play alarm sound
- Clear passcode
- Reset passcode
- Reset profile passcode
- Enable lost mode
- Wipe device

<img src="./docs/management-devices-view.png?raw=true" width="100%" alt="devices view"/>

Double-clicking on a device shows more information.

<img src="./docs/management-devices-single-view.png?raw=true" width="100%" alt="single device view"/>

<img src="./docs/management-devices-single-applications.png?raw=true" width="100%" alt="single device applications tab"/>

<img src="./docs/management-devices-single-deployments.png?raw=true" width="100%" alt="single device deployments tab"/>

<img src="./docs/management-devices-single-action-log.png?raw=true" width="100%" alt="single device action log tab"/>

### Configuration profiles

List of configuration profiles. Configuration profiles are configurations such as location tracking, restrictions (application or system), passcode policy, kiosk mode, etc.

<img src="./docs/management-configuration-profiles-view.png?raw=true" width="100%" alt="configuration profiles view"/>

Example of adding a configuration profile.

<img src="./docs/management-configuration-profiles-step-1.png?raw=true" width="100%" alt="configuration profiles step 1"/>

<img src="./docs/management-configuration-profiles-step-2.png?raw=true" width="100%" alt="configuration profiles step 2"/>

<img src="./docs/management-configuration-profiles-step-3.png?raw=true" width="100%" alt="configuration profiles step 3"/>

Double-clicking on a configuration profile shows more information.

<img src="./docs/management-configuration-profiles-single-view.png?raw=true" width="100%" alt="single configuration profile view"/>

### Applications

List of applications. This is where you can add applications through either:
- APK download (file upload)
- APK download (external URL)
- Google Play store
- Managed Google Play store

If the applications are added with the 'Managed Google Play store' option, they can be deployed silently to the devices. 'Managed Google Play store' requires set up of the play store (one time set up) and possibly accepting some kind of permission through the Miradore Client application on the device.

<img src="./docs/management-applications-view.png?raw=true" width="100%" alt="applications view"/>

Example of adding an application through Managed Google Play store.

<img src="./docs/management-applications-step-1.png?raw=true" width="100%" alt="applications step 1"/>

<img src="./docs/management-applications-step-2.png?raw=true" width="100%" alt="applications step 2"/>

<img src="./docs/management-applications-step-3.png?raw=true" width="100%" alt="applications step 3"/>

Double-clicking on an application shows more information.

<img src="./docs/management-applications-single-view.png?raw=true" width="100%" alt="single application view"/>

### Files and certificates

List of files and certificates. Can also extract archive (currently only .zip is supported).

<img src="./docs/management-files-and-certificates-view.png?raw=true" width="100%" alt="files and certificates view"/>

Example of adding a file.

<img src="./docs/management-files-and-certificates-step-1.png?raw=true" width="100%" alt="files and certificates step 1"/>

Double-clicking on a file shows more information.

<img src="./docs/management-files-and-certificates-single-view.png?raw=true" width="100%" alt="single file view"/>

### Business policy

List of business policies. A business policy is essentially a collection of 'configuration profiles', 'applications' and 'files'. Business policies be added to specific tags.

When devices have the same tag, the business policy would apply to the device - reflected in device info whether the device is compliant to the business policy or not.

When syncing a business policy, the 'configuration profiles', 'applications' and 'files' under it will be pushed down to the devices of matching tags.

Basically, this will be used to push configurations down to devices because the alternative is deploying 'configuration profiles', 'applications' and 'files' individually.

<img src="./docs/management-business-policies-view.png?raw=true" width="100%" alt="business policies view"/>

Example of adding a business policy.

<img src="./docs/management-business-policies-step-1.png?raw=true" width="100%" alt="business policies step 1"/>

Double-clicking on a business policy shows more information.

<img src="./docs/management-business-policies-single-view.png?raw=true" width="100%" alt="single business policy view"/>

### Patches

*(Have not explored.)*

### Action log

List of actions made to devices and by who or what. This is like an audit log trial.

<img src="./docs/management-action-log-view.png?raw=true" width="100%" alt="action log view"/>

## Company

### Users

List of users. Users can be added through the interface or through import from CSV or Microsoft Active Directory. Tags can also be added to users, not sure how this will affect business policies.

<img src="./docs/company-users-view.png?raw=true" width="100%" alt="users view"/>

Example of adding a user.

<img src="./docs/company-users-step-1.png?raw=true" width="100%" alt="users step 1"/>

Double-clicking on a user shows more information.

<img src="./docs/company-users-single-view.png?raw=true" width="100%" alt="single user view"/>

### Attributes

List of custom attributes which includes categories, attributes, locations, organizations, and tags. Attributes created can be added to business policies, users, devices, etc.

<img src="./docs/company-attributes-view.png?raw=true" width="100%" alt="attributes view"/>

Example of adding a custom attribute.

<img src="./docs/company-attributes-step-1.png?raw=true" width="100%" alt="attributes step 1"/>

Double-clicking on an attribute shows more information.

<img src="./docs/company-attributes-single-view.png?raw=true" width="100%" alt="single attribute view"/>

### Retired devices

*(Have not explored.)*

- [How to retire device](https://www.miradore.com/knowledge/getting-started/retiring-device/)

## System

### Permissions

List of users who can access the Miradore portal. Can set Admin, Editor or Reader. Invitations are through email.

<img src="./docs/system-permissions-view.png?raw=true" width="100%" alt="permissions view"/>

Example of inviting a user to access the Miradore portal.

<img src="./docs/system-permissions-step-1.png?raw=true" width="100%" alt="permissions step 1"/>

### Infrastructure diagram

Overview of infrastructure. This is where you can set up the 'Managed Google Play store', create API keys to use Miradore APIs, change self-enrollment settings, etc.

<img src="./docs/system-infrastructure-diagram-view.png?raw=true" width="100%" alt="infrastructure diagram view"/>

Example of Managed Google Play Enterprise settings (enroll/unenroll).

<img src="./docs/system-infrastructure-diagram-play-store-settings.png?raw=true" width="100%" alt="infrastructure diagram play store settings"/>

Example of API settings (API keys). API swagger can be found at:
- https://SITE_NAME.online.miradore.com/swagger/

<img src="./docs/system-infrastructure-diagram-api-settings.png?raw=true" width="100%" alt="infrastructure diagram api settings"/>

### Subscription

To subscribe. List of subscription history and billing history.
