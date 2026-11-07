# WebMiddle
### Hi, my name is Tyoma

<img src="https://thumb.wikimedia.org/wikipedia/commons/thumb/d/d7/Android_robot.svg/1280px-Android_robot.svg.png?utm_source=uk.wikipedia.org&utm_campaign=index&utm_content=thumbnail" alt="Опис фото" width="300" >


**I'm javascript developer.**
*There is Example of my code:*
```javascript
let types = ["education", "recreational", "social", "diy", "charity", "cooking", "relaxation", "music", "busywork"];


$.each(types,function(index,type)
{
    $('#typeSelect').append(`
            <option value="${type}">${type.charAt(0).toUpperCase() + type.slice(1)}</option>
        `)
});

$('#activity').hide();

$('#ranActBut').click(function () {
    $('#ranActBut').attr('disabled', true);
    $('#ranActBut').html('Loading....');
    let params = $('#filters').serialize();
    console.log(params);
    $.ajax(`https://www.boredapi.com/api/activity?${params}`, {
        success: function (data) {
            $('#activity').fadeIn(500);
            $('#activity').html(
                `
                <p>Activity: ${data.activity}</p>
                <p>Price: ${data.price} $</p>
                <p>Type: ${data.type}</p>
                `
            );
            $('#ranActBut').attr('disabled', false);
            $('#ranActBut').html('Random Again');
        },
        error: function (xhr) {
            console.log(xhr.statusText);
            $('#ranActBut').attr('disabled', false);
        }

    })
});

 ```
 
You can reach me via the links:
* [my facebook](http://github.com)
* [my website](http://github.com)
* [my telegram](http://github.com)
