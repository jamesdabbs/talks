# [fit] Ruby on Rails
# [fit] _**a Crash Course**_
# [fit] James Dabbs _|_ james@theironyard.com

---

# [fit] Ruby

![](http://a4.files.readwrite.com/image/upload/c_fit,cs_srgb,dpr_1.0,q_80,w_620/MTIyMzI4OTI5MTU0NTI2NDg5.jpg)

---

# _Ruby_

* Dynamic
* Object-oriented
* General purpose

---

# _Ruby_

* Expressive
* Elegant
* Optimized for _**happiness**_

---

# [fit] Rails

![](https://pbs.twimg.com/profile_images/2556368541/alng5gtlmjhrdlr3qxqv.jpeg)

---

# _Rails_

* MVC web framework
* Convention over configuration
* Optimized for _productivity_

^ Essentially 10 years of codified best practices for building CRUD apps
^ and a great ecosystem of extensions

---

# [fit] Demo

![](http://www.eonline.com/eol_images/Entire_Site/2013719/rs_600x398-130819150912-live1.jpg)


^ * Generate project
^   * rails new crash
^ * Add model - Meme
^   * rails generate scaffold Meme title:string link:text description:text
^ * Add Votes - +/- and count
^   * rails generate migration AddScoreToRecipes score:integer
^   * rake db:migrate
^
^ * Add User accounts
^   * Add `gem 'devise'` to `Gemfile`
^   * bundle install
^   * rails generate devise:install
^   * rails generate devise User
^   * rake db:migrate
^ * Add Vote model
^   * rails generate model Vote user:belongs_to recipe:belongs_to
^
^ * Add admin section
^   * Add `gem 'rails_admin'` to `Gemfile`
^   * rails g rails_admin:install

---

# _References_

* Slides @ github.com/jamesdabbs/rails-crash-course/slides.md
* Chris Pine's [Learn to Program](https://pine.fm/LearnToProgram/) for people with no prior experience
* Russ Olsen's [Eloquent Ruby](http://www.amazon.com/Eloquent-Ruby-Addison-Wesley-Professional-Series/dp/0321584104) for people without no prior experience
* Michael Hartl's [Rails Tutorial](https://www.railstutorial.org/)
