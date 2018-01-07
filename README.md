# YashCinemas
Online Ticket System

#
# DUMP FILE
#
# Database is ported from MS Access
#------------------------------------------------------------------
# Created using "MS Access to MySQL" form http://www.bullzip.com
# Program Version 5.5.282
#
# OPTIONS:
#   sourcefilename=C:/Users/Yashwanth Anand S/Documents/online/Dream.mdb
#   sourceusername=
#   sourcepassword=
#   sourcesystemdatabase=
#   destinationdatabase=movedb
#   storageengine=MyISAM
#   dropdatabase=0
#   createtables=1
#   unicode=1
#   autocommit=1
#   transferdefaultvalues=1
#   transferindexes=1
#   transferautonumbers=1
#   transferrecords=1
#   columnlist=1
#   tableprefix=
#   negativeboolean=0
#   ignorelargeblobs=0
#   memotype=LONGTEXT
#   datetimetype=DATETIME
#

CREATE DATABASE IF NOT EXISTS `movedb`;
USE `movedb`;

#
# Table structure for table 'Cinema'
#

DROP TABLE IF EXISTS `Cinema`;

CREATE TABLE `Cinema` (
  `ID` INTEGER NOT NULL AUTO_INCREMENT, 
  `Name` VARCHAR(30), 
  `Address` VARCHAR(100), 
  `CityID` INTEGER, 
  `NoOfScreens` INTEGER, 
  `Capacity` INTEGER, 
  `Rating` INTEGER, 
  `PlatinumRate` INTEGER, 
  `GoldRate` INTEGER, 
  `SilverRate` INTEGER, 
  `EstablishDate` DATETIME, 
  INDEX (`Name`), 
  INDEX (`CityID`), 
  INDEX (`PlatinumRate`), 
  PRIMARY KEY (`ID`)
) ENGINE=myisam DEFAULT CHARSET=utf8;

SET autocommit=1;

#
# Dumping data for table 'Cinema'
#

INSERT INTO `Cinema` (`ID`, `Name`, `Address`, `CityID`, `NoOfScreens`, `Capacity`, `Rating`, `PlatinumRate`, `GoldRate`, `SilverRate`, `EstablishDate`) VALUES (1, 'DreamWorld', 'Dream World Cinemas,<br>Opp. Income Tax Office,<br>Ashram Road', 1, 3, 750, NULL, 200, 150, 125, '2000-10-02 00:00:00');
INSERT INTO `Cinema` (`ID`, `Name`, `Address`, `CityID`, `NoOfScreens`, `Capacity`, `Rating`, `PlatinumRate`, `GoldRate`, `SilverRate`, `EstablishDate`) VALUES (2, 'ADLABS Dream World', 'Dream World Cinemas<br>\nNear Isckon Megamall<br>\nS.G. Highway', 1, 3, 750, NULL, 200, 150, 125, '2005-01-23 00:00:00');
INSERT INTO `Cinema` (`ID`, `Name`, `Address`, `CityID`, `NoOfScreens`, `Capacity`, `Rating`, `PlatinumRate`, `GoldRate`, `SilverRate`, `EstablishDate`) VALUES (4, 'Xenon Cinemas', 'Xenon Cinemas,<BR>\nBerkeley Street,<br>Brooklyn,', 15, 2, 500, NULL, NULL, NULL, NULL, '1985-12-15 00:00:00');
INSERT INTO `Cinema` (`ID`, `Name`, `Address`, `CityID`, `NoOfScreens`, `Capacity`, `Rating`, `PlatinumRate`, `GoldRate`, `SilverRate`, `EstablishDate`) VALUES (5, 'Francos Cinema', 'Francos Cinema<br>\nDolivich Streete<br>\nDenis Forte \n\n', 16, 3, 400, NULL, NULL, NULL, NULL, '1988-02-16 00:00:00');
INSERT INTO `Cinema` (`ID`, `Name`, `Address`, `CityID`, `NoOfScreens`, `Capacity`, `Rating`, `PlatinumRate`, `GoldRate`, `SilverRate`, `EstablishDate`) VALUES (6, 'Liberos', 'Liberos Multiplex<br>\nFrankfinn street,<br>\nNear WTC\n', 10, 3, 500, NULL, NULL, NULL, NULL, '1991-01-01 00:00:00');
INSERT INTO `Cinema` (`ID`, `Name`, `Address`, `CityID`, `NoOfScreens`, `Capacity`, `Rating`, `PlatinumRate`, `GoldRate`, `SilverRate`, `EstablishDate`) VALUES (7, 'Xeon', 'HomeTown ', 3, 3, 500, NULL, NULL, NULL, NULL, '1986-10-12 00:00:00');
# 6 records

#
# Table structure for table 'City'
#

DROP TABLE IF EXISTS `City`;

CREATE TABLE `City` (
  `ID` INTEGER NOT NULL AUTO_INCREMENT, 
  `Name` VARCHAR(25), 
  `StateID` INTEGER, 
  PRIMARY KEY (`ID`), 
  INDEX (`StateID`)
) ENGINE=myisam DEFAULT CHARSET=utf8;

SET autocommit=1;

#
# Dumping data for table 'City'
#

INSERT INTO `City` (`ID`, `Name`, `StateID`) VALUES (1, 'Ahmedabad', 1);
INSERT INTO `City` (`ID`, `Name`, `StateID`) VALUES (2, 'Surat', 1);
INSERT INTO `City` (`ID`, `Name`, `StateID`) VALUES (3, 'Vadodara', 1);
INSERT INTO `City` (`ID`, `Name`, `StateID`) VALUES (4, 'Mumbai', 2);
INSERT INTO `City` (`ID`, `Name`, `StateID`) VALUES (5, 'Pune', 2);
INSERT INTO `City` (`ID`, `Name`, `StateID`) VALUES (6, 'Delhi', 3);
INSERT INTO `City` (`ID`, `Name`, `StateID`) VALUES (7, 'Hyderabad', 4);
INSERT INTO `City` (`ID`, `Name`, `StateID`) VALUES (8, 'Calcutta', 5);
INSERT INTO `City` (`ID`, `Name`, `StateID`) VALUES (9, 'Las vegas', 7);
INSERT INTO `City` (`ID`, `Name`, `StateID`) VALUES (10, 'New York', 8);
INSERT INTO `City` (`ID`, `Name`, `StateID`) VALUES (11, 'Shanghai', 9);
INSERT INTO `City` (`ID`, `Name`, `StateID`) VALUES (12, 'Beijing', 10);
INSERT INTO `City` (`ID`, `Name`, `StateID`) VALUES (13, 'Sydney', 11);
INSERT INTO `City` (`ID`, `Name`, `StateID`) VALUES (14, 'Tokyo', 12);
INSERT INTO `City` (`ID`, `Name`, `StateID`) VALUES (15, 'London', 13);
INSERT INTO `City` (`ID`, `Name`, `StateID`) VALUES (16, 'Paris', 14);
# 16 records

#
# Table structure for table 'Country'
#

DROP TABLE IF EXISTS `Country`;

CREATE TABLE `Country` (
  `ID` INTEGER NOT NULL AUTO_INCREMENT, 
  `Name` VARCHAR(40), 
  `Currency` VARCHAR(3), 
  `GMTDiff` INTEGER, 
  PRIMARY KEY (`ID`)
) ENGINE=myisam DEFAULT CHARSET=utf8;

SET autocommit=1;

#
# Dumping data for table 'Country'
#

INSERT INTO `Country` (`ID`, `Name`, `Currency`, `GMTDiff`) VALUES (1, 'India', 'INR', NULL);
INSERT INTO `Country` (`ID`, `Name`, `Currency`, `GMTDiff`) VALUES (2, 'China', 'CNY', NULL);
INSERT INTO `Country` (`ID`, `Name`, `Currency`, `GMTDiff`) VALUES (3, 'United States', 'USD', NULL);
INSERT INTO `Country` (`ID`, `Name`, `Currency`, `GMTDiff`) VALUES (4, 'Austrailia', 'ASD', NULL);
INSERT INTO `Country` (`ID`, `Name`, `Currency`, `GMTDiff`) VALUES (5, 'Japan', 'JY', NULL);
INSERT INTO `Country` (`ID`, `Name`, `Currency`, `GMTDiff`) VALUES (6, 'United kingdom', 'BSP', NULL);
INSERT INTO `Country` (`ID`, `Name`, `Currency`, `GMTDiff`) VALUES (7, 'France', 'EUR', NULL);
INSERT INTO `Country` (`ID`, `Name`, `Currency`, `GMTDiff`) VALUES (8, 'Canada', 'USD', NULL);
# 8 records

#
# Table structure for table 'Credit'
#

DROP TABLE IF EXISTS `Credit`;

CREATE TABLE `Credit` (
  `ID` INTEGER NOT NULL AUTO_INCREMENT, 
  `crno` VARCHAR(255), 
  `balance` INTEGER DEFAULT 0, 
  UNIQUE (`crno`), 
  PRIMARY KEY (`ID`)
) ENGINE=myisam DEFAULT CHARSET=utf8;

SET autocommit=1;

#
# Dumping data for table 'Credit'
#

INSERT INTO `Credit` (`ID`, `crno`, `balance`) VALUES (1, '5100000000000000', 46678);
INSERT INTO `Credit` (`ID`, `crno`, `balance`) VALUES (3, '4233365789898990', 992);
INSERT INTO `Credit` (`ID`, `crno`, `balance`) VALUES (4, '41325848329480', 214288);
INSERT INTO `Credit` (`ID`, `crno`, `balance`) VALUES (5, '5305678392249550', 0);
INSERT INTO `Credit` (`ID`, `crno`, `balance`) VALUES (6, '41234623679630', 799897782);
INSERT INTO `Credit` (`ID`, `crno`, `balance`) VALUES (7, '5500000000000000', 0);
INSERT INTO `Credit` (`ID`, `crno`, `balance`) VALUES (12, '5134435890444460', 0);
INSERT INTO `Credit` (`ID`, `crno`, `balance`) VALUES (15, '5128583759205290', 5000);
INSERT INTO `Credit` (`ID`, `crno`, `balance`) VALUES (22, '535956065940', 200);
INSERT INTO `Credit` (`ID`, `crno`, `balance`) VALUES (24, '5359560659406', 4545);
INSERT INTO `Credit` (`ID`, `crno`, `balance`) VALUES (27, '535956065941', 4545);
INSERT INTO `Credit` (`ID`, `crno`, `balance`) VALUES (31, '12345678', 1234);
INSERT INTO `Credit` (`ID`, `crno`, `balance`) VALUES (32, '12', 0);
INSERT INTO `Credit` (`ID`, `crno`, `balance`) VALUES (34, '23432', 0);
INSERT INTO `Credit` (`ID`, `crno`, `balance`) VALUES (35, '232', 0);
INSERT INTO `Credit` (`ID`, `crno`, `balance`) VALUES (36, '3434322', 42343);
INSERT INTO `Credit` (`ID`, `crno`, `balance`) VALUES (37, '45', 45);
INSERT INTO `Credit` (`ID`, `crno`, `balance`) VALUES (38, '453', 3543);
INSERT INTO `Credit` (`ID`, `crno`, `balance`) VALUES (39, '2322', 2321);
INSERT INTO `Credit` (`ID`, `crno`, `balance`) VALUES (40, '13', 0);
INSERT INTO `Credit` (`ID`, `crno`, `balance`) VALUES (41, 'rtyrty', 0);
# 21 records

#
# Table structure for table 'Customer'
#

DROP TABLE IF EXISTS `Customer`;

CREATE TABLE `Customer` (
  `ID` INTEGER NOT NULL AUTO_INCREMENT, 
  `uname` VARCHAR(15), 
  `passw` VARCHAR(15), 
  `fname` VARCHAR(15), 
  `mname` VARCHAR(15), 
  `lname` VARCHAR(15), 
  `email` VARCHAR(30), 
  `address` VARCHAR(70), 
  `phno` VARCHAR(12), 
  `cityid` INTEGER, 
  `crid` TINYINT(3) UNSIGNED, 
  `lastvisit` TIMESTAMP DEFAULT CURRENT_TIMESTAMP, 
  `noofvisits` INTEGER DEFAULT 0, 
  `Totaltkt` INTEGER DEFAULT 0, 
  INDEX (`cityid`), 
  INDEX (`crid`), 
  INDEX (`ID`), 
  PRIMARY KEY (`ID`)
) ENGINE=myisam DEFAULT CHARSET=utf8;

SET autocommit=1;

#
# Dumping data for table 'Customer'
#

INSERT INTO `Customer` (`ID`, `uname`, `passw`, `fname`, `mname`, `lname`, `email`, `address`, `phno`, `cityid`, `crid`, `lastvisit`, `noofvisits`, `Totaltkt`) VALUES (1, 'Admin', 'Admin', 'admin', NULL, 'admin', 'jay.kapasi@yahoo.co.in', NULL, NULL, 1, 1, '2009-02-27 00:10:51', 239, 78);
INSERT INTO `Customer` (`ID`, `uname`, `passw`, `fname`, `mname`, `lname`, `email`, `address`, `phno`, `cityid`, `crid`, `lastvisit`, `noofvisits`, `Totaltkt`) VALUES (23, 'Selina', 'arvind65', 'Selina', 'Arvindkumar', 'Shah', 'ss@mmk.yahoo.com', 'A-345 shemaroo complex\nNew link Road\nMumbai,230005', '804234323432', 4, 15, '2008-12-15 00:08:08', 2, 0);
INSERT INTO `Customer` (`ID`, `uname`, `passw`, `fname`, `mname`, `lname`, `email`, `address`, `phno`, `cityid`, `crid`, `lastvisit`, `noofvisits`, `Totaltkt`) VALUES (25, 'sameer', '', NULL, NULL, NULL, 'smt131@yahoo.co.in', 'None', '9898765434', 1, 22, '2008-12-15 00:00:00', 0, 0);
INSERT INTO `Customer` (`ID`, `uname`, `passw`, `fname`, `mname`, `lname`, `email`, `address`, `phno`, `cityid`, `crid`, `lastvisit`, `noofvisits`, `Totaltkt`) VALUES (26, 'sorryman', '', NULL, NULL, NULL, 'none', 'heaven', '099999999999', 5, 27, '2008-12-15 00:00:00', 0, 0);
# 4 records

#
# Table structure for table 'Film'
#

DROP TABLE IF EXISTS `Film`;

CREATE TABLE `Film` (
  `ID` INTEGER NOT NULL AUTO_INCREMENT, 
  `Name` VARCHAR(100), 
  `Story` LONGTEXT, 
  `Image` VARCHAR(30), 
  `Trailer` VARCHAR(50), 
  `Cast` LONGTEXT, 
  `Category` VARCHAR(30), 
  INDEX (`ID`), 
  PRIMARY KEY (`ID`)
) ENGINE=myisam DEFAULT CHARSET=utf8;

SET autocommit=1;

#
# Dumping data for table 'Film'
#

INSERT INTO `Film` (`ID`, `Name`, `Story`, `Image`, `Trailer`, `Cast`, `Category`) VALUES (1, 'A Wednesday', 'Mumbai, the financial capital of !India, the city that never sleeps, the city of dreams, fast paced and ever changing, home to Bollywood!\n<br>A Wednesday, tells the story of certain events that unfold between 2 and 6 pm on a particular Wednesday in this city. Events which do not exist in any record but which deeply affect the lives of those involved.\n<br>Prakash Rathod, Commisioner of Police, Mumbai,gets a call demanding the release of four extremely dangerous militants within the next four hours.If it doesnot happen several bombs planted across the city would blow up.He has to make a choice between releasing the militants,who are responsible for the unaccountable damage to civilian lives and property and might even cause further irreparable damage or let Mumbai be ripped apart by blasts again.\n<br>Prakash Rathod is not a man who would give up easily. He lives no stone unturned in order to track down the man who held the city at ransom. He gets a team of his best men together and taps all his resources. He steps up security in all public places airport, stations, malls and multiplexes. A hacker is brought in to trace the calls and the location of the man, but they are always a step behind .Prakash decides that he cannot put innumerable lives at stake and thus hand picks two of his officers Arif Khan and Jai Singh to do the handover of the millitants. It is then that events take a wild turn. Prakash Rathod and his team are confronted with an unimaginable and impossible situation. \n\n<br>It is this turn of events that leaves behind an unforgettable memory!\n\n<br>There is a reason why it has been kept a closely guarded secret!\n\n<br>There is a reason why this case has no written evidence!\n\n<br>There is a reason..... for everthing!', 'wednesday.jpg', 'wednesday.flv', '<b>Director:</b>\nNeeraj Pandey<br>\n \n<b>Cast</b>\nNaseerudin Shah\nAnupam Kher\nJimmy Shergill\nAamir Bashir\nDeepal Shaw\nChetan Pandit<br>\n \n<b>Producer</b>\nShital Bhatia\nAnjum Rizvi\nRonnie Screwvala', 'Thriller');
INSERT INTO `Film` (`ID`, `Name`, `Story`, `Image`, `Trailer`, `Cast`, `Category`) VALUES (2, 'WALL-E', 'In the distant future, a small waste collecting robot,inadvertently embarks on a space journey that will \nultimately decide the fate of mankind       \n', 'walle.jpg', 'walle.flv', '<b>DIRECTOR:</b> Andrew Stanton<br>\n<b>SCREENWRITER:</b> Andrew Stanton<br>\n<b>ORIGINAL MUSIC:</b> Thomas Newman<br>                                     <b>CINEMATOGRAPHER:</b>Animation<br>\n<b>CAST:</b> Animation<br>\n<b>STUDIO/PRODUCER:</b> Walt Disney / Pixar Animation', 'Animation');
INSERT INTO `Film` (`ID`, `Name`, `Story`, `Image`, `Trailer`, `Cast`, `Category`) VALUES (3, '1920', 'The year is 1920 and the house is isolated in the wilderness has a secret.It is waiting for the curse to come true. For years everyone who has bought the house and tried to pull it down has died under strange circumstances.It is like the house has a will and a life of its own.Arjun (Rajneesh Duggal) and his wife Lisa (Adah Sharma) move into the house and he has been given the task of pulling it down and making a hotel there. The haunting begins. Strange and inexplicable events start taking place. The curse says they will not survive. The only thing they have that is true is the love they once shared, which is now under the shadow of doubt. They will have to depend on the love and faith if they are to come out of this alive.', '1920.jpg', '1920.flv', '<b>Director:</b>Vikram Bhatt<br>\n<b>Cast:</b> Rajneesh Duggal, Barkha Bhist, Dilip Thadeshwar, Amita Bishnoi, Vipin Sharma <br>\n<b>Producer:</b>Mrs. Bhagwati Gabrani, Surendra Sharma, Amita Bishnoi <br>\n<b>Music :</b> Adnan Sami ', 'Horror');
INSERT INTO `Film` (`ID`, `Name`, `Story`, `Image`, `Trailer`, `Cast`, `Category`) VALUES (4, 'The Dark Knight Why So Serious?', 'Batman, Gordon and Harvey Dent are forced to deal with the chaos unleashed by an anarchist mastermind known only as the Joker, as it drives each of them to their limits.', 'dknight.jpg', 'dknight.flv', '<b>DIRECTOR:</b> Christopher Nolan<br>\n<b>CAST:</b> Christian Bale, Heath Ledger, Aaron Eckhart, Michael Caine,Gary Oldman, Maggie Gyllenhaal, Morgan Freeman, Eric Roberts<br>\n<b>STUDIO/PRODUCER:</b> Warner Home Video ', 'Action');
INSERT INTO `Film` (`ID`, `Name`, `Story`, `Image`, `Trailer`, `Cast`, `Category`) VALUES (5, 'Harry Potter And The Half-Blood Prince', 'Harry Potter\"s sixth year at Hogwarts turns out to be quite the exciting year. First off is the arrival of a new teacher at Hogwarts, Horace Slughorn, who is a bit more useful to Harry than he realizes. Next, Harry obtains a Potions book which used to be belong to the very mysterious Half-Blood Prince. Harry finds that the Half-Blood Prince\"s ancient scribbles are written along the margins of almost every page, giving Harry advice on how to improve greatly on his Potions work, and also teaching him a few helpful (and dangerous) spells along the way.\n<p>Amidst this, Harry is starting private lessons with Professor Dumbledore, during which Harry learns the dark secrets of Voldemort\"s past, hoping that they could use these secrets to find a way to defeat him.\n<p>Throughout all the school drama, however, the obvious darkness of Voldemort\"s impending rise to power is always apparent. The incredible action-packed climax is sure to leave the audience stunned and, inevitably, prove that you shouldn\"t trust everybody who you think is good, and also prove that not everyone can manage to survive.', 'hp6.jpg', 'hp6.flv', '<b>Director:</b>David Yates <br/>\n<b>Writers</b>:Steve Kloves (screenplay),J.K. Rowling (novel)<br/>\n<b>Cast :</b>Daniel Radcliffe,Emma Watson,Rupert Grint,Michael Gambon,Tom Felton', 'Mystery ');
# 5 records

#
# Table structure for table 'Schedule'
#

DROP TABLE IF EXISTS `Schedule`;

CREATE TABLE `Schedule` (
  `ID` INTEGER NOT NULL AUTO_INCREMENT, 
  `ScreenID` INTEGER, 
  `ShowDate` DATETIME, 
  `FilmID` INTEGER, 
  INDEX (`FilmID`), 
  PRIMARY KEY (`ID`), 
  INDEX (`ScreenID`)
) ENGINE=myisam DEFAULT CHARSET=utf8;

SET autocommit=1;

#
# Dumping data for table 'Schedule'
#

INSERT INTO `Schedule` (`ID`, `ScreenID`, `ShowDate`, `FilmID`) VALUES (1, 1, '2008-12-17 00:00:00', 2);
INSERT INTO `Schedule` (`ID`, `ScreenID`, `ShowDate`, `FilmID`) VALUES (2, 1, '2008-12-08 00:00:00', 3);
INSERT INTO `Schedule` (`ID`, `ScreenID`, `ShowDate`, `FilmID`) VALUES (3, 1, '2008-12-08 00:00:00', 2);
INSERT INTO `Schedule` (`ID`, `ScreenID`, `ShowDate`, `FilmID`) VALUES (4, 1, '2008-10-22 00:00:00', 4);
INSERT INTO `Schedule` (`ID`, `ScreenID`, `ShowDate`, `FilmID`) VALUES (6, 4, '2008-12-18 00:00:00', 1);
INSERT INTO `Schedule` (`ID`, `ScreenID`, `ShowDate`, `FilmID`) VALUES (8, 4, '2008-12-19 00:00:00', 1);
INSERT INTO `Schedule` (`ID`, `ScreenID`, `ShowDate`, `FilmID`) VALUES (9, 4, '2008-12-27 00:00:00', 1);
INSERT INTO `Schedule` (`ID`, `ScreenID`, `ShowDate`, `FilmID`) VALUES (10, 1, '2009-01-25 00:00:00', 1);
INSERT INTO `Schedule` (`ID`, `ScreenID`, `ShowDate`, `FilmID`) VALUES (11, 4, '2009-01-30 00:00:00', 2);
INSERT INTO `Schedule` (`ID`, `ScreenID`, `ShowDate`, `FilmID`) VALUES (12, 3, '2009-01-30 00:00:00', 1);
INSERT INTO `Schedule` (`ID`, `ScreenID`, `ShowDate`, `FilmID`) VALUES (13, 3, '2009-01-30 00:00:00', 1);
# 11 records

#
# Table structure for table 'Screen'
#

DROP TABLE IF EXISTS `Screen`;

CREATE TABLE `Screen` (
  `ID` INTEGER NOT NULL AUTO_INCREMENT, 
  `No` INTEGER, 
  `CinemaID` INTEGER, 
  `TimeID` INTEGER, 
  INDEX (`CinemaID`), 
  PRIMARY KEY (`ID`), 
  INDEX (`TimeID`)
) ENGINE=myisam DEFAULT CHARSET=utf8;

SET autocommit=1;

#
# Dumping data for table 'Screen'
#

INSERT INTO `Screen` (`ID`, `No`, `CinemaID`, `TimeID`) VALUES (1, 1, 1, 2);
INSERT INTO `Screen` (`ID`, `No`, `CinemaID`, `TimeID`) VALUES (2, 2, 1, 3);
INSERT INTO `Screen` (`ID`, `No`, `CinemaID`, `TimeID`) VALUES (3, 3, 1, 1);
INSERT INTO `Screen` (`ID`, `No`, `CinemaID`, `TimeID`) VALUES (4, 1, 2, 2);
# 4 records

#
# Table structure for table 'State'
#

DROP TABLE IF EXISTS `State`;

CREATE TABLE `State` (
  `ID` INTEGER NOT NULL AUTO_INCREMENT, 
  `Name` VARCHAR(25), 
  `CountryID` INTEGER, 
  INDEX (`CountryID`), 
  PRIMARY KEY (`ID`)
) ENGINE=myisam DEFAULT CHARSET=utf8;

SET autocommit=1;

#
# Dumping data for table 'State'
#

INSERT INTO `State` (`ID`, `Name`, `CountryID`) VALUES (1, 'Gujarat', 1);
INSERT INTO `State` (`ID`, `Name`, `CountryID`) VALUES (2, 'Maharashtra', 1);
INSERT INTO `State` (`ID`, `Name`, `CountryID`) VALUES (3, 'Delhi', 1);
INSERT INTO `State` (`ID`, `Name`, `CountryID`) VALUES (4, 'Andhra Pradesh', 1);
INSERT INTO `State` (`ID`, `Name`, `CountryID`) VALUES (5, 'West bengal', 1);
INSERT INTO `State` (`ID`, `Name`, `CountryID`) VALUES (6, 'California', 3);
INSERT INTO `State` (`ID`, `Name`, `CountryID`) VALUES (7, 'Florida', 3);
INSERT INTO `State` (`ID`, `Name`, `CountryID`) VALUES (8, 'Washington', 3);
INSERT INTO `State` (`ID`, `Name`, `CountryID`) VALUES (9, 'Shanghai', 2);
INSERT INTO `State` (`ID`, `Name`, `CountryID`) VALUES (10, 'Beijing', 2);
INSERT INTO `State` (`ID`, `Name`, `CountryID`) VALUES (11, 'Sydney', 4);
INSERT INTO `State` (`ID`, `Name`, `CountryID`) VALUES (12, 'Tokyo', 5);
INSERT INTO `State` (`ID`, `Name`, `CountryID`) VALUES (13, 'London', 6);
INSERT INTO `State` (`ID`, `Name`, `CountryID`) VALUES (14, 'Paris', 7);
# 14 records

#
# Table structure for table 'Ticket'
#

DROP TABLE IF EXISTS `Ticket`;

CREATE TABLE `Ticket` (
  `ID` INTEGER NOT NULL, 
  `customerid` INTEGER, 
  `ScheduleID` INTEGER, 
  `Seats` VARCHAR(50), 
  `Quantity` INTEGER, 
  `amount` INTEGER, 
  `SoldDate` DATETIME, 
  `Timeslot` VARCHAR(1), 
  UNIQUE (`ID`), 
  INDEX (`customerid`), 
  PRIMARY KEY (`ID`), 
  INDEX (`ScheduleID`)
) ENGINE=myisam DEFAULT CHARSET=utf8;

SET autocommit=1;

#
# Dumping data for table 'Ticket'
#

INSERT INTO `Ticket` (`ID`, `customerid`, `ScheduleID`, `Seats`, `Quantity`, `amount`, `SoldDate`, `Timeslot`) VALUES (1, 1, 1, '41;45;', 2, 200, '2008-10-20 13:19:10', '1');
INSERT INTO `Ticket` (`ID`, `customerid`, `ScheduleID`, `Seats`, `Quantity`, `amount`, `SoldDate`, `Timeslot`) VALUES (2, 1, 1, '1;2;3;4;5;', 5, 375, '2008-10-20 22:26:08', '2');
INSERT INTO `Ticket` (`ID`, `customerid`, `ScheduleID`, `Seats`, `Quantity`, `amount`, `SoldDate`, `Timeslot`) VALUES (3, 1, 1, '26;27;28;29;30;', 5, 375, '2008-10-20 22:34:51', '2');
INSERT INTO `Ticket` (`ID`, `customerid`, `ScheduleID`, `Seats`, `Quantity`, `amount`, `SoldDate`, `Timeslot`) VALUES (4, 1, 1, '87;89;88;90;91;', 5, 625, '2008-10-20 23:33:38', '1');
INSERT INTO `Ticket` (`ID`, `customerid`, `ScheduleID`, `Seats`, `Quantity`, `amount`, `SoldDate`, `Timeslot`) VALUES (5, 1, 1, '7;9;8;10;11;', 5, 375, '2008-10-20 23:34:50', '1');
INSERT INTO `Ticket` (`ID`, `customerid`, `ScheduleID`, `Seats`, `Quantity`, `amount`, `SoldDate`, `Timeslot`) VALUES (6, 1, 4, '88;89;90;91;92;', 5, 625, '2008-10-21 16:49:05', '1');
INSERT INTO `Ticket` (`ID`, `customerid`, `ScheduleID`, `Seats`, `Quantity`, `amount`, `SoldDate`, `Timeslot`) VALUES (7, 1, 4, '68;69;70;71;72;', 5, 500, '2008-10-21 16:54:08', '1');
INSERT INTO `Ticket` (`ID`, `customerid`, `ScheduleID`, `Seats`, `Quantity`, `amount`, `SoldDate`, `Timeslot`) VALUES (8, 3, 4, '8;9;10;11;12;', 5, 375, '2008-10-21 17:40:52', '1');
INSERT INTO `Ticket` (`ID`, `customerid`, `ScheduleID`, `Seats`, `Quantity`, `amount`, `SoldDate`, `Timeslot`) VALUES (9, 3, 4, '28;29;30;31;32;', 5, 375, '2008-10-21 17:44:49', '1');
INSERT INTO `Ticket` (`ID`, `customerid`, `ScheduleID`, `Seats`, `Quantity`, `amount`, `SoldDate`, `Timeslot`) VALUES (10, 1, 1, '31;32;33;34;35;', 5, 375, '2008-12-08 21:50:39', '1');
INSERT INTO `Ticket` (`ID`, `customerid`, `ScheduleID`, `Seats`, `Quantity`, `amount`, `SoldDate`, `Timeslot`) VALUES (11, 1, 1, '27;28;29;30;', 4, 300, '2008-12-08 21:58:11', '1');
INSERT INTO `Ticket` (`ID`, `customerid`, `ScheduleID`, `Seats`, `Quantity`, `amount`, `SoldDate`, `Timeslot`) VALUES (12, 1, 1, '51;52;53;54;55;', 5, 500, '2008-12-08 21:59:08', '2');
INSERT INTO `Ticket` (`ID`, `customerid`, `ScheduleID`, `Seats`, `Quantity`, `amount`, `SoldDate`, `Timeslot`) VALUES (13, 1, 1, '70;91;90;71;91;', 5, 575, '2008-12-08 22:00:28', '2');
INSERT INTO `Ticket` (`ID`, `customerid`, `ScheduleID`, `Seats`, `Quantity`, `amount`, `SoldDate`, `Timeslot`) VALUES (14, 1, 1, '2;43;48;82;76;', 5, 500, '2008-12-13 10:26:21', '1');
INSERT INTO `Ticket` (`ID`, `customerid`, `ScheduleID`, `Seats`, `Quantity`, `amount`, `SoldDate`, `Timeslot`) VALUES (15, 1, 1, '68;67;69;71;70;', 5, 500, '2008-12-15 00:22:02', '1');
INSERT INTO `Ticket` (`ID`, `customerid`, `ScheduleID`, `Seats`, `Quantity`, `amount`, `SoldDate`, `Timeslot`) VALUES (16, 1, 1, '63;64;', 2, 200, '2008-12-17 22:01:41', '2');
INSERT INTO `Ticket` (`ID`, `customerid`, `ScheduleID`, `Seats`, `Quantity`, `amount`, `SoldDate`, `Timeslot`) VALUES (17, 1, 6, '1;3;2;5;4;', 5, 375, '2008-12-18 23:42:57', '1');
INSERT INTO `Ticket` (`ID`, `customerid`, `ScheduleID`, `Seats`, `Quantity`, `amount`, `SoldDate`, `Timeslot`) VALUES (18, 1, 8, '47;48;49;50;51;', 5, 500, '2008-12-19 00:01:19', '1');
INSERT INTO `Ticket` (`ID`, `customerid`, `ScheduleID`, `Seats`, `Quantity`, `amount`, `SoldDate`, `Timeslot`) VALUES (19, 1, 13, '46;49;48;47;50;', 5, 500, '2009-01-30 17:32:54', '3');
# 19 records

#
# Table structure for table 'tTime'
#

DROP TABLE IF EXISTS `tTime`;

CREATE TABLE `tTime` (
  `ID` INTEGER NOT NULL, 
  `SlotNo` VARCHAR(1) NOT NULL, 
  `Slot` DATETIME, 
  INDEX (`ID`), 
  PRIMARY KEY (`ID`, `SlotNo`)
) ENGINE=myisam DEFAULT CHARSET=utf8;

SET autocommit=1;

#
# Dumping data for table 'tTime'
#

INSERT INTO `tTime` (`ID`, `SlotNo`, `Slot`) VALUES (1, '1', '1899-12-30 11:00:00');
INSERT INTO `tTime` (`ID`, `SlotNo`, `Slot`) VALUES (1, '2', '1899-12-30 14:00:00');
INSERT INTO `tTime` (`ID`, `SlotNo`, `Slot`) VALUES (1, '3', '1899-12-30 17:00:00');
INSERT INTO `tTime` (`ID`, `SlotNo`, `Slot`) VALUES (1, '4', '1899-12-30 20:00:00');
INSERT INTO `tTime` (`ID`, `SlotNo`, `Slot`) VALUES (2, '1', '1899-12-30 10:00:00');
INSERT INTO `tTime` (`ID`, `SlotNo`, `Slot`) VALUES (2, '2', '1899-12-30 13:00:00');
INSERT INTO `tTime` (`ID`, `SlotNo`, `Slot`) VALUES (2, '3', '1899-12-30 16:00:00');
INSERT INTO `tTime` (`ID`, `SlotNo`, `Slot`) VALUES (2, '4', '1899-12-30 19:00:00');
INSERT INTO `tTime` (`ID`, `SlotNo`, `Slot`) VALUES (3, '1', '1899-12-30 11:30:00');
INSERT INTO `tTime` (`ID`, `SlotNo`, `Slot`) VALUES (3, '2', '1899-12-30 14:00:00');
INSERT INTO `tTime` (`ID`, `SlotNo`, `Slot`) VALUES (3, '3', '1899-12-30 16:30:00');
INSERT INTO `tTime` (`ID`, `SlotNo`, `Slot`) VALUES (3, '4', '1899-12-30 19:00:00');
INSERT INTO `tTime` (`ID`, `SlotNo`, `Slot`) VALUES (4, '1', '1899-12-30 10:30:00');
INSERT INTO `tTime` (`ID`, `SlotNo`, `Slot`) VALUES (4, '2', '1899-12-30 12:15:00');
INSERT INTO `tTime` (`ID`, `SlotNo`, `Slot`) VALUES (4, '3', '1899-12-30 15:15:00');
INSERT INTO `tTime` (`ID`, `SlotNo`, `Slot`) VALUES (4, '4', '1899-12-30 19:30:00');
INSERT INTO `tTime` (`ID`, `SlotNo`, `Slot`) VALUES (5, '1', '1899-12-30 07:30:00');
# 17 records


