Gold Cards have a 10% chance of spawning!

A normal chain of 3 cards gives you 6 points
A chain with a gold card at the end will give you 15 points!
Try to leave Gold cards till the very end of a chain to get more points!
Adds straetgy to try and risk chaining gold cards last. 



							Here is my code I added

Changes made to Deck code:

int ran = Random.Range(0, 100); //Generates random #
GameObject cgo;
if (ran < 10) //Gold Card 10% chance
{
	cgo = Instantiate(prefabCardGold) as GameObject;
}
else
{
	cgo = Instantiate(prefabCard) as GameObject;
}

if (ran < 10) //Gold Card 10% chance
{
	tSR.sprite = cardBackGold;
}
else
{
	tSR.sprite = cardBack;
}

Changes made to Score code:

if(cd.tag == "Gold")
{
	ScoreManager.EVENT(eScoreEvent.mine);
	FloatingScoreHandler(eScoreEvent.mine);
}