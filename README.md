# Dharma Tower Website

Ye ek static website hai (sirf `index.html`), isliye GitHub Pages par free host hoti hai.

## 1. GitHub par online karna
1. github.com par login karein, **New repository** dabayein. Naam rakhein `dharma-tower`, **Public** chunein, Create dabayein.
2. **Add file > Upload files** se `index.html` upload karein (photos baad mein section 3 se jodein), phir **Commit changes** dabayein.
3. **Settings > Pages** kholein. "Build and deployment" mein Source: **Deploy from a branch**, Branch: **main**, folder: **/(root)**, phir **Save**.
4. 1-2 minute baad site yahan khulegi: `https://AAPKA-USERNAME.github.io/dharma-tower/`

Phone se upload mushkil ho to Chrome mein "Desktop site" on karein, ya laptop use karein.

## 2. Details badalna (phone, address, flats)
GitHub mein `index.html` kholein, pencil (Edit) icon dabayein aur file ke upar ke 2 hisse badlein, phir **Commit changes**:
- `CONFIG`: phone, phoneDisplay, whatsapp, address, hours, mapEmbedUrl, endpoint
  - phone: `"+919999999999"` (country code ke saath), whatsapp: `"919999999999"`
  - jab tak ye khaali hain, site mein "To be confirmed" dikhta hai.
- `FLATS`: har flat ka id, type, rent, deposit, items. Jab management availability confirm kare tabhi `verified:true` karein. Flat hatane ke liye uski poori `{...}` line delete karein.

## 3. Photos badalna
1. **Add file > Upload files** se photos upload karein; unka naam `images/...` rakhne ke liye pehle **Create new file** mein `images/x.txt` naam likhkar folder banayein, ya photos seedha repo mein daalkar path `photo.jpg` use karein (chhoti rakhein, 250 KB ke aas-paas, `.jpg` ya `.webp`).
2. Flat ke liye: `photos:["images/a1-living.jpg","images/a1-bedroom.jpg"]`
3. Gallery ke liye: `{k:"living",l:"Living room",src:"images/living.jpg"}`

## 4. Enquiries sach mein receive karna
GitHub Pages sirf static hosting hai, isliye form ke liye alag service chahiye. Sabse aasaan: **Formspree** (free).
1. formspree.io par account banayein, **New form** banayein.
2. Mila hua link (jaise `https://formspree.io/f/abcdwxyz`) `CONFIG.endpoint` mein daal dein.
3. Ab har enquiry aapke email par aayegi, aur Formspree dashboard mein bhi dikhegi.

Jab tak `endpoint` khaali hai, form "Not sent" dikhata hai aur kuch bhejta nahi. Booking confirm karna abhi phone/WhatsApp se manually hoga. Online payment ya auto-booking is website mein nahi hai.

## Dhyan rakhein
- Repository public hai, isliye usme koi password ya secret key kabhi na daalein. Formspree ka form link public hota hai, wo theek hai.
- Privacy Policy aur Terms ka text placeholder hai, use sahi text se badalwa lein.
