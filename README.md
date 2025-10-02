# GTM Click IDs Manager

**Click IDs Manager** is a versatile and privacy-conscious Google Tag Manager (GTM) **web tag template** that captures, stores, and manages marketing **click identifiers** such as `gclid`, `fbclid`, `ttclid`, and any **custom URL parameters**. It helps advertisers, analysts, and marketers track both **first-click** and **last-click attribution** events across web sessions and user journeys.

Developed by **Jonah Tochukwu Onyejekwe**, the tag template ensures flexibility, reliability, and compliance by offering configurable storage options and dataLayer integration without writing any custom code.

---

## 🚀 Key Features

- 🔐 Supports both **first-click** and **last-click** identifier tracking.
- 🍪 Stores identifiers in either **separate cookies** or a **single object cookie**.
- 🧠 Uses **localStorage** as a backup and for cookie recovery.
- 🧪 Integrates seamlessly with the **GTM dataLayer** for downstream tagging and analytics.
- 🛠️ Fully configurable with support for **custom identifier parameters**.
- 🔄 Option to **refresh** cookie lifespan on each page load.
- 🧱 Built to work within GTM’s secure **Sandboxed JavaScript** environment.
- 🧬 Developed with flexibility to support custom naming conventions and storage separation.
- ⚖️ Licensed under the **Apache 2.0 License**.

---

## 🧰 Use Case Examples

Use this tag template when you want to:

- Capture marketing click identifiers (e.g., `gclid`, `fbclid`, `ttclid`) from URLs for attribution.
- Store both first-click and last-click values for campaign effectiveness tracking.
- Push identifiers into the `dataLayer` for use with Google Ads, Facebook Pixel, or analytics tools.
- Recover expired cookies using persistent localStorage backup.
- Persist identifiers across sessions and refresh them on new visits.
- Store custom identifiers from affiliate networks, partner referrals, or UTM alternatives.

---

## 📥 Download & Import

To get started:

1. **Download the template file**:
   - Click on the [Releases](https://github.com/YOUR_USERNAME/gtm-click-ids-manager/releases) section of this repository.
   - Download the latest `.tpl` file.

2. **Import into your GTM container**:
   - Go to your **Web GTM container**.
   - Navigate to **Templates**.
   - Click **"New"** under **Tag Templates**.
   - Use the vertical 3-dot menu (⋮) and choose **"Import"**.
   - Upload the `.tpl` file you downloaded.
   - Save the template.

---

## ⚙️ Configuration

When adding the tag to a GTM trigger, configure the following fields:

### ✅ Identifier Settings
- **Enable GCLID**, **FBCLID**, **TTCLID**, etc.: Select the built-in identifiers you want to capture.
- **Use Custom Click Identifiers**: Enable if you want to capture additional URL parameters.
- **Custom Identifiers Table**:
  - `URL Parameter Name`: The name of the custom identifier to capture (e.g., `affid`, `partner_id`).

### ✅ Storage Configuration
- **Storage Type**: Choose between:
  - `Separate Cookies`: One cookie per identifier.
  - `Single Object Cookie`: All identifiers stored together.
- **Use Custom Cookie Prefix**: Customize the prefix for cookies when using separate mode.
- **Cookie Domain / Path**: Define optional scope for cookie storage.
- **Cookie Lifespan / Unit**: Set how long cookies should persist.

### ✅ LocalStorage Support
- **Enable LocalStorage**: Stores and retrieves identifiers from persistent localStorage.
- **Use LocalStorage to Restore Expired Cookies**: Automatically recovers missing cookies when localStorage is still valid.

### ✅ First Click Identifier Settings
- **Enable First Click Tracking**: Only sets values if neither cookie nor localStorage already has it.
- **First Click Storage Type**: Choose between separate or single cookie.
- **Custom Prefix or Cookie Name**: Optional overrides for naming.

### ✅ dataLayer Integration
- **Push to dataLayer**: Enable to make identifiers available for triggers, tags, or reporting.
- **Custom Event Name** (optional): Set your own event name or use the default `gtm_dd_click_identifier_data`.

---

## 🧪 Example Scenarios

| Scenario | Behavior |
|---------|----------|
| A user lands on your page with `?gclid=XYZ` | The `gclid` is stored as last-click and first-click (if applicable). |
| Cookie expires but `localStorage` still has the value | The value is restored into a new cookie. |
| A custom click ID like `affid=12345` is present | If configured, it will be captured, stored, and pushed to dataLayer. |
| A user returns without any click ID | Existing cookie/localStorage values are reused, no new overwrite. |
| A click identifier is not in URL, cookie, or localStorage | It is ignored entirely (no “deleted” value is recorded). |

---

## 👤 Author

**Jonah Tochukwu Onyejekwe**  
Creator of [DumbData](https://dumbdata.co/)  
Focused on making powerful GTM tooling for modern marketers and analysts.

---

## 📄 License

This project is licensed under the **Apache License 2.0**.  
You are free to use, modify, and distribute it under the terms outlined in the [LICENSE](./LICENSE) file.

---

## 🙌 Feedback & Contributions

Have a suggestion, spotted a bug, or want to improve the template?  
Open an issue or submit a pull request. Contributions are welcome!

