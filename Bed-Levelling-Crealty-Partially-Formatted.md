# Levelling a Creality Pro 3
The following discussion occurred between *an informed source, _Andrew_* and *[Christian Schladetch](christian@schladetsch.com)* in early 2022 regarding how to level a Creality 3d Pro.

## Andrew
Do NOT move anything round rapidly.

That is, when moving the bed... do it quite slowly
Because moving the bed (or the nozzle) causes the steppers to rotate. And this causes them to act as dynamos, and generates back-current into the board electronics... which is not protected.

In theory you can damage your board. Slow movements only.

Next step: in the menu you'll have an option to "auto home". Something like control/movement. It will be different for your machine, but you want to home everything.
Let me know when that's done.

## Christian
Sorry just setup printer laptop for Facebook.
One sec to read back.
Bed is wobble-free with all nuts at reasonably tightened clockwise rotation.

## Andrew
And homed?

## Christian
Had to use Pi Power source, relog to FB, and Purify, and other nonsense.
Waiting for Octorpint to boot.
Still giving under-power even tho it's a Pi power supply plugged into a down-shofted 3-phase GPO.
Will read again.
I have never turned off stepper motors.

## Andrew
Well maybe your version of the printer has an assisted levelling routine. I'm going through the completely manual process.

## Christian
But I've also never manually moved any motors.
 
## Andrew
I have maybe another half hour i can spare you.

## Christian
I have auto-homed the head. All levelling screws are 100+ CW.

## Andrew
Ok, and your bed moved right to the back too?

## Christian
Yes.

## Andrew
So the nozzle is about front left relative to the bed?

## Christian
Yes.

## Andrew
If you eyeball it, there maybe comehing like 3-5mm clearance from the tip of the nozzle to the bed?

## Christian
2-3mm but yeah
 
## Andrew
Ok good.  Now here's an extremely important thing to understand:
When you ajust those screws, the whole bed pivots ONLY around those 4 points of attachment.
In reality for aplane you should have 3 points to define the plane.

## Christian
Yeah that's annoying.

## Andrew
Ok, but the point being - when you are adjusting, it's really only important to do the adjustment and check for spacing when the nozzle is directly above one of those 4 points.

## Christian
Ahh.

## Andrew
More to the point, when you are adjusting one of those 4 screws, your nozzle should be above that screw and that's where you check the spacing/distance. Because that's the point you are directly affecting.

## Christian
Right.

## Andrew
Ok. Somewhere in the menu you will see disable steppers.
Probably in the same menu with the auto home.
Typically at this point yo would also set the bed temperature to something like 50°C

## Christian
Yeah but I can't activate it.

## Andrew
So you have something like a menu option to level the bed, which takes you through the steps?

## Christian
I have "Set Home Offsets"

## Andrew
No. Not that. You must have a menu that lets you move around the bed and nozzle maybe in there?

## Christian
"Disable Steppers" is visible, but when I click on it, nothing happens.

## Andrew
Nothing should happen. But now when you grab the bed you should be able to move it (gently) back and forth

## Christian
I mean, there's no response from the controller to acknowledge that steppers enabled/disabled etc

## Andrew
You don't get a response.
But if you can manually move the bed, we're good to go.

## Christian
Ok done.

## Andrew
Can you manually move the bed? And the nozzle? (slowly)
Don't move the nozzle up/down. Only left/right.

## Christian
Ok.

## Andrew
So, all good?

## Christian
Yes.

## Andrew
Ok, get a piece of paper - a4

## Christian
Yeah I have a folded receipt.

## Andrew
Normal printer paper is better if you can find something like that. Thickness is the key.

## Christian
I heared receipt paper is better one moment.

## Andrew
Now, this next bit is another very important one....
After your last print, a tiny bit of filament is still poking out of the tip of the nozzle, and it hardens there
so if you do a bed-level without heating up the nozzle, you have that hardened filament glob poking out
and it totally screws your levelling.

## Christian
I've flushed and brused it with metal brush

## Andrew
Ah. Well, I'd never never do that. I shudder to think, actually!

## Christian
They are purpose built for the job.

## Andrew
Let's just heat up the nozzle to (say) 190�C and the bed to 50�C.
And we want to get through this levelling reasonably quickly because I don't want to leave them on too long
so start the heating. And meanwhile put the paper on the bed, front left.

## Christian
Done and done.

## Andrew
We want to move the bed AND the nozzle so that the nozzle is directly above the axis of the front left adjustment screw.
And we're going to turn that screw, opposite direction now, so that we bring the bed closer to the nozzle holding one corner of the paper, slide it back and forth as youre' doing the adjustment, until you feel just a little bit of scraping on the paper.
When you first do this you'll see some of the filament as a trail on the paper. This is just scraping off that "glob"
When the nozzle is up to heat.
You want to be able to move that paper back and forth while holding a distant corner, without the paper buckling.
but you want a definite light scrape.

## Christian
Done it.

## Andrew 
Ok, and you saw a bit of filament on the paper?
Now we move to the front-right corner.... paper in pace, and then adjust. remember to move nozzle/bed slowly
and then... we do them all AGAIN.

Because adjusting each of them will throw out the adjustmet of all the others
next, here's another super-important thing to remember....

## Christian
Done.

## Andrew
this process ajusts (perfectly) the distance from thos pivot points to the nozzle BUT your bed is almost certainly warped. i.e., not truly flat.
And so the middle of the bed is probably badly adjusted at this point.
It's possible the bed is raised, which would mean your nozzle would gouge a hole trying to get to the center.
Or maybe it's lowered, so you have a dip in the middle.
You need to fudge things so that your center is "about right".
So carefully move the nozzle to about the center of the bed, being careful not to scrape the bed you may need to keep the paper under the nozzle and move them togther.

## Christian
Wait - back right doesn't get close enough to nozzle.

## Andrew
Ok, that's a problem.
This means we'll need to adjust the endstop.
Basically at this point it's hard to see how you could get consistent printing, particularly on anything towards that back right corner.
Turn off the temeprature on nozzle/bed at this point.

## Christian
Done.

## Andrew
When you auto-home, the whole x-axis assembly carrying the nozzle moves down.
And on the left side lower left of your vertical frame bar, you have a little microswitch
that gets triggered when the z axis moves down.

## Christian
Yeah the hard stop.

## Andrew
Yes. Well that's adjustable.
Because we couldnt' get that back right corner close enough, we have to allow the z to go a fraction lower so we have to move that endstop down by a tiny fraction -- say 1mm.
Depends on what the distance to the nozzle was at the back right corner. Must be at least that.

## Christian
Where is the end stop switch for the back right or is it the same switch?

Andrew
One switch to rule them all.

## Christian
Ok thanks good night.

## Andrew
This is not a common problem.

## Christian
I really appreciate your time and I learned a lot.

## Andrew
What's really really important now... I wasn't signing off... you are?

## Christian
But I also know that changing the endstop switch means repeating everything again.

## Andrew
Yes, you are now in danger of crashing the nozzle into the bed, so make sure you fully adjust the bed down -- like we did at first -- before doing ANYHING else.

## Christian
I can keep going (I WFH) but don't want to steal all your time.

## Andrew
We're close to done. You can do the final steps alone.
But remember, you are adjusting only 4 pivot points, and your center may be out of whack due to warpage in your bed.

So you need to find a compromise. Once your 4 points are good, then you may need to get the middle "closer" in which case turn all 4 the same amount (closer/farther) by - say - 1/4 turn.

If you are adjusting all 4 at the same time by the same amount, you are keeping the whole thing parallel to "true" but shifting it up/down.

## Christian
Glass shouldn't bend in a couple of years :/

## Andrew
You're printing on glass?

## Christian
Yes.

## Andrew
Godawful surface.

## Christian
Well, it's textured glass from Creality.

## Andrew
Ok, we can actually put pieces of tape under the middle of the glass to shift that midpoint up if we need to you may be lucky and it's not warped.
How is your glass surface affixed to the underlying bed mechanism?

## Christian
(4 clips)

## Andrew
Ok, that's good.
It's likely flat, so we could be good.
So go through the whole thing again. First all 4 points adjusted so bed is as far away as possible, then heat bed/nozzle, then paper/adjust 4 points, to the adjustment for 4 points another time, and finally check in the middle to see what the clearance is like oh, and textured glass should be OK to print on.
It's just smooth glass is a bear to get adhesion with.

## Christian
I can't get TopLeft low enough, or TopRight high enough

## Andrew
can we go with front and back?
what's top left?

## Christian
Facing the printer from the front.

## Andrew
So front left.

## Christian
Back left in that case.

## Andrew
Let me think for a few seconds. Did you do an auto-home? Before that.

## Christian
No.

## Andrew
Don't. I'm just a bit worried about. The nozzle scraping the glass.
So first manually move the nozzle to the left.
And make sure your bed is as low as it can be.

## Christian
Now front left is also too high. This is why I hate this :(

## Andrew
You don't do this every time.  Your printer was poorly setup.

Don't get ahead of me as i need to know in my mind exactly what your printer is at.
You should have the bed way down, the nozzle left, and have just auto-homed.

Ok, well I'm going to leave you with some instructions....
Once the bed is down, nozzle left, and auto-homed, turn on the temperatures and repeat the levelling as before.

All 4 points, done twice. Assuming you can adjust them correctly with that "just scraping" and the middle is OK too, then your bed is actually adjusted correctly.

You try a print. If you can't get adhesion, then make the bed a little closer (again, just a 1/4 turn on all wheels -- you don't need to paper-test)

## Christian
I tried repeating everything, starting front left and then back right. I still couldn't level back left

## Andrew
As to print temperatures, i'd recommend bed at about 60°C and nozzle at about 200°C for first test

## Christian
Right.

## Andrew
It was back right last time.

## Christian
I'll figure it out.

## Andrew
How far away is the nozzle back left?

## Christian
I've rebuilt the entire thing twice. I get it, but yeah I didn't fully grok the levelling 1.8mm

## Andrew
when the others are scraping???!!

## Christian
No, both back ends are away from surface by .50-1.50mm.

## Andrew
When the bed is as close as possible?

## Christian
Front ends are fine. Yes.

## Andrew
100% sure you are turning the screws the right way?

## Christian
Warped bed?
Yes.
There's only one way to turn them when they are maxxed.

## Andrew
It makes no sense. There is ample adjustment in the bed height on those screws to allow for significant issues something else is wrong.
Try adjistnig those two FIRST see if you can get them close.

## Christian
You mean the back ends?

## Andrew
Move the bed totally down all 4

## Christian
Makes sense.

## Andrew
Then adjust. The back left one. I'm just trying to see if the range is OK for those back ones when you adjusted the endstop did you move it up or down?

## Christian
Great success. By adjusted back levels first, then front, it seems I have a level bed even in center.

## Andrew
Ok, that's not how it should work, but if it's level it's level. Last step...

Just to be paranoid and confirm everythinng we do an auto-home, and then double-check that the nozzle isn't scraping the bed, by just moving it and the bed to check a few random areas on the bed. paper on bed and auto-home first, then disable steppers, then move nozzle around to see how the clearance looks.
If OK you can do a print.
