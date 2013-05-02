Andrew Dunne

What follows is my attempt at defining my project.  In words: I created a type constructor of TrackPoint with a value constructor of TP with components of rpm, time, distance and speed.  The initial goal was to have a function that returned the time, distance and speed as a kart entered the corner which I defined as an rpm value less than 10000.  I then wanted to define corner exit as rpm greater than 9999 again returning time, distance and speed. Using those two points I would then have the program calculate time in the corner (exit time- entry time) and distance in corner (exit distance - entry distance) and corner speed (exit speed - entry speed).  By comparing these variables in each corner when analyzing lap to lap differences a driver coach would be able to show the driver the effect of entry speed on corner time and distance which in turn would be reflected in exit speed.  From my practical experience sometimes having a slower entry speed gives you a greater exit speed which may lead to an overall faster lap time, however, my goal for the program was to have objective criteria to use when evaluating driver performance and identifying areas for improvement. 
I tried to but I am unable to figure out how to map and filter the data to do what I wanted it to. I experimented with guards and comprehensions but failed to get a workable model. 

data TrackPoint = TP { rpm ::  Integer
                     , time ::  Integer
                     , distance :: Float
                     , speed :: Float
                     } deriving (Show) 

cornerentry :: [TrackPoint] -> [(Integer, Float, Float)] (output is time, distance and speed at corner entry) entry = TP { rpm < 10000, time _ , distance _, speed _ } 

cornerexit :: [TrackPoint] -> [(Integer, Float, Float)] (output is time, distance and speed at corner exit)

exit = TP { rpm > 9999, time _ , distance _, speed _ } 

cornertime :: ( exit time - entry time ) -> Integer

cornerdistance :: ( exit distance - entry distance ) -> Float

cornerspeed :: ( exit speed - entry speed) -> Float
