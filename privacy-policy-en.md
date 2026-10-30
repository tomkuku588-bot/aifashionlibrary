# AI Costume Gallery Privacy Policy

- App name: AI Costume Gallery (AI服装库)
- Bundle name: com.xmgod.aifashionlibrary
- Version: 1.1.0
- Platform: HarmonyOS (API 26 / HarmonyOS 6.0.0(20)+), phone · tablet · 2in1
- Updated on: 2026-11-01
- Effective on: 2026-11-01
- Contact email: tomkuku588@gmail.com

Welcome to AI Costume Gallery (AI服装库). This policy applies to the HarmonyOS version of the app and explains how information is handled when you install and use it. The developer/operator is the entity publishing the app, as displayed on the AppGallery listing under the verified developer identity. The contact email is tomkuku588@gmail.com.

The app is a fully offline garment-entry browser and prompt-text assembler. It is free, ad-free, requires no registration, makes no network connections, and requests no system permissions. In one sentence: **it cannot reach anything beyond your device, and it cannot send anything out.**

## 1. What Information We Process and Why

The app does not collect, store, or upload any personal information. What we handle is limited to data you generate locally on your device and that is kept inside the app's private directory:

- **App settings**: interface language (中文 / English / 日本語), theme (system / light / dark), and consent state.
- **Closet favorites**: the garment entry numbers you favorite, notes you write yourself, and pin flags.
- **On-device usage history**: recently viewed entries, recent copies and search records, and tag usage counts.
- **Workshop drafts**: the tags, parameters, and manually edited prompt text currently selected in the prompt workshop.

These are processed only to implement local features: filtering and searching garment entries, assembling prompt text locally, closet favorites and notes, ordering frequently used tags, showing "recently viewed / recently copied", and preserving language and theme preferences. This data is not used to build a user profile and is not used for push, marketing, or personalization.

The current version provides no account registration or login and does not collect your phone number, email address, precise location, contacts, SMS, call logs, photo library contents, facial data, fingerprints, or similar personal information by default. Notes in the closet are written by you; please avoid recording other people's identifying information in them.

## 2. Storage Location, Retention, and Deletion

All of the above is stored on your device, inside the app sandbox's private directory, in a relational database and preferences files. It is not encrypted, is not uploaded to any developer server or external service, and the current version provides no cloud sync or cloud backup.

Retention depends on your own actions. You can remove the data by:

- unfavoriting entries or clearing search records in the app;
- withdrawing consent on the "Mine" page, which also clears on-device usage history and workshop drafts;
- clearing app data in system settings or uninstalling the app, which deletes all local data;
- resetting the device.

Because no server-side copy exists, such deletions are final and the app has no cloud capability to restore anything. If you use the export features to save look cards or prompt text to your album, another folder, or a third-party drive, that copy is controlled by you.

## 3. Permissions and System Capabilities

The app's `module.json5` declares no `requestPermissions` at all, which means it requests no system permissions, including network access; no network API is referenced anywhere in the project. Core features run completely offline and do not depend on network access.

Only two operations involve system capabilities, and both happen solely when you explicitly trigger them in the interface:

- **Saving a look card to your album**: uses the HarmonyOS `SaveButton` security control. The system grants write access to the album directory only for that single tap when you press the button yourself. The app does not request album permissions and never reads existing album contents. If you do not use this feature, the app has zero interaction with your album.
- **Exporting text or look files**: uses the HarmonyOS `DocumentViewPicker`, and the destination folder is chosen by you in the system picker; the write scope never exceeds the location you select.

Other than these capabilities, the current version does not read unrelated files in the background and does not collect personal information unrelated to garment browsing and prompt-text assembly. If a future version adds new permissions or system capabilities, we will explain them before the relevant feature is triggered and obtain authorization where required by law.

## 4. Sharing, Transfer, and Public Disclosure

We do not sell, rent, trade, or otherwise share your personal information with any third party, and we do not publicly disclose it without authorization. External transfer may occur only when you actively use features such as saving look cards, exporting files, or system sharing to move content out of the app; when required by laws, regulators, or courts; or when necessary to protect the personal or property safety of you, other users, or the public. In such cases, we will take reasonable protective measures within the scope permitted by law.

## 5. Third-Party SDKs, External Services, and AI-Generated Content

Apart from HarmonyOS base system capabilities, the app integrates no third-party SDKs for advertising, commercial analytics, social login, maps, payment, push notifications, or crash reporting; the project's third-party dependency list is empty. The app also uploads none of your favorites, notes, search records, or settings to any developer-operated server or external service.

**The app does not provide any AI generation or synthesis service.** The prompt workshop performs retrieval and template assembly under fixed rules: the same tag selection always yields the same text, no local or cloud model is called at runtime, no image, audio, or video is produced, and there is no random or probabilistic synthesis. Therefore the "generation and synthesis" case regulated by the *Measures for the Labeling of AI-Generated Synthetic Content* does not apply to this app, and the text you see in the app is not AI-generated synthetic content. Any image you obtain from a third-party drawing tool using that text is subject to that tool's and your own labeling obligations, not to this app.

If a future version introduces network services, AI services, or other third-party services, we will update this policy, change the version number, ask for your consent again on the next app launch, and, where necessary, obtain explicit consent through notices, dialogs, or system authorization flows.

## 6. Bundled Content and Third-Party Assets

The app ships 600 garment entries, 126 tags, and trilingual (Chinese / English / Japanese) texts written independently by the developer. The bundled garment reference photos (a seasonal and party subset) remain the property of the original site, whose terms prohibit redistribution; they are included only to display garments, the app claims no rights in them and does not sublicense them, and entries with no matching image or a decode failure fall back to code-drawn vector silhouettes. The filtering and search interaction model references the open-source project `Brilliant666/ai-costume-gallery-cn` (code under the MIT license, Chinese translation under CC BY 4.0); the app credits it on the "About" page and in the bundled `notice.md`.

This section concerns the app's deliverables and intellectual property; it does not involve any processing of your personal information.

## 7. Data Security

The app uses fully local processing and a zero-permission design, which removes the data-exfiltration path by architecture, and follows the minimum-necessary principle by writing only what the features require. Please understand that no technical measure can guarantee absolute security: the local database and preferences files are not additionally encrypted, so anyone with physical access to your device or to a copy of the app's data could read the local contents described above. You remain responsible for the security of your device, system accounts, and any look cards or text files you export.

## 8. Your Rights

You can view, correct, supplement, or delete closet favorites, notes, search records, and workshop drafts in the app, clear local data, or uninstall the app to remove all information; withdrawing consent on the "Mine" page also clears on-device usage history and drafts. Because the current version has no online account system, rights of access, correction, deletion, and withdrawal can all be exercised locally without sending us a request. If you still have questions about this policy, data handling, or permission use, you may contact us through the email provided above.

## 9. Minors

The app's content is for all ages, contains no adult material (age rating 3+), and shows no violence, pornography, or inappropriate content. The bundled reference images are faceless invisible mannequins or floating garments, and the vector fallbacks are flat garments, with no faces and no nudity. The app has no account system, no social features, and no in-app purchases, and submits no data to any service, so it is suitable for minors to use with parental awareness.

If you are under the age of 14, you should use the app only after your parent or legal guardian has read and agreed to this policy. We do not knowingly conduct targeted marketing toward minors or intentionally collect personal information from minors that is unrelated to the app's functions.

## 10. Updates and Contact

If there is a material change to product features, processing purposes, data types, permission use, or applicable rules, we will update this policy, change the version number, and ask for your consent again the next time the app starts; continued use means you accept the updated version. You can read the full text of the version currently in force on the "Mine" page in the app, which matches this page.

You may contact us at tomkuku588@gmail.com, or visit this repository at https://github.com/tomkuku588-bot/aifashionlibrary.
