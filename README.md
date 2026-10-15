# Git & GitHub პრაქტიკული დავალება: სტუდენტების საზოგადოება

## მიზანი

ივარჯიშე Git-ისა და GitHub-ის გამოყენებით თანამშრომლობით სამუშაო პროცესში:

**Fork → Clone → Branch → Edit → Commit → Push → Pull Request**

შენი დავალებაა, Student Community ვებსაიტს დაამატო ერთი მკაფიოდ განსაზღვრული `About Me` სექცია. მთავარი მიზანი Git-ისა და GitHub-ის სამუშაო პროცესის პრაქტიკაა და არა არსებული გვერდის დიზაინის შეცვლა.

## ნაწილი 1 — Fork და Clone

1. გახსენი ლექტორის მიერ გაზიარებული ორიგინალი რეპოზიტორია.
2. დააჭირე **Fork** ღილაკს, რათა რეპოზიტორიის ასლი შენს GitHub ანგარიშზე შექმნა.
3. დააკლონე შენი Fork კომპიუტერში.
4. გახსენი დაკლონილი პროექტის საქაღალდე VS Code-ში.
5. ცვლილებების შეტანამდე შეამოწმე რეპოზიტორიის მიმდინარე მდგომარეობა.

## ნაწილი 2 — Branch-ის შექმნა

შექმენი ახალი Branch და გადადი მასზე. Branch-ის სახელი ზუსტად უნდა იყოს:

`feature/add-profile`

**არ შეიტანო ცვლილებები პირდაპირ `main` Branch-ში.**

## ნაწილი 3 — HTML-ის განახლება

გახსენი `index.html` და დაამატე ქვემოთ მოცემული სექცია **`<main>` ელემენტის შიგნით**, არსებული Community სექციის შემდეგ და `</main>` ელემენტამდე.

გამოიყენე ზუსტად ეს HTML სტრუქტურა და შინაარსი, თუმცა მაგალითში მოცემული სახელი და ტექსტები შეცვალე საკუთარი ინფორმაციით.

```html
<section class="about section" id="about">
  <div class="container">
    <p class="eyebrow">ABOUT THE STUDENT</p>
    <h2>About Me</h2>
    <p class="about-description">
      Hi! My name is Your Name. I am learning frontend development and
      practicing HTML, CSS, Git, and GitHub.
    </p>

    <div class="about-details">
      <p><strong>My goal:</strong> Build my first web projects.</p>
      <p><strong>Currently learning:</strong> HTML and CSS.</p>
      <p><strong>My interests:</strong> Design, technology, and learning.</p>
    </div>
  </div>
</section>
```

შეცვალე `Your Name` და მაგალითში მოცემული აღწერები საკუთარი ინფორმაციით.

**მნიშვნელოვანია:** არ შეცვალო HTML ელემენტების სავალდებულო `class` ატრიბუტები და `id="about"`, რადგან ქვემოთ მოცემული CSS სტილები მათზეა დამოკიდებული.

## ნაწილი 4 — CSS-ის განახლება

გახსენი `style.css` და ფაილის ბოლოში დაამატე შემდეგი სტილები:

```css
.about {
  background: #edf2ff;
}

.about-description {
  max-width: 650px;
  color: #526174;
}

.about-details {
  max-width: 650px;
  margin-top: 24px;
  padding: 24px;
  border: 1px solid #d8e2f5;
  border-radius: 12px;
  background: #ffffff;
}

.about-details p {
  margin-bottom: 12px;
}

.about-details p:last-child {
  margin-bottom: 0;
}
```

შეგიძლია ტექსტები საკუთარ ინფორმაციას მოარგო, მაგრამ არ წაშალო აუცილებელი HTML კლასები და იდენტიფიკატორები (`id`).

**არ შეცვალო ვებსაიტის სხვა ნაწილები.**

## ნაწილი 5 — ცვლილებების შემოწმება და Commit

1. შეამოწმე, რომელ ფაილებშია ცვლილებები შეტანილი.
2. Stage-მდე გადახედე ცვლილებებს და დარწმუნდი, რომ მხოლოდ საჭირო ნაწილები შეცვალე.
3. Stage-ში გადაიტანე `index.html` და `style.css`.
4. შექმენი Commit შემდეგი შეტყობინებით:

`feat: add about me section`

დარწმუნდი, რომ Commit შექმნილია `feature/add-profile` Branch-ზე და არა `main` Branch-ზე.

## ნაწილი 6 — Branch-ის ატვირთვა

ატვირთე `feature/add-profile` Branch **შენს Fork-ში** და არა ლექტორის ორიგინალ რეპოზიტორიაში.

ატვირთვის შემდეგ გახსენი შენი Fork GitHub-ზე და გადაამოწმე, რომ `feature/add-profile` Branch ნამდვილად გამოჩნდა.

## ნაწილი 7 — Pull Request-ის შექმნა

შექმენი Pull Request შემდეგი პარამეტრებით:

- **Base repository:** ლექტორის ორიგინალი რეპოზიტორია
- **Base branch:** `main`
- **Head repository:** შენი Fork
- **Compare branch:** `feature/add-profile`

Pull Request-ის სათაურად გამოიყენე:

`Add About Me section`

აღწერის ველში ჩასვი შემდეგი ტექსტი:

```text
Added an About Me section to the Student Community website.

Changes:
- Added personal introduction and learning goals in index.html
- Added styles for the About Me section in style.css
```

გადახედე Pull Request-ს და დარწმუნდი, რომ მასში მხოლოდ შენ მიერ დაგეგმილი ცვლილებებია წარმოდგენილი.

შემდეგ შექმენი Pull Request.

**არ გააერთიანო (Merge) Pull Request, თუ ლექტორი ამას არ მოგთხოვს.**

## დასრულების საკონტროლო სია

- [ ] შევქმენი ორიგინალი რეპოზიტორიის Fork.
- [ ] დავაკლონე ჩემი Fork კომპიუტერში.
- [ ] შევქმენი და გამოვიყენე `feature/add-profile` Branch.
- [ ] დავამატე მოთხოვნილი HTML სექცია.
- [ ] დავამატე მოთხოვნილი CSS სტილები.
- [ ] შევქმენი Commit მითითებული შეტყობინებით.
- [ ] Branch ავტვირთე ჩემს Fork-ში.
- [ ] შევქმენი Pull Request ორიგინალი რეპოზიტორიის `main` Branch-ის წინააღმდეგ.
- [ ] შევამოწმე Pull Request-ის სათაური, აღწერა და შეცვლილი ფაილები.

## მნიშვნელოვანი წესები

- არ შექმნა Commit პირდაპირ ლექტორის რეპოზიტორიაში.
- არ იმუშაო `main` Branch-ზე.
- არ შეცვალო ვებსაიტის სხვა სექციები.
- დაიცავი დავალებაში მითითებული HTML სტრუქტურა, კლასები და `id`.
- Pull Request-ის Merge საჭირო არ არის.

**დავალება დასრულებულად ითვლება მაშინ, როდესაც Pull Request შექმნილია და მზად არის ლექტორის მიერ შესამოწმებლად.**