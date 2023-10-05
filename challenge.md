# Introduction to DOM - Exercises

1. Answer the following questions:

   - How would you select from JavaScript an element `p` that has the class `text` and also the class `important`?
    document.querySelector('p.text.important');

   - How would you select from JavaScript a `button` element with class `button` and that is disabled?
    document.querySelector('button.button:disabled');

   - How would you select from JavaScript all the `li` elements that are direct children of an `ul` element with class `list`?
    document.querySelectorAll('ul.list > li');

   - How would you select from JavaScript all the `input` elements that are descendants of a `form` element with class `form-new-item`, and that have a `type` attribute with a value `text`?
   document.querySelectorAll('form > input.form-new-item input [type='text']');

2. From the following HTML structure, create a script that selects the header "The MEAN stack". Next, change the text to "The MERN stack" and remove the "subtitle" class.

```html

<main class="main-content">
  <h1 class="app-title">Bootcamp technologies</h1>
  <section class="info">
    <h2 class="subtitle">The MEAN stack</h2>
    <p class="text">
      The MEAN stack is the set of technologies used in the bootcamp by
      FullStack Web Development.
    </p>
  </section>
  <script>
    const subtitle = document.querySelector('h2');
    subtitle.textContent = 'The MERN stack';
    subtitle.classList.remove('subtitle');
  </script>
</main>
```

3. Here you have an HTML without data:

```html
<article class="student">
  <h2 class="student-name"></h2>
  <span class="student-age"></span> years
  <img class="student-photo" src="" alt="" />
</article>
<script>
    const student = {
      name: "Nil Farras",
      age: 18,
      photoUrl: "https://t3.ftcdn.net/jpg/05/06/55/22/360_F_506552238_j3Y4oq4rrlLEgzVG30AdEe0TaRINtUKr.jpg"
    };

    const name = document.querySelector('.student-name');
    const age = document.querySelector('.student-age');
    const photo = document.querySelector('.student-photo');
  
    name.textContent = student.name;
    age.textContent = student.age;
    photo.src = student.photoUrl;
    photo.alt = student.name + "'s photo";
  </script>
```

Create a script where you declare a variable with a student's data
(name, age and photo URL). Next, get the elements from the HTML
and fill them in with the student's information.