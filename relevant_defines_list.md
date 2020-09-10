# NGame

COMBAT_TICK_LIMIT = 1

# NCharacter

RANDOM_CHARACTER_PROWESS_MIN = 0
RANDOM_CHARACTER_PROWESS_MAX = 10

# NOldAge

LOWER_PROWESS_START_AGE = 45 					// At this age characters start getting the chance to lose prowess each year
LOWER_PROWESS_BASE_CHANCE = 0.1					// This is the base chance of losing prowess at the START_AGE
LOWER_PROWESS_YEARLY_INCREASE = 0.015			// This is the yearly increase of the chance to lose prowess
LOWER_PROWESS_MAX_CHANCE = 0.75					// This is the maximum chance to lose prowess
LOWER_PROWESS_FACTOR = 0.1						// This is the prowess change mutliplier on each failed yearly roll

# NCharacterOpinion

// The offensive war opinion penalty is applied to all direct vassals
// It ticks up if you lead an offensive war that isn't a Great Holy War or a civil war
OFFENSIVE_WAR_PENALTY_GRACE_PERIOD = 6			// How many months do you need to be at war before you start getting the offensive war opinion penalty? If you've already got the penalty, the grace period is ignored (E.G., if you go to war for a few years, are at peace for a few months, then go to war again it will immediately start ticking up)
OFFENSIVE_WAR_PENALTY_PER_MONTH = 0.5			// How much of a penalty gets added each month?
OFFENSIVE_WAR_PENALTY_DECAY_PER_MONTH = 0.5		// How much of a penalty decays each month when no longer gaining it?
AT_PEACE_PENALTY_GRACE_PERIOD = 6				// How many months do you need to be at peace before you start getting the at peace opinion penalty? If you've already got the penalty, the grace period is ignored
AT_PEACE_PENALTY_PER_MONTH = 0.5				// How much of a penalty gets added each month?
AT_PEACE_PENALTY_CAP = 30						// The penalty will be capped to this value (the opinion will be at worst -AT_PEACE_PENALTY_CAP)

# NCombat

UNRAISED_LEVY_REGIMENTS_SPEED = 40.0			// How many distance units do unraised regiments travel per day when gathering
COMBAT_ROLL_DAYS = 3							// How many days are there between rolls?
COMBAT_EVENT_DAYS = 5							// How many days are there between knight events?
DEVIATION_FALLOFF = 0.1							// If the mean was clamped to ACTION_LEVELS, the standard deviation is decreased using this factor (the higher the value the faster the decrease)
WAR_ATTACKER_COMBAT_SCORE_SCALE = 50			// Scale factor for how much war score battles give to the war attacker. Can be overriden by CB
WAR_DEFENDER_COMBAT_SCORE_SCALE = 50			// Scale factor for how much war score battles give to the war defender. Can be overriden by CB
WAR_ATTACKER_COMBAT_MAX_SCORE = 50				// The maximum amount of warscore gained from a single battle by the war attacker
WAR_DEFENDER_COMBAT_MAX_SCORE = 50				// The maximum amount of warscore gained from a single battle by the war attacker
MANEUVER_PHASE_DAYS = 3							// How many days should the maneuver phase last
LEVY_TOUGHNESS = 10								// How much toughness does each levy soldier have
LEVY_ATTACK = 10								// How much attack does each levy soldier have
DAMAGE_SCALING_FACTOR = 0.03					// Scaling factor for dealing damage in combat
BASE_RATIO_CASUALTIES_CONVERSION = 0.3			// How many of the soft casualties should be converted to hard casualties during the main phase
PURSUIT_PHASE_DAYS = 3							// How many days should the pursuit phase be
ADVANTAGE_DAMAGE_SCALING_FACTOR = 2				// How much should the advantage affect damage given
BASE_WIDTH_RATIO = 1							// The base combat width is set by multiplying the size of the defender by this ratio
COMMANDER_MIN_ROLL = 0
COMMANDER_MAX_ROLL = 10
MEN_AT_ARMS_MAX_COUNTER = 0.9					// When RATIO_FOR_MAX_COUNTER is hit, the damage output for the MaA will be reduced by this much. For values lower, it'll be linear between 0 and this value
RATIO_FOR_MAX_COUNTER = 2.0						// You need this many effective regiment chunks to counter a single regiment chunk. Modified by counter effectiveness (E.G., = 2.0 in the MaA's counter section means twice as effective countering). So if stack size is 100, 50 men from a regiment with 2x counter will produce one point of countering. Thus if the ratio for max counter is 1.0, they'd fully counter a full-strength MaA chunk, or halfway counter two, etc.
MEN_AT_ARMS_COUNTER_MODIFICATION = 6			// A countered men at arms base type get this modification to all of their rolls
MIN_DAYS_BEFORE_MANUAL_RETREAT = 14				// Number of days before a retreat can be ordered
RANDOM_ADVANTAGE_MIN = -25						// The worst initial battle Advantage from the 'random_advantage' Trait modifier
RANDOM_ADVANTAGE_RANGE = 65						// The roll range from the 'random_advantage' Trait modifier
MINIMUM_COMBAT_WIDTH = 100						// Combat width cannot be smaller than this
BASE_RATIO_CASUALTIES_CONVERSION_PURSUIT = 1	// How many of the hard casualties inflicted on the retreating side should be converted to hard casualties during retreat. Interacts with BASE_TOUGHNESS_TO_PURSUIT and such
PURSUIT_STAT_TO_PURSUIT_DAMAGE = 0.5			// The pursuit stat is multiplied by this before being turned into actual damage
BASE_TOUGHNESS_TO_PURSUIT = 0.05				// This many % of the toughness of the retreater's soft casualties will turn into pursuit (during the full pursuit, not per day). Essentially, this means if neither side has screen or pursuit, 5% of the soft casualties will become hard casualties. More if the pursuer has more pursuit than the defender has screen, and vice versa
MINIMUM_PURSUIT_DAMAGE = 0.01					// High screen can't bring casualties below 1% in the pursuit phase
DISEMBARK_PENALTY_DAYS = 30						// How long does an army have a penalty after disembarking?
KNIGHT_DAMAGE_PER_PROWESS = 100					// How much "Damage" stat does a knight get per prowess?
KNIGHT_TOUGHNESS_PER_PROWESS = 10				// How much "Toughness" stat does a knight get per prowess?
COMBAT_RESULT_MONTHS_TO_TIMEOUT = 12			// Combat results timeout after this many months

# NArmy

MOVEMENT_SPEED_RETREAT = 4.5					// Movement speed while retreating
MOVEMENT_SPEED = 3								// Normal movement speed
MOVEMENT_SPEED_BONUS_FRIENDLY_AREA = 0.2		// In friendly areas you get a 20% speed bonus
REGIMENT_MONTHLY_REINFORCE_SPEED = 0.03			// Monthly reinforcement percentage of unraised chunks [0-1]
REGIMENT_MONTHLY_MAA_REINFORCE_SPEED = 0.1		// Monthly reinforcement percentage of unraised MAA chunks [0-1]
GOLD_COST_PER_SOLDIER = 0.0033					// Gold maintenance cost per soldier
RAID_ARMY_COST_MULT = 0.5						// Maintenance of raid armies is multiplied by this
MOVEMENT_LOCKED = 0.5							// Percentage after which movement is locked
COUNTY_MOVEMENT_ATTRITION_PERCENTAGE = 0.05
MINIMUM_COUNTY_MOVEMENT_ATTRITION = 100	
REGIMENT_DEFAULT_STACK_SIZE = 100
REGIMENT_DEFAULT_MAX_SIZE = 3					// Number of regiment chunks
REGIMENT_MAA_CAP_BY_TIER = { 0 1 2 3 4 5 }
REGIMENT_MAA_EXTRA_BY_CAP = 0.2					// Percentage [0-1] applied to each MAA regiment by each regiment above the cap
REGIMENT_MAA_SHOW_INFO_PERCENTAGE = 0.3
REGIMENT_MAA_STARTING_COUNT = 5
FULL_SUPPLY = 100								// Fully supplied units' supply value
SUPPLY_LOSS_AT_SEA = 8							// This is the supply loss at sea after the ATTRITION_AFTER_DAYS grace period
SUPPLY_LOSS_PER_SOLDIER_ABOVE_LIMIT = 0.01		// Each check's supply loss per every soldier over the province's supply limit
SUPPLY_LOSS_MINIMUM = 5							// This is the minimum supply limit loss (before commander effects)
SUPPLY_LOSS_MAXIMUM = 10						// This is the maximum supply limit loss (after commander effects)
SUPPLY_GAIN_BELOW_LIMIT = 20					// Each check's supply gain under or at the province's supply limit
SUPPLY_OWN_REALM = 0.15							// Extra supply within top realm
SUPPLY_OWN_SUB_REALM = 0.3						// Extra supply within subrealm
MINIMUM_SUPPLY_LIMIT = 1000						// Supply limit will never ever be lower than this
NO_SUPPLY_LOSS_DAYS = 30						// After gathering, armies won't lose supplies for this number of days

SUPPLY_STATE_LEVELS = {
	60
	10
	0
}

SUPPLY_STATE_NAMES = {
	"SUPPLY_STATE_0"
	"SUPPLY_STATE_1"
	"SUPPLY_STATE_2"
}

SUPPLY_STATE_ATTRITION = {
	0.0
	0.0
	0.05
}

MAA_PRESTIGE_BUY_COST_MULT = 2					// If using prestige as gold for MaA, multiply buy cost by this
MAA_PRESTIGE_LOW_COST_MULT = 0.7				// If using prestige as gold for MaA, multiply basic maintenance cost by this
MAA_PRESTIGE_HIGH_COST_MULT = 0.7				// If using prestige as gold for MaA, multiply raised/reinforce cost by this
REGIMENT_MAX_SIZE = 1000						// The game will avoid making regiments larger than this. Can still happen if a province provides more levies than the cap
REGIMENT_MAX_SIZE_PERCENT = 0.2					//  The game will avoid making regiments larger than this compared to the max troops you can raise

# NFleet

FLEET_SPEED = 15								// Fleet speed
EMBARK_GOLD_COST_PER_HUNDRED = 1				// Embark cost for every hundred units
GOLD_COST_MAINTENANCE_MULT = 0.25				// Increase in the gold maintenance for armies that are embarked
ATTRITION_AFTER_DAYS = 30						// After embarking the army can expend this time without getting attrition

# NRetreat

SHATTERED_RETREAT_PREFERRED_PROVINCES = 7
SHATTERED_RETREAT_MAX_PREFERRED_OFFSET_PENALTY = 7
SHATTERED_RETREAT_OWN_REALM = 340
SHATTERED_RETREAT_OWN_SUBREALM = 60
SHATTERED_RETREAT_OWN_CAPITAL = 100
SHATTERED_RETREAT_WAR_FRIEND = 200
SHATTERED_RETREAT_ENEMY = -250
SHATTERED_RETREAT_SAME_RELIGION = 30
SHATTERED_RETREAT_SAME_CULTURE = 10
SHATTERED_RETREAT_COASTAL = 10
SHATTERED_RETREAT_OCCUPIED = -60
SHATTERED_RETREAT_DISTANCE_MULTIPLIER = -50
SHATTERED_RETREAT_MAX_PROVINCES = 15
SHATTERED_RETREAT_NEIGHBOUR_UNIT_MULTIPLIER = 0.5
SHATTERED_RETREAT_OWN_UNIT_MULTIPLIER = 0.05
SHATTERED_RETREAT_ENEMY_UNIT_MULTIPLIER = -0.2
SHATTERED_RETREAT_DISTANCE_FROM_CAPITAL = -0.01

# NWar

ATTACKER_TICKING_WAR_SCORE = 0.055				// Default ticking war score per day for attackers. Can be overwritten by CB. Set to 0 to disable
ATTACKER_TICKING_WAR_SCORE_DELAY_DAYS = 0		// Default delay in days before applying ticking war score for attackers. Can be overwritten by CB
DEFENDER_TICKING_WAR_SCORE = 0.055				// Default ticking war score per day for defenders. Can be overwritten by CB. Set to 0 to disable
DEFENDER_TICKING_WAR_SCORE_DELAY_DAYS = 365		// Default delay in days before applying ticking war score for defenders. Can be overwritten by CB
ATTACKER_OCCUPATION_SCORE_SCALE = 90			// War score from occupation by the attacker is given by occupied territory ratio (0.0 ... 1.0) multiplied by this value. Can be overriden by CB
DEFENDER_OCCUPATION_SCORE_SCALE = 90			// War score from occupation by the defender is given by occupied territory ratio (0.0 ... 1.0) multiplied by this value. Can be overriden by CB
MAX_ATTACKER_BATTLES_WAR_SCORE = 50				// How much war score is it possible for the attacker to get from battles. Can be overriden by CB
MAX_DEFENDER_BATTLES_WAR_SCORE = 100			// How much war score is it possible for the defender to get from battles. Can be overriden by CB
MILITARY_RATIO_LEVELS = 5						// How many military ratio levels are there
OCCUPIED_CAPITAL_WAR_SCORE = 10					// Bonus war score from occupying the enemy capital
CAPTURED_VASSAL_WAR_SCORE = 0					// War Score for each direct vassal of the war leader
CAPTURED_SPOUSE_WAR_SCORE = 0					// War Score from capturing one or more spouses
CAPTURED_HEIR_WAR_SCORE = { 50 25 10 }			// War Score in order of succession
BATTLE_WAR_CONTRIBUTION_MULTIPLIER = 0.2		// War contribution from battles are multiplied with this value
SIEGE_WAR_CONTRIBUTION_MULTIPLIER = 10			// War contribution from sieges are multiplied with this value
OCCUPATION_WAR_CONTRIBUTION_MONTHLY = 2			// War contribution from monthly occupation of provinces
OCCUPATION_SCORE_PER_BARONY_SCALE = 0.04		// Extra occupation score (before scaling) from each individual barony. 0.01 is equivalent to 1% per barony. So 10 baronies occupied out of 20 total, would mean 50% + 10% = 60% occupation score (before scaling)
MINIMUM_CONTRIBUTION_FOR_REWARD = 100			// You need at least this amount of contribution points in order to get a reward
WAR_RESULT_MONTHS_TO_TIMEOUT = 12				// War results time out after this many months

# NReligion

HOSTILITY_COMBAT_MOD_MULT = {					// Multiplier to how big of an effect tolerance_advantage_mod has. The higher it is, the greater the effect
	0
	0
	0.005
	0.01
}

# NSiege

ACTIONS_TO_REMEMBER = 4								// How many previous siege actions are remembered
ACTION_WEIGHTS = {									// How likely are the the actions to be picked. The probability is given by the ratio of the weights.
	40		// breach
	15		// starvation
	15		// disease
	10		// desertion
	20		// stalemate
}
BASE_DEFENDER_MORALE = 100							// Defender morale with no buildings, garrison etc
DEFENDER_MORALE_PER_FORT_LEVEL = 50					// Defender morale added to the base per for level
BASE_DAILY_MORALE_LOSS = 1							// How much morale is lost every day of the siege
MIN_DAILY_MORALE_LOSS = 0.5							// Minimum daily morale loss for the defenders
DAILY_MORALE_LOSS_FROM_RELATIVE_ATTACKER_MEN = 0.01	// How much morale is lost every day of the siege for extra stack of men defined in RELATIVE_ATTACKER_MEN_STACK_SIZE
RELATIVE_ATTACKER_MEN_STACK_SIZE = 200				// Extra stack size of men to start getting daily morale loss
MONTHLY_ATTRITION = 0.01							// Monthly attrition during siege
BASE_SIEGE_PHASE_LENGTH = 20						// Base length of a siege phase (time between picking new actions) in days
BREACH_PHASE_TIMER_LEVELS = {						// How many levels of breach are there and how much (as percentage) is the phase timer reduced by these levels.
	-0.1
	-0.3
}
BREACH_WEIGHT_PER_FORT_TIER = 2.0					// How much breach weight does each level of fort remove? Siege weight is the ACTION_WEIGHT, times the max siege tier in the attacking army, minus fort level \* BREACH_WEIGHT_PER_FORT_TIER
BREACH_ASSAULT_TICK_PERCENTAGE_CASULATIES = {		// How many casualties will the assaultin armies receive based on the breach level
	2.5
	1
}
BREACH_ASSAULT_PROGRESS_CHUNK = 100					// How many mens take an impact in the assault (rounds up)
BREACH_ASSAULT_PROGRESS_PER_CHUNK = 0.2				// How much impact in assault will have every chunk
STARVATION_MORALE_LEVELS = {						// How many levels of starvation are there, and how much morale does the defender lose (as a percentage of total morale)
	0.10
	0.30
}
DISEASE_MORALE_LOSS_LEVELS = {						// How many levels of disease are there and how much (as percentage) is the defender morale loss increased by these levels.
	0.1
	0.2
}
DESERTION_MORALE_LOSS = 5							// How much defender morale is lost on desertion
SIEGE_FORT_THRESHOLDS = {							// At what levels is another level of siege tier needed to avoid reduced siege speed?
	4
	10
	16
	22
	30
}
SIEGE_FORT_THRESHOLD_IMPACT = 0.6					// What is the impact of not having enough siege tier? Siege speed is multiplied for this for each missing tier. E.G., if siege tier is 0, and fort level is 4, siege speed is multiplied by 0.5 \* 0.5
SIEGE_LOOOT_MULTIPLIER = 40							// The income of the holding multiplied by this number is how much loot the besieging army will get for occupying it.
DEFENDER_OVERESTIMATION_FOR_SPLIT = 1.5				// Multiply number of defenders with this when splitting of a siege army to account for troops lost by the attacker to attrition during the remainder of the siege

# NProvince
BASE_SUPPLY_LIMIT = 2000						// The unmodified base supply limit of a province
SUPPLY_PER_DEVELOPMENT = 150					// Each development adds this much sto the supply limit

# NPathFinding
EMBARK_COST = 30								// This value will be set as pathfinding cost if it goes from land to sea
DISEMBARK_COST = 10								// This value will be set as pathfinding cost if it goes from sea to land

# NMercenary
LEVELS = { 0 7 14 }								// Defines how many different sizes of mercenary companies are there and how many are spawned for a given culture. The numbers correspond to numbers of counties of the culture. No company exists if the number is lower than the first value specified here.
HIRE_RANGE = 500								// The maximum distance of mercenaries that can be hired (capital to mercenary location)
LEVIES = { 400 800 1200 }						// The base numbers of levies for levels of mercenary bands
MAA_REGIMENTS = { 1 2 3 }						// The number of MAA regiments for levels of mercenary bands
NUM_KNIGHTS = { 2 3 4 }							// The number of knights for levels of mercenary bands
MAA_REGIMENT_SIZES = { 300 300 300 }			// The base sizes of MAA regiments for levels of mercenary bands
SIZE_INNOVATIONS_RATIO = 1.0					// How much are mercenary companies growing with the ratio of discovered to all cultural innovations of the culture. 1.0 means +100% if SIZE_INNOVATIONS_RATIO = 2, the mercenaries will be 3x their original size if all innovations are discovered
HIRE_MONTHS = 36								// The length of the period mercenaries are hired for in months
LEVY_COST_PER_100_SOLDIERS = 12.0				// The cost of the levy regiment part of mercenary companies, per 100 soldiers for better precision
MAA_COST_RATIO = 0.5							// The cost of the MAA regiments of mercenary companies as a fraction of what those regiments cost when buying them
ALLOWED_DEBT_MONTHS = 24						// How many months of monthly income in dept are characters allowed to have before being blocked from hiring mercenaries
REINFORCEMENT_FACTOR = 3.0						// How much faster do mercenary regiments reinforce than regular regiments
COUNTY_REMOVAL_FACTOR = 1.2						// When removing mercenaries from shrinking cultures, first multiply culture size with this

# NHolyOrder

// In addition to the holding levies, a holy order has levies according to this formula: NUM_LEVIES_BASE + <num holdings> \* NUM_LEVIES_PER_HOLDING
NUM_LEVIES_BASE = 500
NUM_LEVIES_PER_HOLDING = 200
NUM_MAA_BASE = 200								// The holy order starts out with NUM_MAA_BASE Men-At-Arms. These will always try to use the holy_order_maa defined in the religion, if any are available.
NUM_MAA_PER_HOLDING = 100						// The holy order also gets NUM_MAA_PER_HOLDING additional Men-At-Arms for each holding leased to it.
RELIGION_MAA_RATIO = 0.7						// The regiment type of these additional Men-At-Arms has a chance of RELIGION_MAA_RATIO % (multiplied by 100) to use a religious type, like NUM_MAA_BASE. Otherwise it will use a random type with the holy_order_fallback = yes flag.
PATRON_MIN_TIER = 4								// minimum tier for a ruler to be a patron of a holy order
LEVY_COST_PER_100_SOLDIERS = 5.0				// The piety cost of the levy regiment part of holy orders, per 100 soldiers for better precision
MAA_COST_RATIO = 0.2							// The piety cost of the MAA regiments of holy orders as a fraction of what those regiments cost when buying them
PATRON_HIRE_COST_MULT = 0						// The patron pays only a fraction for hiring a holy order. Set to 0 to make it free.
HIRE_LIMIT = 1									// One character can hire up to this many holy orders. Set to -1 to disable the limit.
ENEMY_MIN_HOSTILITY_LEVEL = 2					// Must be at war with someone with at least this hostility level to be able to hire holy orders. Once hired hey can be used against all enemies, though.
BASE_NUM_KNIGHTS = 2							// How many knights do holy orders have?
EXTRA_KNIGHTS_PER_HOLDING = 0.5					// How many knights do holy orders get for each holding? Rounds down

# NPlayer

RALLY_POINT_LIMIT = 10								// Rally point number limit for players
MIN_PATH_COST_SAVINGS_TO_CONSIDER_WATER_PATH = 45	// Number of travel days saved before right-clicking considers going through water instead

# NRaid

RAID_LOOT_PER_SOLDIER = 0.1				// How much loot can a single soldier carry? Minimum increment is 0.001
MIN_SOLDIERS_TO_RAID = 200				// How small can a raid army be and still be able to loot?
MONTHLY_ATTRITION = 0.01				// How much attrition do you take while looting a province? 0.01 = 1% per month
MONTHS_OF_RAID_LOOT = 12				// How many months of holding income (with owner effects discounted) does raiding provide?
// Progress cannot be lower than 1/day (except when interrupted by combat)
BASE_PROGRESS = 20						// How much base raid action progress do you get per day?
PROGRESS_PER_SOLDIER = 0.01				// How much raid action progress do you get per day per soldier? Minimum resolution is 0.001
BASE_DIFFICULTY = 350					// How much base progress is needed?
DIFFICULTY_PER_FORT_LEVEL = 350			// How much progress is needed per fort level in the holding?
DIFFICULTY_PER_COUNTY_FORT_LEVEL = 250	// How much progress is needed per fort level in the county *outside* the holding?
DAYS_OF_HOSTILITY = 180					// How long after raiding do hostilities last?
DAYS_OF_IMMUNITY = 1825					// How long does raid immunity after defeating a raid army last?
RAID_REALM_AI_COOLDOWN = 1				// How many years the AI should wait before considering raiding again, after any AI raiders have been defeated previously

# NAI

MIN_WAR_CHEST = {											// The desired war chest will always be at least this much money, by tier
	25
	25
	50
	100
	200
	300
}
MONTHS_OF_MAINTENANCE_IN_WAR_CHEST = 24						// The AI will want this many months of max maintenance in their war chest, if that's more than what MIN_WAR_CHEST says
PERCENTAGE_INTO_WAR_CHEST = 0.75							// When the war chest hasn't been filled, the AI will put this much of the money it earns into the war chest (reserved gold still gets filled first)
MEN_AT_ARMS_EXPENSE_GOAL = 0.4								// The AI will try to spend this much of its income on MAA maintenance
MEN_AT_ARMS_EXPENSE_MAX = 0.6								// The AI will disband MAA if it ends up spending more than this amount of its income on maintenance
MEN_AT_ARMS_PRESTIGE_EXPENSE_GOAL = 0.4						// The AI will try to spend this much of its prestige income on MAA maintenance
MEN_AT_ARMS_PRESTIGE_EXPENSE_MAX = 0.6						// The AI will disband MAA if it ends up spending more than this amount of its prestige income on maintenance
MEN_AT_ARMS_CHANCE_EXPENSE_ZERO = 1							// Chance the AI will prefer MaA to buildings when spending nothing on MaA
MEN_AT_ARMS_CHANCE_EXPENSE_MIN = 0.2						// Chance the AI will prefer MaA to buildings when spending the goal amount on MaA. For values between that and zero, we interpolate
MEN_AT_ARMS_REALM_SIZE_FOR_COST_EFFECTIVENESS_START = 5		// At realm sizes of this and below, men at arms quality is based on stat points compared to cost
MEN_AT_ARMS_REALM_SIZE_FOR_COST_EFFECTIVENESS_END = 50		// At realm sizes after this, men at arms quality is completely unaffected by cost. Between the two values, we interpolate between the unmodified and modified quality
THREAT_MIN_STRENGTH_RATIO = 0.5								// Only consider threats above this ratio
THREAT_CLAIM_TIER_MULTIPLIER = 10							// Multiplied with each claim's tier squared
THREAT_DE_JURE_CLAIM_MULTIPLIER = 50						// Multiplied de jure claim
THREAT_MAX_DIPLO_DISTANCE = 1000							// Max distance to be considered a threat
THREAT_STRENGTH_NEIGHBOUR_RATIO_MULTIPLIER = 100			// Multiplied with the strength ratio
THREAT_STRENGTH_RATIO_MULTIPLIER = 50						// Multiplied with the strength ratio
ENEMY_MAX_STRENGTH_MULTIPLIER = 1.5							// Only consider enemies equal or below this ratio
ENEMY_CLAIM_TIER_MULTIPLIER = 10							// Multiplied with each claim's tier squared
ENEMY_DE_JURE_CLAIM_MULTIPLIER = 50							// Multiplied de jure claim
FRIEND_ALLY_MAX_DIPLO_DISTANCE = 1000						// Max distance to be considered for a strength ratio bonus
FRIEND_ALLY_MIN_STRENGTH_RATIO = 0.25						// Only add strength ratio bonus for equal or above this ratio
FRIEND_ALLY_STRENGTH_RATIO_MULTIPLIER = 100					// Multiplied with the strength ratio
MIN_PATH_COST_TO_CONSIDER_WATER_PATH = 120					// Number of travel days before AI considers searching for a path across water instead
MIN_PATH_COST_SAVINGS_TO_CONSIDER_WATER_PATH = 65			// Number of travel days saved before AI considers going through water instead
MAX_PATH_COST_FACTOR = 5									// The maximum cost for a path is this factor times the straight path cost
RAISE_LEVIES_COOLDOWN = 180									// Number of days before the AI tries to raise levies if it already has an army
RAISE_TROOPS_MIN_RATIO_OF_SELF = 0.3						// If the AI doesn't have troops raised, it won't raise them unless the troops amount to at least this much compared to its max troops
RAISE_TROOPS_MIN_RATIO_OF_ENEMY = 0.5						// Or this much compared to its enemy
REDUCED_EFFECTIVE_WEALTH_PER_HIRED_MERC = 100				// For each hired merc, the AI pretends to have less money so that it ends up keeping some reserves
MIN_HIRING_GOAL = 500										// If missing less than this amount to outnumber its enemies, the AI will hire as if were actually missing this amount
MAX_HIRING_GOAL_OVERFLOW_RATIO = 2							// The AI won't hire more than this times as many men as it is missing. It'll hire the most expensive merc that fits within this. E.G., this means that if the AI is missing 1000 men, it'll hire the most expensive merc with less than 2000 men
MONTHS_BEFORE_CONTRACT_END_TO_REHIRE = 3					// This many months before a merc contract ends, the AI will rehire mercs if it can afford it and thinks it still needs them
// When buying/disbanding MaA, these mults are used to figure out the score. Note that the score is divided by cost, and multiplied by stack size (except for siege value, which is only divided by cost)
TOUGHNESS_SCORE_MULT = 10
ATTACK_SCORE_MULT = 10
PURSUIT_SCORE_MULT = 2
SCREEN_SCORE_MULT = 1
SIEGE_VALUE_SCORE_MULT = 1000
NEGATIVE_SCORE_PER_EXISTING_REGIMENT = 20					// How much is the score of the regiment type reduced per existing subregiment of that type?
RANDOM_REGIMENT_SCORE_MAX = 0.2								// How much extra score can the AI randomly give to this regiment? Will always be the same for the same character + regiment. 0.2 means 0-20% extra
NORMAL_SUB_REGIMENTS_PER_SIEGE_SUB_REGIMENT = 5				// How many non-siege regiments should there be for each siege regiment? Siege will always be the first sub-regiment purchased, and the AI will maintain this ratio
SUBTRACT_NORMAL_SUB_REGIMENTS_FOR_SIEGE_PURPOSES = 3		// Ignore this many normal regiments when buying siege sub-regiments. This effectively means the AI will buy their first siege weapon after this many normal ones, and then one more for every NORMAL_SUB_REGIMENTS_PER_SIEGE_SUB_REGIMENT additional normal sub-regiments
REGIMENT_OBSOLETION_SCORE_DIFFERENCE = 20					// The AI will disband a regiment if it is this much worse than the best available regiment, and it is unable to hire more regiments (due to cost or being at cap). Quick math: 10 damage * 100 men / 200 cost = 5 score difference
AI_BASE_WAR_CHANCE = 0.5									// Basic chance of declaring war. Further reduced by energy; x0 at -100, x1 at 100, x0.5 at 0 energy
AI_WAR_BASE_COOLDOWN = 365									// How long, in days, does the AI have to wait between wars?
AI_WAR_COOLDOWN_RATIO_FOR_FULL_CHANCE = 3					// How far beyond the cooldown do you have to go before the time since the last war stops reducing the chance? With these numbers, chance at day 3650 would be 0x, 1x at 3650*2, and 0.5x at 3650*1.5
AI_WAR_MAX_OFFENSIVE_WAR_PENALTY = 0.0						// If your offensive war penalty is higher than this, don't declare war unless you're a warmonger (faith doctrine) or irrational
AI_WAR_MIN_RATIONALITY_FOR_OFFENSIVE_WAR_PENALTY = -30		// At or below this value, the AI will declare war even if their offensive war penalty is high
TARGET_MAX_DEFENSIVE_WARS = 3								// AI won't declare war on someone who already has this many or more defensive wars
DESIRED_WAR_SIDE_STRENGTH = 2.0								// AI won't call in more allies if its side in a war has at least this ratio of troops compared to the enemy. Uses current strength for own side, max strength for enemy side
ENEMY_COMBAT_STRENGTH_MULTIPLIER = 1.1						// The AI will take its estimated enemy strength times this multiplier
COUNTER_RAID_MIN_DISTANCE = 75								// The AI will try to raise counter-raid troops at least this far awy from the raid
COUNTER_RAID_MAX_DISTANCE = 200								// The AI will raise counter-raid troops at most this far away from the raid
OTHER_RAID_ARMY_COMBINED_STRENGTH_MAX_DISTANCE = 200		// Other raid armies no more than this far away will be considered as part of the same raid army for strength purposes
VASSAL_COUNTER_RAID_MIN_STRENGTH_RATIO = 0.9				// A vassal at least this strong as the raid will be responsible for countering it
INDEPENDENT_COUNTER_RAID_MIN_STRENGTH_RATIO = 0.6			// An independent ruler at least this strong as the raid will be responsible for countering it if no vassal does
MAX_RAID_DISTANCE = 1500									// How far away will the AI raid?
MAX_RAID_DISTANCE_NEXT_COUNTY = 200							// After raiding one county, how far is the AI willing to go to the next?
MIN_STRENGTH_TO_RAID_VASSAL = 500							// How strong do vassals have to be for the AI to go raiding?
MIN_STRENGTH_TO_RAID_INDEPENDENT = 300						// How strong do independent rulers have to be for the AI to go raiding?
MAX_RAID_TARGET_STRENGTH = 1.5								// Don't raid enemies too strong
MAX_RAID_TARGET_STRENGTH_AT_WAR = 5.0						// But if they're at war, the risk might be worth it
MIN_STRENGTH_FOR_RAIDER_TO_AVOID = 0.9						// If there's hostile units in this county and neighboring counties that are combined this strong compared to the raid army, flee home
RAID_SCORE_MIN_STRENGTH_RATIO = 0.2 						// We divide the score by how strong the target is compared to us; if lower than this, we use this number. So 0.2 means that outnumbering them 5:1 and 2:1 are equivalent
RAID_SCORE_DISTANCE_OFFSET = 200 							// We divide the score by the distance from the realm (or army, if follow-up raid) plus this number
RAID_SCORE_DISTANCE_OFFSET_NEXT_TARGET = 30 				// We divide the score by the distance from the army plus this number when finding the next county to go to
RAID_SCORE_FORT_LEVEL_OFFSET = 5 							// We divide the score by the sum of all fort levels in the county, plus this number
MIN_RAID_SCORE_COMPARED_TO_BEST_SCORE = 0.4					// Scores this much worse than the best score are just discarded
RAID_CHANCE_AT_MAX_GREED = 0.9								// Chance to go raiding each year if at 100 greed. 0.0 at -100 greed. Must still meet all other conditions
MAX_RAID_DAYS = 365											// After this long, the AI will go home when a raid action concludes
RAID_COOLDOWN_DAYS = 1825									// The AI won't start a new day for this long after last having started one
COUNTER_RAID_COOLDOWN_DAYS = 180							// The AI won't counter-raid for this long after they last counter-raided
// Hostility levels start at 0 (same faith or equivalent to same faith)
RAID_SCORE_FAITH_HOSTILITY_MULT = {	// Raid score mult based on hostility
	1
	1.5
	2
	3
}
RAID_SCORE_MULT_SAME_CULTURE = 0.5
RAID_SCORE_MULT_SAME_CULTURE_GROUP = 0.75
CHASE_MIN_SIZE = 100										// The AI will not bother trying to chase armies smaller than this
// The AI will only retreat if the following are true:
// It predicts it'll lose according to RETREAT_COMBAT_PREDICTION_RATIO
// AND it either has significant forces elsewhere, or there's a better defensive location nearby as defined by RETREAT_TO_BETTER_TERRAIN_DISTANCE
RETREAT_COMBAT_PREDICTION_RATIO = 0.45						// Below this combat prediction ratio the AI will retreat
RETREAT_TO_BETTER_TERRAIN_DISTANCE = 2						// The AI will retreat to better terrain this many provinces away (might do another retreat once it gets there)
RETREAT_IF_MISSING_STRENGTH = 0.25							// The AI will retreat if it has this many troops elsewhere compared to the potentially retreating army. E.G., if 2000 men are considered for retreat, it'll do so if there's at least 0.25 * 2000 = 500 men elsewhere
STAND_AND_FIGHT_DAYS = 30									// If the AI decides to stand still so the other party can kill it on defensible terrain, it'll start doing regular orders again after this many days if death is not forthcoming
STAND_AND_FIGHT_COOLDOWN_DAYS = 90							// If the AI abandons "stand and fight" due to the above, it'll avoid "stand and fight" for this many days
DISCARD_UNIT_GOALS_UNDER_TRESHOLD = 0.5						// The AI will discard potential targets scored at this threshold or lower compared to the best target, even if the best target is unsafe
MIN_GOALS_PER_STACK = 5										// However, it will ensure it always evaluates at least this many goals per stack, even if they're below the threshold
MIN_SUPPLY_COMPARED_TO_AVERAGE_SUPPLY_FACTOR = 0.7			// For the purpose of army sizes, the AI uses the highest of this factor times the average supply in the war area, and the lowest supply in the war area. E.G., if average supply is 2k, and lowest supply is 1k, the AI will act as if available supply is 0.7 * 2k = 1.4k. But if the lowest supply was 1.5k, it'd be using that instead
RESUPPLY_MAX_DISTANCE = 3									// How far out can splinters of the army spread when trying to resupply? In // of provinces. AI will try to keep it lower if possible
RESUPPLY_COOLDOWN_DAYS = 250								// If supplying is interrupted due to insufficient supply, wait for this long before trying to resupply again

# NCombatInterface

COMBAT_BALANCE_UNDECIDED_ZONE = 0.1					// If the balance of the combat is within this range around 50% (0.5) the prediction is considered undecided
COMBAT_BALANCE_DIRECTION_STEPS = 3					// How many steps should the combat balance progress direction indicator have
COMBAT_BALANCE_STEP_CHANGE = 10						// Balance change needed for increasing the steps of the indicator by one
UNIT_QUALITY_THRESHOLDS = {							// If damage + toughness per man is at least the threshold value, the quality level is considered one higher
	25
	50
	75
	100
}
MAX_COMBAT_PREDICTION_DISTANCE = 5					// How far along the path of your units should we bother to look? Higher means we can predict combat further away, but the situation is more likely to change before combat occurs
BATTLE_EVENT_DURATION = 5.0							// How many seconds do battle events stick around for?

# NCombatPrediction

COMBAT_PREDICTION_ADVANTAGE_ROUNDS = 5				// How many rounds of the advantage are added to the starting advanatage when predicting the combat result
EDGE_COMMANDER_MARTIAL_THRESHOLD = 3				// Commanders' martial skill difference needs to be at least this for it to be counted as an edge
EDGE_COMMANDER_TRAITS_THRESHOLD = 1					// Commanders' number of commander traits skill difference needs to be at least this for it to be counted as an edge
EDGE_SOLDIERS_RATIO_THRESHOLD = 1.25				// Total soldier count ratio needs to be at least this for it to be counted as an edge
EDGE_QUALITY_THRESHOLD = 1.25						// Quality ratio needs to be at least this for it to be counted as an edge (together with EDGE_MIN_MEN_AT_ARMS)
EDGE_COUNTER_RATIO_THRESHOLD = 1.25					// Total MAA counters need to be at least this for it to be counted as an edge
EDGE_FORTIFICATION_THRESHOLD = 20					// Fortification needs to be at least this for it to be counted as an edge
COMBAT_PREDICTION_LEVELS = { 0.4 0.5 0.7 0.9 }		// Prediction levels thresholds