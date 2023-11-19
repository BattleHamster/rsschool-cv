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

### Code examples
```
$( document ).ready(function() {
	$('.xdget-trainingList .stream-table tr a' ).append(`<div class='progress-block'> <div class='progress_name'> Прогресс: </div><div class='theory_module-status'> 0%	</div></div>`);


let modules = $('.stream-table > tbody > tr');
let training_links = [];

modules.each(function() {
    training_links.push($(this).find('a').attr('href'));
});

let get_status = function(url, module) {
    $.ajax({
        method: "Get",
		url: url,		
		success: function(data) {
			var menuPageDom = $('<xxx></xxx>').append($.parseHTML(data));
							
			if ((!$(module).hasClass('no-lessons'))) {
			
			let total_lessons_module = menuPageDom.find('.lesson-list li:not(".divider"):not(".lesson-is-hidden")').length;				
			let passed_lessons_module = menuPageDom.find('.lesson-list li.user-state-accomplished').length;
			
			console.log("passed_lessons_module: "+passed_lessons_module);


			if (passed_lessons_module == total_lessons_module) {
				$(module).addClass('done');				
				$(module).find('.theory_module-status').text('Пройдено 100%');
			} else {
				$(module).addClass('active');
				let progress_module = parseInt(passed_lessons_module * 100 / total_lessons_module);
				$(module).find('.theory_module-status').text( progress_module + '%');
			}
			} 			
			}
		});
};

for(let i = 0; i < training_links.length; i++) {
    get_status(training_links[i], modules[i]);
}

});


```
