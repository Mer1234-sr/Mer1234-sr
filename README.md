
//alert("I work!");

/*algorithm (JS)
1. Getting the user input (DOM) -> Document Object Model
2. Division
3. Display the result

if( fnumber == "" ){      //notify the user that there is a problem      $('#fnumber_error').html("Please fill in the first number");        $('#fnumber').addClass('is-invalid');      $('#fnumber').focus();   }else if(snumber == ""){      $('#snumber_error').html("Please fill in the second number");      $('#snumber').addClass('is-invalid');        $('#snumber').focus();  }else if(snumber == 0){      //2c. The second number is NOT zero       $('#snumber_error').html("Please enter a non-zero value for the second number");      $('#snumber').addClass('is-invalid');       $('#snumber').focus();   }else{        //2d. Divide     let result = fnumber / snumber;     //3a. Get the element to display the result   //3b. Display the result in the element    $('#results').html(result);}
*/


/*algorithm (JS)
0. When a user clicks the calculate button
1. Getting the user input (DOM) -> Document Object Model
1a. First number (value)
1b. Second number (value)
2. Division(before we divide,make sure)
2a. The first and second value is NOT empty(there is a value)
2b. The values are numbers
2c. The second number is NOT zero
2d. Divide
3. Display the result
3a. Get the element to display the result
3b. Display the result in the element*/

//0. When a user clicks the calculate button
$('#calc').click(function(){
        console.log('clicked');
        //1. Getting the user input (DOM) -> Document Object Model
        //document.getElementById('fnumber').value;    
        let fnumber = $('#fnumber').val();   
        let snumber = $('#snumber').val();
        console.log('fnumber : '+ fnumber + ' snumber: '+ snumber);

        if( fnumber == "" ){
                    //notify the user that there is a problem       
        $('#fnumber_error').html("Please fill in the first number");            
        $('#fnumber').addClass('is-invalid');        
        $('#fnumber').focus();    
    }
        else if(snumber == ""){        
            $('#snumber_error').html("Please fill in the second number");        
            $('#snumber').addClass('is-invalid');        
            $('#snumber').focus();    
        }
        else if(snumber == 0){        
            //2c. The second number is NOT zero        
            $('#snumber_error').html("Please enter a non-zero value for the second number");        
            $('#snumber').addClass('is-invalid');       
            $('#snumber').focus();
        }
        else{       
            //2d. Divide       
            let result = fnumber / snumber;
                 //3a. Get the element to display the result       
                 //3b. Display the result in the element
                 $('#results').html(result);    }

       //clear the error messages onkeyup for the input field - fnumber and snumber
       $('.form-control').on('keyup',function(){
            let first_num = $('#fnumber').val();
            let second_num = $('#snumber').val();
            if( first_num != ""){
                $('#fnumber_error').html("");
                $('#fnumber').removeClass('is-invalid');
                $('#fnumber').addClass('is-valid');
            }
            if( second_num != ""){       
                $('#snumber_error').html("");        
                $('#snumber').removeClass('is-invalid');        
                $('#snumber').addClass('is-valid');    
            }
        });
    });

    

// ALTERNATIVE CODE----INCASE THE ONE ABOVE WASN'T CORRECT
 
//alert("I work!");

/*algorithm (JS)
0. If the divide bbutton is clicked.. START (EVENT)
1. Getting the user input (DOM) -> Document Object Model
    1a. firstnumber
    1b. second number
2. Division
(before we divide, ensure that)
    2a. There is a value
    2b. Value for thr second number must not be zero
    2c. If all is well(2a,2b) then we divide
3. Display the result
    3a. get the result element(DOM)
    3b. show the result in the result element

*/
//1. Getting the user input(DOM) -> Document ObjectModel
$('#calc').click(function () {
    let first_num = $('#fnumber').val();
    let second_num = $('#snumber').val();
    console.log('First number : ' + first_num);
    console.log('Second number : ' + second_num);

    //2a. The first and second value is NOT empty(there is a value)
    if (first_num == "") {
        //notify the user that there is a problem
        $('#fnumber_error').html("Please fill in the first number");
        $('#fnumber').addClass('is invalid');
        $('#fnumber').focus();

    } else if (second_num == "") {
        $('#snumber_error').html("Please fill in the second number");
        $('#snumber').addClass('is-invalid');
        $('#snumber').focus();

    } else if (second_num == 0) {
        //2c. The second number is NOT zero
        $('#snumber_error').html("Please enter a non-zero value for the second number");
        $('#snumber').addClass('is-invalid');
        $('#snumber').focus();

    } else {
        //2d. Divide
        let result = first_num / second_num;

        //3a. Get the element to display the result
        //3b. Display the result in the element
        $('#results').html(result);
    }


})
//clearing the messages on keyup for the two input fields.
$('.form-control').on('keyup', function () {
    let first_num = $('#fnumber').val();
    let second_num = $('#snumber').val();

    if (first_num != "") {
        $('#fnumber_error').html("");
        $('#fnumber').removeClass('is-invalid');
        $('#fnumber').addClass('is-valid');
    }
    if (second_num != "") {
        $('#snumber_error').html("");
        $('#snumber').removeClass('is-invalid');
        $('#snumber').addClass('is-valid');
    }
});
