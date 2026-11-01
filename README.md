# Gowri Medicals — Premium static website

A polished, responsive, Telugu-first / English bilingual website for Gowri Medicals, Balaga Mettu, Srikakulam. Default theme is dark; users can switch to light.

## Included
- Premium responsive layout for desktop, tablet and mobile
- Telugu default with English toggle
- Dark default with light-theme toggle
- Mobile navigation and fixed Call / WhatsApp action bar
- Store information, services, contact details and address-based map
- WhatsApp order request form with name, mobile, locality, optional custom address, medicine details, delivery choice and urgent flag
- Optional customer-initiated current-location capture; includes a Google Maps coordinate link in the WhatsApp order message
- Optional selection of up to 3 JPG/PNG/PDF files (10 MB each; 20 MB combined)
- Native file-share handoff on supported browsers; WhatsApp text fallback otherwise
- Real shop photographs: daytime storefront in the homepage hero and illuminated nighttime storefront in a dedicated gallery section (optimised WebP assets)
- SEO metadata, social preview metadata, accessible labels and reduced-motion support
- No backend, database, analytics, tracking, paid API or file storage

## Deploy on Cloudflare Pages (static, no build)
1. Extract the ZIP.
2. Push the contents of this folder (including `assets/favicon.svg`) to the root of a GitHub repository.
3. In Cloudflare Dashboard, open **Workers & Pages → Create → Pages → Connect to Git**.
4. Select the repository.
5. For a plain static site, use no build command and set the output directory to `/` (repository root). If the UI requires a build command, use an empty/no-op setting supported by the dashboard.
6. Deploy. Test the generated `*.pages.dev` HTTPS URL on both desktop and mobile.

You can also use Cloudflare Pages direct upload if preferred. Keep the files at the published root so `index.html` is served as the home page.

## WhatsApp and prescription sharing — important
- Primary WhatsApp is configured as `+91 99891 05144` (`919989105144`).
- The alternate number `+91 99853 58726` is a tap-to-call link only; its WhatsApp registration was not independently confirmed.
- `wa.me` click-to-chat supports prefilled text, not attaching a file automatically.
- On browsers that support Web Share API file sharing, the site opens the device share sheet with the selected file(s) and order text. The customer chooses WhatsApp if offered and presses Send.
- The share sheet cannot guarantee WhatsApp appears as a target on every phone/browser. On unsupported browsers, the site redirects to WhatsApp with the text and tells the customer to attach the prescription manually.
- The site does not upload, transmit to its own server, or retain selected files.
- Current location is requested only after the customer taps the location button. Coordinates are held in page memory and included in the WhatsApp message as a Google Maps link; no reverse-geocoding service or location database is used. File sharing is initiated by the customer from their device.
- Opening WhatsApp or the share sheet is not proof that an order was sent or accepted. The customer must press Send; the pharmacy must confirm availability and order details.

## Business information used
The following details were transcribed from the supplied Gowri Medicals reference material and should be confirmed by the shop owner before public launch:
- Name: Gowri Medicals (గౌరి మెడికల్స్), Chemist & Druggist
- Address: Balaga Mettu Main Road, Srikakulam, Andhra Pradesh – 532001
- Main phone / WhatsApp: +91 99891 05144
- Alternate phone: +91 99853 58726
- Store hours: 7:30 AM–10:30 PM, 7 days a week (confirm current hours)
- Delivery and pickup are described in the reference material; confirm current service area and availability.
- Localities listed in the order form are suggested area choices from the reference material, not a guarantee that delivery is available in every locality.
- The embedded map and directions button perform an address-based Google Maps search. They do not claim to identify a verified storefront pin.

Third-party directory results found for a different "Gowri Medicals" in Sompeta, Srikakulam district; they do not corroborate this Balaga Mettu store. Do not use those conflicting directory details as the store's address or phone.

## Before launch — owner checklist
- Confirm both phone numbers and that the primary number receives WhatsApp messages.
- Confirm exact address, map pin, opening hours and delivery localities.
- Test the order form on Android Chrome and iPhone Safari over HTTPS, including location permission allow/deny and GPS-off cases.
- Test file handoff using actual JPG, PNG and PDF prescription samples. Ensure the intended WhatsApp account is offered by the device share sheet.
- Review the supplied real storefront photographs and confirm they are suitable for public display. The website uses the supplied originals converted to optimised WebP; no generated image is presented as a real storefront photo.
- Check that the WhatsApp message looks correct and that the customer can edit it before sending.

## Privacy and medical safety
Prescription images can contain sensitive health information. This site does not store them. Customers decide whether to share files with the pharmacy through their device's share menu. The pharmacy should restrict access to received prescriptions and retain them only as required for legitimate business and applicable law. The site does not diagnose, recommend medicines, or replace a clinician's advice.
