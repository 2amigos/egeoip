egeoip
======

***EGeoIp Extension uses geoPlugin free webservice to locate IP geo information***

This extension allows you to easily integrate the geoPlugin webservice into your Yii applications. 


##What is geoPlugin?
geoPlugin offers you, the webmaster, the ability to easily geo-localize your visitor down to the city they are in, know what currency they use and the up-to-date currency exchange rate of their currency versus yours.  

##Requirements

Developed with Yii 1.1.6

##Usage

Unpack the contents of the extension to your protected/extensions directory. Once you do that, the following is an example on how to use it:

~~~
Yii::import('ext.EGeoIP');

$geoIp = new EGeoIP();

$geoIp->locate('88.27.28.44'); // use your IP

echo 'Information regarding IP: <b>'.$geoIp->ip.'</b><br/>';
echo 'City: '.$geoIp->city.'<br>';
echo 'Region: '.$geoIp->region.'<br>';
echo 'Area Code: '.$geoIp->areaCode.'<br>';
echo 'DMA: '.$geoIp->dma.'<br>';
echo 'Country Code: '.$geoIp->countryCode.'<br>';
echo 'Country Name: '.$geoIp->countryName.'<br>';
echo 'Continent Code: '.$geoIp->continentCode.'<br>';
echo 'Latitude: '.$geoIp->latitude.'<br>';
echo 'Longitude: '.$geoIp->longitude.'<br>';
echo 'Currency Symbol: '.$geoIp->currencySymbol.'<br>';
echo 'Currency Code: '.$geoIp->currencyCode.'<br>';
echo 'Currency Converter: '.$geoIp->currencyConverter.'<br/>';

echo 'Converting $10.00 to '.$geoIp->currencyCode.': <b>'.$geoIp->currencyConvert(10).'</b><br/>';
~~~
##Note 

Please make use of the forum post to report errors, requests, and suggestions. Let comments on this extension for coding hints.

##Resources
 * [Project page](http://www.ramirezcobos.com/)
 * [geoPlugin Webservice](http://www.geoplugin.com/)
 * [Forum Post](http://www.yiiframework.com/forum/index.php?/topic/16495-extension-egeoip-extension/)