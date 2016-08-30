# glowCards plan
* ~~test UI~~
  * ~~left/right next side~~
  * ~~down(next)/up(prev) card~~
* MVP
  * model: user (first name, last name, email, password)
    * has_many :decks
    * has_secure_password
  * model: deck (deck_name, user_id)
    * belongs_to :user
    * has_many :cards
  * model: card (front, back, rotation, index, deck_id)
    * belongs_to :deck
  * view: layout
  * view: index/signup/login/home
  * view: add_deck
  * view: show_deck
  * controller: application_controller
    * get '/'
      * sign up & how it works
      * decks, add deck button
  * controller: users_controller
    * post '/signup'
    * post '/login'
    * post '/logout'
  * controller: decks_controller
    * get 'add_deck'
    * post 'add_deck'
    * get '/decks/:id'
    * get '/decks/:id/edit'
* stage 2
  * update view: show_deck to include buttons to daily/weekly/monthly with one active
  * view: edit_deck
  * controller: decks_controller
    * get '/decks/:id/edit'
    * post '/decks/:id/edit'