---
icon: circle-question
---

# FAQ

### Does the Butter Box give me the internet?

Not quite. The Butter Box doesn’t provide internet access. Instead, it creates its own local Wi-Fi network that lets you access apps, content (previously set up), and message board features offline . Everything is stored and shared locally — no internet or data connection needed.

***

### How do you power a Butter Box?

The Butter Box is super flexible! You can power it using a USB power bank, a wall adapter, or even a small solar panel. As long as it provides power to the Raspberry Pi, you’re good to go. Go to the [Power Supply](build-a-box/power-supply.md) section to learn more.

***

### If I’m powering the Butter Box with a solar panel, do I need a power bank?

A power bank isn’t strictly required, but it’s highly recommended. Solar panels can be inconsistent — clouds, shade, or changing sunlight can interrupt power. A power bank helps smooth that out by storing energy and keeping the Butter Box running steadily, even when sunlight dips. Check it out this use case to know more: (insert use case URL)

***

### What are the security features of the Butter Box? Can I put a password on it?

Currently, the Butter Box broadcasts an open Wi-Fi network — that means no password is required to connect. This makes it easy for people nearby to join, especially in offline or community settings.

However, users must either enter the Butter Box’s local IP address manually, or scan a QR code that takes them directly to the content. Since it’s all offline, there’s no exposure to the internet or external threats.

You can configure the Raspberry Pi to require a Wi-Fi password if you want more control. It’s not enabled by default, but it’s totally doable for more secure environments. Check out the [Security](/broken/pages/euE9z9Dog2t9F4QA9ESs) section for more information.

***

### How much storage does a Butter Box have?

The Butter Box storage capacity is defined by the microSD card you install — it doesn’t have fixed built-in memory. You can choose anything from a 16 GB card up to 1 TB (the Raspberry Pi Zero 2 W supports microSD sizes up to that). We recommend 256 GB.

| Use Case                              | Suggested micro SD Size    |
| ------------------------------------- | -------------------------- |
| Basic setup (apps + message board)    | 16 GB – 32 GB              |
| Additional content or media storage   | 64 GB – 128 GB             |
| Handling large content packs or files | 256 GB or more, up to 1 TB |

***

### Can I customize it?

Absolutely! You can add, for example, your own content - dropping in PDFs, videos, images, and HTML pages to build a local library, or add your own apps - including Android APKs (even if they’re not on F-Droid).
