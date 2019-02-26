# footballi-api-wrapper
Simple PHP wrapper for Footballi.net API

Required PHP modules: `php-curl`

If you want to remove my name in your projects, please donate some money to me via http://zarinp.al/@ntrolly79.
## Usage
Just include `subscene.php` to your project and use it:
```
<?php

require_once __DIR__.'/sfootballi-api-wrapper.php	';

// Get matches of today
 echo json_encode($footballi::getMatchesOfToday());
// Get matches of an specific date
 echo json_encode($footballi::getMatchesOfDate('2018-6-16'));
// Search in matches
 echo json_encode($footballi::searchMatches(array(array('property' => 'ENABLE', 'value' => '1', 'operator' => '='), array('property' => 'TYPE', 'value' => '0', 'operator' => '=')), 'DESC'));
// Get info of an specific match
 echo json_encode($footballi::getMatchInfo(37760));
// Get standings of a competition
 echo json_encode($footballi::getCompetitionStandings(9));
// Get fixtures of a competition
echo json_encode($footballi::getCompetitionFixtures(9));
// Get top scorers of a competition
 echo json_encode($footballi::getTopScorersOfCompetition(9));
// Get latest news
 echo json_encode($footballi::getLatestNews(1));
// Get contents of a news
 echo json_encode($footballi::getNewsContent(339749));
 ?>
 ```
