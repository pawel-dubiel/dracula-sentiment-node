# dracula-sentiment-node

<center>
<img src="http://dracula.sentimentron.co.uk/img/dracula-js.svg" alt="dracula.js" /> <br />
<img src="https://travis-ci.org/Sentimentron/dracula-sentiment-node.png?branch=master" style="max-width:100%;" />
</center>

[Try a live web demo &raquo;](http://dracula.sentimentron.co.uk/sentiment-demo/)

[View on npm &raquo;](https://www.npmjs.com/package/dracula-sentiment)

A quick way to get "good enough" sentiment analysis into your applications, this package uses character and word-level embeddings and LSTM networks to decide if a given text is either "positive" or "negative".

## Installation

    npm install dracula-sentiment --save

## Usage
    
    var dracula = require('dracula-sentiment');
    var text = "xoxo cant wait";
    // Output a 'positive', 'negative', or 'neutral' label
    console.log(text, dracula.analyze(text));
    // To output a [negative, neutral, positive] float array
    console.log(text, dracula.score(text));

For best performance and accuracy, remove any non-ascii characters by converting them to their closest equivalents via [`unidecode`](https://www.npmjs.com/package/unidecode) or something similar, and feed it sentence-sized chunks of text. 

## Testing
    
    npm test

Tests aren't very extensive at present. 

## Contributing

If you encounter any sentences where the classification is obviously wrong, open an issue and we'll work out a way to extend Dracula's training data so that it doesn't happen. Contributions to clean up the code and improve its style and performance are certainly welcome! 

## Release
* 1.0.0 Original release
* 1.1.0 Adds a new function to get the underlying scores
* 1.1.1 Documentation and npm package updates
