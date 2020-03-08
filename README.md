# executing command line codes with electron JS
## We are using  `node child_process`

        const exec = require('child_process').exec;

      function execute(command, callback) {
          exec(command, (error, stdout, stderr) => { 
              callback(stdout); 
          });
      };

      // call the function
      execute('ping -c 4 0.0.0.0', (output) => {
          console.log(output);
      });
      
 
 #### The file [`main.js`](https://github.com/fahad-israr/command_line_with_electron/blob/master/main.js) demonstrates an example.

--------------------------------------------------------------------------------------------------------------
#### More at: https://discuss.atom.io/t/execute-shell-commands-from-application/20013 
