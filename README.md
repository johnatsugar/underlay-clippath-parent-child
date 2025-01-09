**underlay-clippath-parent-child**
Implement clip-path from iframe or child

**underlay-clippath-single**
underlay test with css clip-path


**BACKGROUND:**
This project began as a personal experiment to enhance a custom build for the [Gold Peak Takeover campaign in September 2023](https://hymnal.voxmedia.com/ads/114908/). The goal was to create a parallax-like visual effect by displaying an image beneath the parent site’s background, while making only the ad’s background transparent. This effect mimics a scroll reveal, offering a dynamic and immersive experience. A sample [test page](https://tinyurl.com/23ktkpum) showcases the initial concept. The experiment gained attention during the 2024 Product Summit, leading to its evolution into a potential new ad product.

**CHALLENGES:**
The primary obstacle was scaling the effect across all O&O sites. Customizing each homepage and subpage with their unique layouts, div structures, and CSS classes was infeasible.

**OBJECTIVE:**
Develop mobile and desktop-friendly underlay templates using Hymnal that align with global branding standards.

----------------------------------------------------------------------

**PROPOSED SOLUTIONS**

**SOLUTION I: Embedding the Image in the Hymnal SafeFrame/iFrame**
- Approach: Position the large background image within the Hymnal ad’s SafeFrame/iFrame, leveraging JavaScript to control scroll events and reposition the image.
- Issue: On mobile devices, the background image appeared jumpy due to frequent pixel recalculations, making the effect unstable.
 - [Test page](https://tinyurl.com/mws7s5ad)
 - [Hymnal build](https://hymnal.voxmedia.com/ads/130743/)
 - [GAM setting](https://tinyurl.com/ybwxzkpz)

**SOLUTION II: Original Implementation with Full Page Restyling**
Approach: Restore the ad effect by restyling entire pages.
Issue: While functional, this approach was time-intensive and unreliable, especially with dynamic content additions.
Examples:
- [Desktop-only Homepage](https://tinyurl.com/yk227rer) | [Hymnal](https://hymnal.voxmedia.com/ads/131324/)
- [Desktop-only Article](https://tinyurl.com/23ktkpum) | [Hymnal](https://hymnal.voxmedia.com/ads/131409/)
- [Desktop-only Features](https://tinyurl.com/57xp8zvt) | [Hymnal](https://hymnal.voxmedia.com/ads/131409/)
- [Mobile-only Features](https://tinyurl.com/npy9zuwj) | [Hymnal](https://hymnal.voxmedia.com/ads/131490/)
- [Mobile-only Article](https://tinyurl.com/yc2w495t) | [Hymnal](https://hymnal.voxmedia.com/ads/131490/)

**SOLUTION III: Using CSS Clip-Path**
Approach: Implement CSS clip-path to mask the underlay, repositioning the mask on scroll events.
Outcome: Works well on mobile and desktop, but the background image does not remain fixed to the parent window.
Examples:
- github: [underlay-clippath-parent-child](https://tinyurl.com/bdzkbecj)
- github: [2025-01-08-single-file-test](https://tinyurl.com/5n7muefv) scroll down the page
- github: [2025-01-09-parent-child-test](https://tinyurl.com/yknje8nc) scroll down the page
- And here is the [test page](https://tinyurl.com/hxe6jh3d) | [Hymnal](https://hymnal.voxmedia.com/ads/131544/)

**OTHER LINKS:**
- [Asana card](https://tinyurl.com/y5anfe6k)

----------------------------------------------------------------------

**SUMMARY:**
**GOOD NEWS** >>> clip-path provides a functional and scalable solution for both mobile and desktop platforms.
**BAD NEWS** >>> The background image currently moves away from the parent window, causing visual misalignment.

----------------------------------------------------------------------

NEXT STEPS:
We need assistance to:
- 1. Fix the background image, ensuring it remains fixed or sticky relative to the parent window.
- 2. Refine the mask's position to maintain alignment with the iframe window.

----------------------------------------------------------------------
_Last updated: 01/09/2025. 4PM_

