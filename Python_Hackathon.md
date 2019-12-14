# Python Hackathon
[Back](index.md)

![hackathon](https://i.imgur.com/VAN0Jbo.gif)

<iframe width="560" height="315" src="https://www.youtube.com/embed/dOREDa6kEN8" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

For my final project I chose to continue a project that I started at work at the beginning of the summer: implementing the [Toast POS System](https://pos.toasttab.com/) at [Jack’s Urban Eats at Renaissance Creek in Roseville](https://www.yelp.com/biz/jacks-urban-eats-roseville).The project was initially pitched as a way for me to continue to develop my tech skills during the summer break. To research the system, I worked at the [Jack’s @ the Fountains in Roseville](https://www.yelp.com/biz/jacks-urban-eats-roseville-2) where a trial implementation was up a running. 

![store](https://i.imgur.com/vE9EPRx.jpg)

While I was there we made some updates to the implementation including an additional point of interaction. I delivered a Cost/Benefit analysis to stakeholders once I felt sufficiently versed in the system. The decision was then made to install the system not only at the initial target location, but at the majority of Jack’s Urban Eats stores. 

![handheld](https://i.imgur.com/k4Jppvu.jpg)
![layout](https://i.imgur.com/une46sJ.png)

I chose to work alone on this project only with respect to the scope of this class. In reality, this has been a group project all along including stakeholders, management, end users, and considerable investment of time and resources necessary for installation. While I believe I’m missing out slightly by not partnering with an IT75 classmate, my professional experience tells me that this is a more valuable experience in that a typical work environment is composed of multi-disciplinary teams. That, and I should be able to pitch this a billable contract.

For the GUI automation project I turned in a stripped down version of reporting within Toast POS. This version is much closer to what will actually be implemented at Jack's as a cost saving measure.

Using Selenium, XPATHs make it easy to locate data within a webpage. I did my best to figure out the exact locations of all of the data necessary to properly populate a daily report for Jack's. Presently, I'm only able to get a few values out reliably. I suspect this is due to some sort of dynamic rendering reports, possibly in AJAX (or something like it.) Here's a list of XPATHS:

```python
labor = {
	"boh_hrs_reg" : ('F35','/html/body/div[2]/div[1]/div/div[2]/div[2]/div/div/div[4]/div/div[2]/div[1]/table[1]/tbody/tr[1]/td[2]'),
	"boh_hrs_ot" : ('F35','/html/body/div[2]/div[1]/div/div[2]/div[2]/div/div/div[4]/div/div[2]/div[1]/table[1]/tbody/tr[1]/td[3]'),  # might need to de-dupe? these get combined... same with the rest of the hours fields
	"boh_pay" : ('G35','/html/body/div[2]/div[1]/div/div[2]/div[2]/div/div/div[4]/div/div[2]/div[1]/table[1]/tbody/tr[1]/td[6]'),
	"cash_hrs_reg" : ('F36','/html/body/div[2]/div[1]/div/div[2]/div[2]/div/div/div[4]/div/div[2]/div[1]/table[1]/tbody/tr[2]/td[2]'),
	"cash_hrs_ot" : ('F36','/html/body/div[2]/div[1]/div/div[2]/div[2]/div/div/div[4]/div/div[2]/div[1]/table[1]/tbody/tr[2]/td[3]'),
	"cash_pay" : ('G36','/html/body/div[2]/div[1]/div/div[2]/div[2]/div/div/div[4]/div/div[2]/div[1]/table[1]/tbody/tr[2]/td[6]'),
	"foh_hrs_reg" : ('F37','/html/body/div[2]/div[1]/div/div[2]/div[2]/div/div/div[4]/div/div[2]/div[1]/table[1]/tbody/tr[3]/td[2]'),
	"foh_hrs_ot" : ('F37','/html/body/div[2]/div[1]/div/div[2]/div[2]/div/div/div[4]/div/div[2]/div[1]/table[1]/tbody/tr[3]/td[3]'),
	"foh_pay" : ('G37','/html/body/div[2]/div[1]/div/div[2]/div[2]/div/div/div[4]/div/div[2]/div[1]/table[1]/tbody/tr[3]/td[6]'),
	"janitorial_hrs_reg" : ('F38','/html/body/div[2]/div[1]/div/div[2]/div[2]/div/div/div[4]/div/div[2]/div[1]/table[1]/tbody/tr[4]/td[2]'),
	"janitorial_hrs_ot" : ('F38','/html/body/div[2]/div[1]/div/div[2]/div[2]/div/div/div[4]/div/div[2]/div[1]/table[1]/tbody/tr[4]/td[3]'),
	"janitorial_pay" : ('G38','/html/body/div[2]/div[1]/div/div[2]/div[2]/div/div/div[4]/div/div[2]/div[1]/table[1]/tbody/tr[4]/td[6]'),
	"lead_hrs_reg" : ('F39','/html/body/div[2]/div[1]/div/div[2]/div[2]/div/div/div[4]/div/div[2]/div[1]/table[1]/tbody/tr[5]/td[2]'),
	"lead_hrs_ot" : ('F39','/html/body/div[2]/div[1]/div/div[2]/div[2]/div/div/div[4]/div/div[2]/div[1]/table[1]/tbody/tr[5]/td[3]'),
	"lead_pay" : ('G39','/html/body/div[2]/div[1]/div/div[2]/div[2]/div/div/div[4]/div/div[2]/div[1]/table[1]/tbody/tr[5]/td[6]'),
	"mgr_hrs_reg" : ('F40','/html/body/div[2]/div[1]/div/div[2]/div[2]/div/div/div[4]/div/div[2]/div[1]/table[1]/tbody/tr[6]/td[2]'),
	"mgr_hrs_ot" : ('F40','/html/body/div[2]/div[1]/div/div[2]/div[2]/div/div/div[4]/div/div[2]/div[1]/table[1]/tbody/tr[6]/td[3]'),
	"mgr_pay" : ('G40','/html/body/div[2]/div[1]/div/div[2]/div[2]/div/div/div[4]/div/div[2]/div[1]/table[1]/tbody/tr[6]/td[6]'),
}
```
Though they aren't entirely accurate at the time of publishing, this is actually a pretty decent visualization of how many actions must be taken for each reporting cycle. No wonder this can actually take a decent amount of time while attempting to manage a team closing.

Check it out here! [github](https://github.com/frymatic/Python-Hackathon)

[Home](index.md)