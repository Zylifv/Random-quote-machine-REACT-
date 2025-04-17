class App extends React.Component {
      state = {
        quote: '"Hey! Just because i don\'t care, doesn\'t mean i don\'t understand."',
        author: '- Homer Simpson',
        error: null
    }
    
 
  fetchQuotes() {
    fetch("https://thesimpsonsquoteapi.glitch.me/quotes")
        .then(res => res.json())
        .then(data =>
             this.setState({
            quote: '"' + data[0].quote + '"',
            author: "- " + data[0].character
          })
         ) 
          .catch(error => this.setState({error: true
      }));
    }
 
   render() {
     return (
       <div id="wrapper">
         <div id="quote-box">
         <p id="text">{this.state.quote}</p>
         <p id="author">{this.state.author}</p>
         <button id="new-quote" onClick={() => {this.fetchQuotes()}}>New Quote</button>
           <a href="twitter.com/intent/tweet" id="tweet-quote"><img src="https://www.svgrepo.com/show/308971/twitter-social-media-social-network-logo.svg"></img></a>
           <a href="https://www.facebook.com/share_channel/?type=empty&source_surface=external_share" id="facebook"><img src="https://images.seeklogo.com/logo-png/46/2/facebook-icon-black-logo-png_seeklogo-468341.png"></img></a>
           <a id="sig">- By R McGregor</a>
         </div>
       </div>
     );
   }
 };

React.render(<App />, document.getElementById("root"));
