# php-weather-plugin
php weather plugin using openweathermap API
THis code is base on this toturial:
https://rudrastyh.com/wordpress/weather-shortcode-api.html

it create a shortcode for displaying weather forcast via shortcode.

If you would like to have the user entering his own values for the weather forcast you can create a custom field that will get the shortcode and add it to a page template lkike so:

##this code goes to the page template where you wqant to display the widjet:
    <section class="hp-weather">
        <div class="weather-container">
            <?php
//fetch the weather shortcode entered by the user:
$users_shortcode = get_field('weather', 'option');
//echo $users_shortcode;
//call the shortcode plugin with the values user has entered:
echo do_shortcode($users_shortcode);
?>
        </div>
</div>
