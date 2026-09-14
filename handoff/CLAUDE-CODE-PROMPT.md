# Hand this to Claude Code

Two ways to get option 1a exactly:

## A. Easiest — give it the finished code
This folder already IS option 1a as plain HTML/CSS:

    handoff/index.html
    handoff/assets/lockup-white.png   (white OASIS lockup, transparent bg)
    handoff/assets/mark-white.png     (white window mark only, transparent bg)

Tell Claude Code:
> Use handoff/index.html as-is. Do not restyle it. Only replace BUTTON_1_TEXT / BUTTON_1_URL,
> BUTTON_2_TEXT / BUTTON_2_URL, BUTTON_3_TEXT / BUTTON_3_URL and the LOCATION_n_AREA lines
> with the real names, Google Maps links and area names below. Keep everything else identical.

## B. If it must rebuild from a description, paste this spec
> Build a single-page mobile-first QR landing page for OASIS ALUMINIUM. Plain HTML + CSS,
> no frameworks, no JS, no animation libraries.
>
> Colours: page background solid #312782 (deep indigo). Accent #35A8E0 (sky blue).
> Secondary text #C6C6C5. Primary text #FFFFFF. No gradients. Exactly one accent colour —
> ALL THREE BUTTONS MUST BE IDENTICAL IN COLOUR.
>
> Type: Poppins (Google Fonts), weights 400/600 only.
>
> Layout: single centred column, max-width 420px, padding 56px 24px 32px, full viewport height
> (use min-height:100dvh), flex column.
> 1. White OASIS lockup PNG on transparent background, 148px wide, centred.
> 2. 40x3px rounded bar in #35A8E0, centred, 22px below the logo.
> 3. Tagline "Choose a location to get directions": 15px, #C6C6C5, centred, max-width 250px.
> 4. 44px gap, then three <a> cards stacked with 14px gap:
>    - background rgba(255,255,255,.08), 1px border rgba(255,255,255,.20), border-radius 18px,
>      padding 20px, min-height 64px, display:flex, align-items:center, gap 16px.
>    - left: 22px-wide white window mark PNG at .9 opacity.
>    - middle: title 17px/600 #FFFFFF, sub-label 13px #C6C6C5, 3px gap, flex:1, min-width:0.
>    - right: 34px circle filled #35A8E0 containing a CSS chevron (8x8 box, 2px white
>      border-top + border-right, rotated 45deg).
>    - hover/focus: background rgba(255,255,255,.16), border-color #35A8E0, .15s transition.
>      No transform, no shadow animation.
> 5. Flex spacer, then footer "OASIS ALUMINIUM": 12px, uppercase, letter-spacing .1em,
>    rgba(255,255,255,.5), centred, 36px top padding.
>
> Placeholders: BUTTON_1_TEXT/BUTTON_1_URL, BUTTON_2_TEXT/BUTTON_2_URL,
> BUTTON_3_TEXT/BUTTON_3_URL, and LOCATION_1_AREA/2/3 for the sub-labels.
> Desktop: same column, just centred horizontally — do not add a wide desktop layout.
