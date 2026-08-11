# Boson Terms of Use

**Effective Date:** August 11, 2026

**Contact:** soap.official@outlook.com

These Terms of Use govern your access to and use of the Boson desktop, iOS, and Android applications and their related cloud synchronization services. By creating an account or using Boson, you agree to these Terms.

## 1. Operator and Agreement

Boson is operated by Jacob Jennette ("Boson," "we," "us," or "our"). These Terms form an agreement between you and Boson. If you do not agree to them, do not create an account or use Boson.

## 2. Eligibility and Accounts

You must be legally able to enter into this agreement and at least 18 years old, or the age of legal majority where you live. You must provide accurate account information, protect your password and devices, and promptly notify us if you believe your account has been compromised.

You are responsible for activity performed through your account and for ensuring that anyone whose information you enter into Boson has been handled in accordance with applicable law and your own obligations.

If you generate an employee key, you are responsible for assigning it only to an authorized person, selecting appropriate permissions, providing that person's correct email address for direct delivery, reviewing its activity, and regenerating or revoking it when access should change or end. A person using an employee key must protect it and use only the access authorized by the business owner. An employee may use a key without an account and activate keys for multiple businesses on one device, or link a key to a normal Boson account to save that business in the account's workspace switcher. Remembering or linking access does not transfer ownership or broaden permissions, and each workspace remains subject to its independently issued key, regeneration, revocation, plan invalidation, and current permission group.

If you explicitly remember a normal account or activate an accountless employee key, Boson stores that profile's Supabase refresh token and limited display/routing metadata in OS-protected encrypted storage on that device. It does not store the access token, readable employee key, temporary employee-authentication password, or account password in the remembered-access vault. Remembered profiles are device-specific, are not synchronized to Boson Cloud, and are excluded from every `.bosonbackup`. The Activated Keys control appears only on the signed-out login screen and only when at least one key profile is remembered; there is no in-app Switch Access action. Accountless Activated Keys require an internet connection and authoritative revalidation before opening a workspace; they receive no trusted-device offline grant. For a remembered profile, Manual Sign Out clears the app's current sign-in state and automatic-reopen marker on that device while preserving its encrypted saved profile and refresh credential for later login-screen use; it does not invoke provider logout or revoke the retained refresh credential. A session without a remembered profile uses normal provider sign-out. Remove From This Device deletes only that profile from the current device and does not revoke, regenerate, or delete the employee key in Boson Cloud; only the business owner controls those backend key actions. You are responsible for securing the device and promptly signing out, removing saved access from devices you no longer control, or asking the business owner to revoke or regenerate a key when access should end.

## 3. The Boson Service

Boson provides local-first tools for viewing an all-in-one financial portfolio. You may create business trackers for sales, expenses, inventory, clients, services, invoices, reporting, permission groups, employee keys, and an employee activity and data-change audit journal; personal-finance trackers for manually entered or imported income, expenses, and transfers; and read-only crypto trackers for one automatically recognized public Bitcoin mainnet, Solana mainnet, or EVM address. A 0x address is checked across Ethereum Mainnet, Base, OP Mainnet, Arbitrum One, and Polygon. Existing records that explicitly identify one EVM network retain that network; older records with no saved network remain assigned to Base. Authenticated account and business records may synchronize automatically through Boson Cloud when a connection is available. Portfolio summaries and charts may combine recorded cash flow with valuation changes, so a displayed 24-hour crypto gain or loss may reflect public market-price movement even when no on-chain transfer occurred.

The owner-account Appointments workspace lets you schedule, describe, link, reschedule, and remove appointments; review completed and not-completed outcomes for up to 90 days after an occurrence; add supported PDF, image, text, CSV/TSV, DOCX, XLSX, and PPTX files; and optionally request reminder emails for the recipient addresses you provide. Appointment files are limited to 5 MiB each, 10 files and 20 MiB per appointment, and 100 MiB per account. Validation and type checks reduce risk but do not guarantee that a file is safe, accurate, or free of malicious content, so you remain responsible for files you open or share. Include Files is optional and off by default. Validated PNG, JPEG, WebP, and TXT sets up to 10 MiB may be attached directly; other supported types and larger sets use protected, expiring Waylith download links. An attachment cannot be recalled after the email provider accepts it, while a protected link may later expire or be revoked. A past appointment may be marked complete, which removes it from the active list. An uncompleted appointment is automatically removed from the active list three days after its scheduled occurrence unless you move it to a future time before then. Appointment History content is deleted no later than 90 days after the scheduled occurrence; minimal deletion/synchronization metadata may remain solely to prevent a stale device from restoring removed content. Reminder timing, inbox placement, and delivery are best-effort: a message may be delayed, filtered, or not delivered because of provider availability, invalid recipient information, delivery limits, rescheduling near the reminder time, or other service conditions.

Personal-finance and crypto tracker profiles, transaction records, import provenance, public addresses, public activity, and balance observations use a separate owner-only account namespace and synchronize through Boson Cloud when a connection is available. Cloud records are stored as ordinary JSON/JSONB and are not end-to-end encrypted from Boson, Supabase, or sufficiently privileged infrastructure administrators. Reproducible public market-price history is fetched when a Crypto overview opens, remains only in temporary app memory for that session, and is not written to device storage, Boson Cloud, or backups. A cold offline launch therefore cannot rebuild a Crypto price or fiat-balance chart, while a chart already loaded in the open app may remain available if the connection drops. CSV, TSV, delimiter-separated text, and XLSX transaction-data files selected for an import are parsed on the device. Boson does not upload or retain the source file as part of the import. The transaction records, classifications, and provenance created by an import remain in the applicable Business or General Purpose tracker. XML and PDF import are not currently supported.

Crypto tracking is read-only. Boson sends the public address and read-only query parameters to the applicable Blockscout, Blockstream, or Solana public endpoint, and may request public Bitcoin or Solana spot prices from Coinbase. Boson never asks for or uses a private key, seed phrase, extended wallet key, wallet approval, or signing credential, and this implementation does not connect to a Coinbase account. Checks are scheduled only while Boson is open and able to run, no more than once per 60 seconds per tracker; Boson does not monitor or refresh wallets while closed or suspended. A Bitcoin wallet may create multiple receiving addresses, and Boson tracks only the exact address entered rather than an entire wallet. A tracker name or its presence in your portfolio does not prove that you own, control, or are associated with the address.

Boson is an evolving prerelease product. Features may change, be interrupted, contain errors, or be discontinued. You should maintain appropriate independent records and backups for your financial information.

Boson's secure backup library is stored on each device rather than as backup history in Boson Cloud. Automatic backup is enabled by default per business, runs when the app is available at or after the device's 3:00 AM schedule, and deletes automatic entries after seven days. Manual and pre-restore entries do not expire automatically, but local entries are not guaranteed to survive device loss, app removal, storage reset, corruption, or other failure; export and independently protect backups you need to retain. A complete-account backup includes General Purpose and Crypto tracker data, active Appointments, and eligible Appointment History, while a single-business backup does not. Appointment file contents and Boson's server-controlled attachment, reminder, delivery, and deletion projections are excluded from every `.bosonbackup`; restoring a backup therefore does not recreate, roll back, or recover appointment files or delivery evidence. A current cloud file can remain associated if its same appointment record ID survives the restore, but a file already deleted or cleaned from Storage cannot be recovered from the backup. A confirmed restore is destructive for the data represented by that backup and the restored cloud generation supersedes older device state. For compatibility and data-loss prevention, an older complete-account backup without a versioned tracker, Appointments, or Appointment History section preserves the account's newer data for that feature instead of deleting it. Restoring an Appointments section preserves its reminder configuration but pauses those restored reminders because the backup contains no service-side delivery history. To resume delivery, change the occurrence, time zone, or reminder lead time; alternatively, save the reminder disabled and enable it in a later edit. A details-only or recipient-only edit does not resume delivery. Permanently deleting the account removes its backup encryption key and prevents Boson from restoring those backup payloads.

## 4. No Accounting, Tax, Legal, or Financial Advice

Boson is an organizational tool and is not a certified accounting, tax-filing, legal, payroll, banking, investment, or financial-advice service. Reports, calculations, exchange-rate conversions, crypto prices, tracked wallet values, provider labels, invoices, and reminders may be delayed, incomplete, or inaccurate and must be independently reviewed before you rely on them for business, tax, legal, investment, or financial decisions. A displayed tracked value is an estimate, not proof of ownership, custody, liquidity, or the amount that could be sold or transferred.

## 5. Your Content and Data

You retain ownership of the information and content you enter into Boson. You grant Boson and its service providers a limited right to host, copy, transmit, process, and display that content only as needed to operate, secure, and support the service and to comply with law.

You represent that you have the rights and permissions needed to enter, process, and synchronize your content, including personal information about clients, staff, or other individuals. Our Privacy Policy explains how information is handled.

When you add a public wallet address, you are responsible for using the public information lawfully and for choosing a tracker name that does not falsely claim ownership or association. Public availability does not authorize harassment, unlawful profiling, discrimination, fraud, or violation of another person's rights.

The business owner controls employee permission groups and may regenerate, revoke, or delete a backend key or request conflict-safe reversal of data changes attributed to it. Successful regeneration invalidates the prior credential and emails a replacement to the employee address on file. Revocation invalidates the credential and stops future Boson Cloud access; a remembered profile that no longer passes online revalidation becomes unusable and is removed from that device's activated list. Removing the saved profile from a login screen is a separate device-local action and never changes the backend key. Neither backend action can remotely erase business records already cached on an employee-controlled device. Undo cannot retract an email already sent or overwrite a record that has since been changed by someone else.

When you direct Boson to email an employee key, invoice, or appointment reminder, you represent that the recipient is the authorized employee, your client, attendee, or another person who expects the applicable communication; that the recipient, appointment, employee, business, and Reply-To information is accurate; and that the message complies with applicable email, consumer-protection, privacy, and anti-spam requirements.

## 6. Acceptable Use

You may not use Boson to:

- Violate a law, regulation, court order, contract, intellectual-property right, privacy right, or other legal right.
- Upload malicious code, interfere with the service, probe or bypass security, or attempt unauthorized access to accounts, systems, or data.
- Share, redeem, or use an employee key outside the business access and permissions authorized by its owner.
- Misrepresent your identity, impersonate another person, facilitate fraud, or use Boson for unlawful, abusive, or harmful activity.
- Use public wallet tracking to harass, threaten, unlawfully profile, discriminate against, defraud, or falsely claim an association with another person.
- Reverse engineer, scrape, resell, sublicense, or commercially exploit the service except where applicable law expressly permits it.
- Use automated means in a way that places unreasonable load on Boson or its providers.
- Send unsolicited, deceptive, harassing, or unlawful invoices or appointment reminders, bypass delivery limits, or use invoice or appointment-reminder delivery as a bulk-email service.

## 7. Third-Party Services and Platforms

Boson relies on third-party services, including Supabase for authentication and cloud data services; Resend for transactional account, employee-access, support, invoice, and appointment-reminder email; Stripe for subscriptions started through Waylith; Apple for iOS distribution, TestFlight, and subscriptions started through the iOS app; Frankfurter for exchange-rate information; Blockscout's public explorer API instances for read-only EVM balances and activity on Ethereum Mainnet, Base, OP Mainnet, Arbitrum One, and Polygon; Blockstream's public API for exact-address Bitcoin balances and activity; Solana's public mainnet RPC and PublicNode's public Solana RPC for exact-address SOL balances and activity; Coinbase's unauthenticated public endpoint for available Bitcoin and Solana spot prices; and IPWhois.io for owner-IP-based time-zone detection. Their availability, data, and terms may affect Boson. We are not responsible for third-party services that we do not control.

For the iOS app, Apple's applicable App Store or TestFlight terms and the Apple Standard Licensed Application End User License Agreement may also apply. Apple is not responsible for providing Boson support except as required by applicable platform terms or law.

## 8. Plans, Fees, Renewal, and Cancellation

Boson offers Free, Suite, Executive, and individually arranged Custom access. Suite and Executive may be offered as automatically renewing monthly or annual subscriptions. The applicable plan, billing period, full price, currency, taxes if applicable, and renewal terms are shown before purchase. Prices and plan contents may change prospectively; a price change does not apply except as permitted by the billing provider and applicable law.

If you subscribe in the iOS app, payment is charged to your Apple Account when Apple confirms the purchase. The subscription automatically renews unless you cancel through Apple at least 24 hours before the current period ends. Apple may charge the renewal within 24 hours before that end. You can restore eligible Apple purchases or open Apple's subscription-management screen from Boson. Apple handles Apple purchase processing, cancellation, and refund requests under Apple's applicable terms.

If you subscribe through Waylith, Stripe processes the payment and the Waylith billing portal provides the available subscription-management options. Canceling automatic renewal ordinarily leaves paid access active through the already-paid period; it does not retroactively refund that period. Any different refund, trial, promotional, or Custom-plan term must be presented in writing.

Boson uses an account-level billing-channel check intended to prevent starting both an Apple and Waylith subscription for the same Boson account. A canceled subscription can continue to block the other channel until its paid-through period ends. If provider delays, a purchase made outside the normal flow, or another error results in overlapping subscriptions, contact support promptly; Boson will preserve verified access while the billing state is reviewed, but it cannot itself reverse an Apple or Stripe charge.

Paid plan access follows the verified Boson account across supported platforms. If a paid subscription expires, is revoked, or is refunded, the account returns to the applicable lower plan after any paid-through or provider-authorized grace period. Existing records are not deleted merely because plan access changes, although higher-plan actions and capacity may become unavailable. Deleting the Boson account does not by itself cancel a subscription with Apple or Stripe; cancel the subscription with its billing provider first.

We may update the service or these Terms as Boson develops. The effective date identifies the current version.

## 9. Suspension, Termination, and Deletion

You may stop using Boson at any time and can permanently delete your account from Account Settings. We may suspend or terminate access when reasonably necessary to protect Boson, users, third parties, or the public; respond to legal requirements; address nonpayment; or enforce these Terms.

Sections that by their nature should survive termination—including ownership, disclaimers, liability limits, and dispute provisions—will continue to apply.

## 10. Disclaimers

To the fullest extent permitted by law, Boson is provided "as is" and "as available," without warranties of merchantability, fitness for a particular purpose, title, noninfringement, uninterrupted availability, data preservation, or error-free operation. Some jurisdictions do not allow certain warranty exclusions, so some of these exclusions may not apply to you.

## 11. Limitation of Liability

To the fullest extent permitted by law, Boson and its operator will not be liable for indirect, incidental, special, consequential, exemplary, or punitive damages, or for loss of profits, revenue, goodwill, data, or business opportunity arising from or related to Boson. Where liability cannot be excluded, total liability will not exceed the greater of the amount you paid for Boson during the twelve months before the event giving rise to the claim or 50 U.S. dollars. These limits do not apply where prohibited by law.

## 12. General Terms and Contact

If any provision is unenforceable, the remaining provisions remain in effect. A failure to enforce a provision is not a waiver. You may not transfer this agreement without our consent; we may transfer it as part of a reorganization, financing, sale, or transfer of Boson. These Terms and the Privacy Policy are the entire agreement concerning the service unless additional written terms apply.

Questions about these Terms may be sent to **soap.official@outlook.com**.
