# დავალება 8 — ანალოგური საათის ანიმაცია

## აღწერა

ამ დავალების მიზანია  HTML-ისა და CSS-ის გამოყენებით ანალოგური საათის
ანიმაციის შექმნა. JavaScript-ის გამოყენების გარეშე უნდა აეწყოს საათის ციფერბლატი
და სამივე ისარი — საათების, წუთებისა და წამების — რომლებიც სწორი სიჩქარით
ბრუნავენ CSS `@keyframes` ანიმაციის მეშვეობით.

## მოთხოვნები

- **საათის კორპუსი (ციფერბლატი):** მრგვალი ფორმის კონტეინერი, რომელზეც
  განთავსებულია ციფრები (მინიმუმ 12, 3, 6, 9).
- **საათების ისარი (`.hours`):** ყველაზე მოკლე და სქელი ისარი, რომელიც
  სრულ წრეს უვლის 12 საათში (ანიმაციის ხანგრძლივობა შესაბამისად დემო რეჟიმში
  შეიძლება შემცირდეს).
- **წუთების ისარი (`.minutes`):** საშუალო სიგრძის ისარი, სრულ წრეს ასრულებს
  60 წუთში.
- **წამების ისარი (`.seconds`):** ყველაზე გრძელი და თხელი ისარი, სრულ წრეს
  ასრულებს 60 წამში.
- სამივე ისარი უნდა ბრუნავდეს ციფერბლატის **ცენტრის** გარშემო — ამისთვის
  გამოიყენეთ `transform-origin`.
- ანიმაცია უნდა იყოს **შეუჩერებელი** (`infinite`) და **წრფივი** (`linear`),
  რათა ისრების მოძრაობა იყოს თანაბარი.

## ტექნიკური მინიშნებები

- `position: absolute` და `position: relative` — ისრების ცენტრში დასაფიქსირებლად.
- `transform-origin` — ბრუნვის ცენტრის შესაცვლელად (მაგ. `right center` ან
  `center`).
- `transform: rotate(...deg)` — ისრის საწყისი მიმართულების დასაყენებლად.
- `@keyframes` — ისრების უწყვეტი ბრუნვისთვის (`0% → rotate(0deg)`,
  `100% → rotate(360deg)`).
- CSS ცვლადები (`--size`) — საათის ზომის მართვისთვის ერთი ადგილიდან.

## სასარგებლო რესურსები

### CSS ანიმაციები

- [MDN — Using CSS animations](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_animations/Using_CSS_animations)
- [MDN — `@keyframes`](https://developer.mozilla.org/en-US/docs/Web/CSS/@keyframes)
- [MDN — `transform`](https://developer.mozilla.org/en-US/docs/Web/CSS/transform)
- [MDN — `transform-origin`](https://developer.mozilla.org/en-US/docs/Web/CSS/transform-origin)
- [CSS-Tricks — Almanac: animation](https://css-tricks.com/almanac/properties/a/animation/)
- [web.dev — Animations](https://web.dev/learn/css/animations/)

### Inspect Element (DevTools) — ბრაუზერის დეველოპერული ხელსაწყოები

Inspect Element არის ბრაუზერში ჩაშენებული ხელსაწყო, რომელიც გვაძლევს HTML-ისა
და CSS-ის რეალურ დროში დათვალიერებისა და შეცვლის შესაძლებლობას. ეს განსაკუთრებით
სასარგებლოა ანიმაციების გამართვისთვის (debug).

**როგორ გავხსნათ:**
- **Chrome / Edge / Brave:** მარჯვენა ღილაკი გვერდზე → `Inspect` ან
  `Cmd + Option + I` (Mac) / `Ctrl + Shift + I` (Windows/Linux).
- **Firefox:** მარჯვენა ღილაკი → `Inspect Element` ან `Cmd + Option + I`.
- **Safari:** ჯერ ჩართეთ `Develop` მენიუ (Settings → Advanced → Show Develop
  menu), შემდეგ `Cmd + Option + I`.

**მთავარი პანელები ანიმაციებისთვის:**
- **Elements / Inspector** — HTML-ის სტრუქტურა და მიმდინარე CSS წესები.
  ნებისმიერი თვისების ჩართვა/გამორთვა შესაძლებელია `checkbox`-ით.
- **Styles პანელი** — ცოცხლად შეცვალეთ `transform`, `animation-duration` და
  სხვა თვისებები ისე, რომ ფაილში ცვლილება არ შეიტანოთ.
- **Animations პანელი** (Chrome DevTools → `⋮` → More tools → Animations) —
  ანიმაციების შენელება (0.25x, 0.1x), ცალკეული `@keyframes`-ის გადახედვა და
  დროის ხაზის (timeline) მართვა. ეს არის **საუკეთესო** გზა საათის ისრების
  გასამართად.
- **Computed პანელი** — საბოლოო, რეალურად გამოყენებული CSS მნიშვნელობები.

**სასარგებლო ბმულები DevTools-ზე:**
- [Chrome DevTools — Inspect animations](https://developer.chrome.com/docs/devtools/css/animations)
- [Chrome DevTools — CSS overview](https://developer.chrome.com/docs/devtools/css)
- [MDN — Firefox Animation Inspector](https://firefox-source-docs.mozilla.org/devtools-user/page_inspector/how_to/work_with_animations/index.html)
- [Chrome DevTools — Overview](https://developer.chrome.com/docs/devtools)

### დამატებითი — ანალოგური საათის მაგალითები

- [Codrops — CSS animation tutorials](https://tympanus.net/codrops/category/tutorials/)
