# glowCards plan
* test UI
  * left/right next side
  * down(next)/up(prev) card
  * use two arrays a=[a0..a9] and b=[b0..b9]
* MVP
  * model: user (first name, last name, email, password)
    * has_many :decks
    * has_secure_password
  * model: deck (deck_name, user_id)
    * belongs_to :user
    * has_many :cards
  * model: card (side_a, side_b, rotation, index, deck_id)
    * belongs_to :deck
  * view: layout
  * view: signup/login/home
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
  * view: edit_deck
  * controller: decks_controller
    * get '/decks/:id/edit'
    * post '/decks/:id/edit'