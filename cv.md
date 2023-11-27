# Krystsina Liubchuk
## Automation QA Engineer

### Contact Info
**Telegram:** https://t.me/Boevoj_Homa

**email:** christy.lubchuk@gmail.com

### Summary
My goal is to learn and reach as much as possible in the life.
I want to improve my programming skills with Python, built a great and useful web application for my family members to make their life and work easier.
Maybe to combine python as a backend part and frontend part of application.

### Skills
* Python
* QA (manual and automation tests)
* HTML/CSS/JS
* SQL
* IT Support
* Languages (English: B2; Polish: C1; Belorussian: native; Russian: native)

### Experience

1. Automation QA Engineer (backend) at FinTech (2023-)
2. Automation QA Engineer at Dell (Software Storage. Python) (2019-2022)
3. Support Network Specialist at Cisco (2018-2019)
4. Salesforce Support (2016-2018)

### Education
1. Master Degree at Information Technologies; Mobile systems and networks (2015-2017);
   University of Maria Curie-Skłodowska in Lublin
2. Bachelor Degree at Information Technologies (2012-2015);
   University of Maria Curie-Skłodowska in Lublin

### English
According to EPAM test I have C1, however I would rather grade it as B2.
In all of my previous jobs I had to use English every day: in communication with customers and the team.
I don't have any problems to elaborate my thoughts or opinions, but I know that I can improve my grammar skills.



### Code examples
```
let needed_val = $('#field-input-1538173').val();
  $('.user-phone').after(`<div class="addition_filed_custom"></div>`);  
  $('.addition_filed_custom').text('Значение из поля: ' + needed_val);
let ajax_content = '';

let user_link = $('.user-name a:first-child').attr('href');
  
let get_field = function(user_link, needed_val) {
$.ajax({
  method: "Get",
  url: user_link,    
  beforeSend: function(jqXHR, settings) {
        // Проверить ссылку, по которой перехожу
        console.log("Request URL:", settings.url);
    },
  success: function(data) {
  setTimeout(function () { console.log("Howdy!") }, 1000);
    var menuPageDom = $('<xxx></xxx>').append($.parseHTML(data));    
    if ( menuPageDom.find('#field-input-1538173').length > 0) {
    console.log("Поле нашлось");
    let test = menuPageDom.find('#field-input-1538173').val();
    console.log("test: " + test);
      }
    ajax_content = $.parseHTML(data);
    }
  });
};  

get_field(user_link, needed_val);

```
