--[[---------------------------------------------------------------------------
DarkRP custom jobs
---------------------------------------------------------------------------

This file contains your custom jobs.
This file should also contain jobs from DarkRP that you edited.

Note: If you want to edit a default DarkRP job, first disable it in darkrp_config/disabled_defaults.lua
	Once you've done that, copy and paste the job to this file and edit it.

The default jobs can be found here:
https://github.com/FPtje/DarkRP/blob/master/gamemode/config/jobrelated.lua

For examples and explanation please visit this wiki page:
http://wiki.darkrp.com/index.php/DarkRP:CustomJobFields


Add jobs under the following line:
---------------------------------------------------------------------------]]


TEAM_LAWYER = AddExtraTeam("Lawyer", {
	color = Color(100, 150, 200, 255),
	model = "models/player/hostage/hostage_04.mdl",
	description = [[As a lawyer you are responsible for fighting
	on your clints behalf this includes bailing him out of jail and or
	pvp confrontation. ]],
	weapons = {"unarrest_stick", "hl2_combo_fists"},
	command = "lawyer",
	max = 3,
	salary = 60,
	admin = 0,
	vote = true,
	hasLicense = false
})

TEAM_POLICE = AddExtraTeam("Police Officer", {
	color = Color(25, 25, 170, 255),
	model = "models/player/police.mdl",
	description = [[The protector of every citizen that lives in the city .
		You have the power to arrest criminals and protect innocents.
		Hit them with your arrest baton to put them in jail
		Bash them with a stunstick and they might learn better than to disobey
		the law.
		The Battering Ram can break down the door of a criminal with a warrant
		for his/her arrest.
		The Battering Ram can also unfreeze frozen props(if enabled).
		Type /wanted <name> to alert the public to this criminal
		OR go to tab and warrant someone by clicking the warrant button. ]],
	weapons = {"arrest_stick", "unarrest_stick", "weapon_mad_glock", "stunstick", "door_ram", "weaponchecker"},
	command = "cp",
	max = 4,
	salary = 50,
	admin = 0,
	vote = true,
	hasLicense = true
})

TEAM_CHIEF = AddExtraTeam("Police Sergeant", {
	color = Color(20, 20, 255, 255),
	model = "models/player/combine_soldier_prisonguard.mdl",
	description = [[The Chief is the leader of the Police Officer's unit.
		Coordinate the police forces to bring law to the city
		Hit them with arrest baton to put them in jail
		Bash them with a stunstick and they might learn better than to
		disobey the law.
		The Battering Ram can break down the door of a criminal with a
		warrant for his/her arrest.
		Type /wanted <name> to alert the public to this criminal
		Type /jailpos to set the Jail Position. ]],
	weapons = {"arrest_stick", "unarrest_stick", "weapon_mad_p228", "stunstick", "door_ram", "weaponchecker"},
	command = "chief",
	max = 1,
	salary = 60,
	admin = 0,
	vote = false,
	hasLicense = true,
	NeedToChangeFrom = TEAM_POLICE
})

TEAM_MAYOR = AddExtraTeam("Mayor", {
	color = Color(150, 20, 20, 255),
	model = "models/player/breen.mdl",
	description = [[The Mayor of the city creates laws to serve the greater
	good of the people.
	If you are the mayor you may create and accept warrants.
	Type /wanted <name>  to warrant a player
	Type /jailpos to set the Jail Position
	Type /lockdown initiate a lockdown of the city.
	Everyone must be inside during a lockdown.
	The cops patrol the area
	/unlockdown to end a lockdown. ]],
	weapons = {},
    command = "mayor",
	max = 1,
	salary = 100,
	admin = 0,
	vote = true,
	hasLicense = false
})

TEAM_SS = AddExtraTeam("Secret Service", {
	color = Color(255, 10, 10, 255),
	model = "models/player/combine_soldier.mdl",
	description = [[As a secret service agent, it is your job to make sure the
	mayor is safe under any Circumstances. But you are still under
	the authority of the police chief. ]],
	weapons = {"weapon_mad_p228", "hl2_combo_fists", "weapon_mad_mp5"},
	command = "secretservice",
	max = 2,
	salary = 50,
	admin = 0,
	vote = true,
	hasLicense = true
})

TEAM_GUN = AddExtraTeam("Gun Dealer", {
	color = Color(255, 140, 0, 255),
	model = "models/player/hostage/hostage_02.mdl",
	description = [[As a gun dealer it is your job to sell light weaponry
	to all jobs. The guns prices are at your disposal. ]],
	weapons = {"hl2_combo_fists"},
	command = "gundealer",
	max = 3,
	salary = 45,
	admin = 0,
	vote = false,
	hasLicense = true
})

TEAM_BOUNTY = AddExtraTeam("Bounty Hunter", {
	color = Color(125, 125, 256, 252),
	model = "models/player/Group01/Female_02.mdl",
	description = [[As a bounty hunter its your job to find wanted players and
	take them down to the station. ]],
	weapons = {"hl2_combo_fists"},
	command = "bounty",
	max = 1,
	salary = 50,
	admin = 0,
	vote = false,
	hasLicense = true
})

TEAM_HIT = AddExtraTeam("Hit Man", {
	color = Color(125, 125, 225, 212),
	model = "models/player/group02/male_08.mdl",
	description = [[As a hit man its your job to kill the players
	that have a "hit" on them. ]],
	weapons = {"hl2_combo_fists", "weapon_mad_auto_glock"},
	command = "hitman",
	max = 1,
	salary = 35,
	admin = 0,
	vote = false,
	hasLicense = false
})

TEAM_FIGHT = AddExtraTeam("Fight Club Manager", {
	color = Color(125, 125, 200, 255),
	model = "models/player/Group01/male_02.mdl",
	description = [[As a fight club manager you can set up your fight club
	on any state you buy. Both players must agree to the fight clubs terms
	before any pvp fights occur. ]],
	weapons = {"hl2_combo_fists"},
	command = "fight",
	max = 1,
	salary = 45,
	admin = 0,
	vote = false,
	hasLicense = false
})

TEAM_HOBO = AddExtraTeam("Hobo", {
	color = Color(80, 45, 0, 255),
	model = "models/player/zombie_fast.mdl",
	description = [[The lowest member of society. All people see you laugh.
		You have no home.
		Beg for your food and money
		Sing for everyone who passes to get money
		Make your own wooden home somewhere in a corner or
		outside someone else's door ]],
	weapons = {"hl2_combo_fists", "weapon_bugbait", "rp_pickpocket"},
	command = "hobo",
	max = 4,
	salary = 0,
	admin = 0,
	vote = false,
	hasLicense = false
})

TEAM_BODYGUARD = AddExtraTeam("Body Guard", {
	color = Color(0,68,89,255),
	model = "models/player/odessa.mdl",
	description = [[As a bodyguard it is your job to protect your employer
	and his estate. ]],
	weapons = {"hl2_combo_fists"},
	command = "bodyguard",
	max = 2,
	salary = 60,
	admin = 0,
	vote = false,
	hasLicense = false
})

TEAM_MEDIC = AddExtraTeam("Doctor", {
	color = Color(47, 79, 79, 255),
	model = "models/player/kleiner.mdl",
	description = [[As a medic it is your job to see to people
	in need of health. It is up to you weather or not you charge
	for you service. ]],
	weapons = {"weapon_mad_medic", "hl2_combo_fists"},
	command = "doctor",
	max = 3,
	salary = 45,
	admin = 0,
	vote = false,
	hasLicense = false
})

TEAM_THIEF = AddExtraTeam("Thief", {
	color = Color(10, 255, 200, 255),
	model = "models/player/arctic.mdl",
	description = [[Your are a thief, Brake into peoples homes
and places of business to piss them off!
Take what you can and run!
You may not shoot if they ain't a threat. ]],
	SALARY:45,
	weapons = {"keypad_cracker", "lockpick", "hl2_combo_fists"},
	command = "thief",
	max = 3,
	salary = 45,
	admin = 0,
	vote = false,
	hasLicense = false
})

TEAM_PROTHIEF = AddExtraTeam("Pro Thief", {
	color = Color(111, 199, 175, 255),
	model = "models/player/arctic.mdl",
	description = [[Your are a pro thief, Brake into peoples homes
and places of business to piss them off!
Take what you can and run!
You may not shoot people in there own only in robbery.
homes or places of business. only in robbery.
to shoot you!. ]],	
	SALARY:60,
	weapons = {"fastkeypad_cracker", "fastlockpick", "hl2_combo_fists", "rp_pickpocket"},
	command = "prothief",
	max = 3,
	salary = 60,
	admin = 0,
	vote = false,
	hasLicense = false
})

TEAM_ITALIANMOBBOSS = AddExtraTeam("Italian Mob Boss", {
	color = Color(100, 128, 128, 128),
	model = "models/player/gman_high.mdl",
	description = [[As the italian mob boss you have the athority to
	tell the italian mobsters what to do. But be careful because
	police informent will be looking out for you ]],
	SALARY:50,
	weapons = {"hl2_combo_fists"},
	command = "italianmobboss",
	max = 1,
	salary = 50,
	admin = 0,
	vote = false,
	hasLicense = false
})

TEAM_ITALIANMOBSTER = AddExtraTeam("Italian Mobster", {
	color = Color(100, 100, 100, 255),
	model = "models/player/guerilla.mdl",
	description = [[You work for the Italian Mob boss,
You take orders from the Italian mob boss only. ]],
	weapons = {"hl2_combo_fists"},
	command = "italianmobster",
	max = 6,
	salary = 45,
	admin = 0,
	vote = false,
	hasLicense = false
})

TEAM_SWAT = AddExtraTeam("S.W.A.T", {
    color = Color(50, 90, 255, 255),
    model = "models/player/urban.mdl",
    description = [[ [Donator Job] As a S.W.A.T officer it is your
	job to infiltrate
	drug labs and and asisest police officers on high level raids.
	You are still under the athorty of the police cheif.]],
    weapons = {"weapon_mad_mp5", "arrest_stick", "door_ram", "stunstick", "unarrest_stick", "weaponchecker", "hl2_combo_fists", "weapon_mad_p228"},
    command = "swat",
    max = 3,
    salary = 100,
    admin = 0,
    vote = false,
    hasLicense = true
})

TEAM_SWATCO = AddExtraTeam("S.W.A.T Commander", {
    color = Color(10, 10, 100, 255),
    model = "models/player/urban.mdl",
    description = [[ [Donator Job] As a S.W.A.T Commander it is your
	job to infiltrate
	drug labs and and asisest police officers on high level raids.
	You are still under the athorty of the police cheif.]],
    weapons = {"arrest_stick", "unarrest_stick", "stunstick", "door_ram", "weaponchecker", "weapon_mad_m4", "hl2_combo_fists", "weapon_mad_deagle"},
    command = "swatco",
    max = 1,
    salary = 130,
    admin = 0,
    vote = false,
    hasLicense = true,
	NeedToChangeFrom = TEAM_SWAT
})


TEAM_NINJA = AddExtraTeam("Ninja", {
	color = Color(255, 93, 0, 255),
	model = "models/player/charple.mdl",
	description = [[As a ninja you can jump from building
	to building with you grapling hook. But be careful
	because grapling hook is not leagel. ]],
	weapons = {"hl2_combo_fists", "weapon_mad_knife", "parkourmod"},
	command = "ninja",
	max = 2,
	salary = 65,
	admin = 0,
	vote = false,
	hasLicense = false
})

TEAM_FBI = AddExtraTeam("F.B.I", {
	color = Color(50, 90, 255, 255),
	model = "models/player/riot.mdl",
	description = [[ [Gold Donator] As a F.B.I Special Agent its your job to find
	Terrorists and kill or arrest them. ]],
	weapons = {"hl2_combo_fists", "weapon_mad_m4", "weapon_mad_p228"},
	command = "fbi",
	max = 2,
	salary = 120,
	admin = 0,
	vote = true,
	hasLicense = false
})

TEAM_ADMIN = AddExtraTeam("Admin On Patrol", {
	color = Color(100, 100, 100, 255),
	model = {
	"models/player/combine_super_soldier.mdl",
	},
	description = [[Ban deez rule brekerz. ]],
	weapons = {"hl2_combo_fists"},
	command = "admin",
	max = 3,
	salary = 1000,
	admin = 1,
	vote = false,
	hasLicense = false,
        customCheck = function(ply)
             return ply:IsSuperAdmin() or ply:IsUserGroup("admin") or ply:IsUserGroup("sadmingolddonator") or ply:IsUserGroup("developer") or ply:IsUserGroup("trialadmin") or ply:IsUserGroup("junioradmin") or ply:IsUserGroup("trialadmingolddonator") 
        end
})

TEAM_OWNER = AddExtraTeam("Owner On Patrol", {
	color = Color(100, 100, 100, 255),
	model = {
	"models/player/combine_super_soldier.mdl",
	},
	description = [[Info]],
	weapons = {"hl2_combo_fists"},
	command = "owner",
	max = 1,
	salary = 1000,
	admin = 2,
	vote = false,
	hasLicense = false,
        customCheck = function(ply)
             return ply:IsUserGroup("owner")
			 end
})





--[[---------------------------------------------------------------------------
Define which team joining players spawn into and what team you change to if demoted
---------------------------------------------------------------------------]]
GAMEMODE.DefaultTeam = TEAM_CITIZEN


--[[---------------------------------------------------------------------------
Define which teams belong to civil protection
Civil protection can set warrants, make people wanted and do some other police related things
---------------------------------------------------------------------------]]
GAMEMODE.CivilProtection = {
	[TEAM_POLICE] = true,
	[TEAM_CHIEF] = true,
	[TEAM_MAYOR] = true,
}

--[[---------------------------------------------------------------------------
Jobs that are hitmen (enables the hitman menu)
---------------------------------------------------------------------------]]
DarkRP.addHitmanTeam(TEAM_HIT)
DarkRP.addHitmanTeam(TEAM_NINJA)
