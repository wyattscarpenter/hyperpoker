# hyperpoker

> I ’ard’ardly know ’er’er

This repo contains various ideas I have had regarding hyperpoker, which I also call generalized poker or generalized hyperpoker. Herein are also contained a wide variety of facts and impressions about playing cards and their history in general, which are relevant only to a small piece of hyperpoker, but must indeed be included for that part (although that part in total can be completely skipped if one does not care).

In this repo, I consistently use english suit abbreviations (AKQJ) and english suit names (Ace, King, Queen, Jack), but this is just a presentation detail and could be configured/adapted (for instance, if we imagine this as a software package you could set the UI language to German and get those translated into the german names for english suits, or (independently) you could set the face card family to German and get Ober, etc, as the guys on the card; the situation is similar for physical decks of cards, you just have to sell more of them).

There are three main categories of thought I have about this topic. Cards, rules, and a hypothetical video game adaption of the rules and cards. Speaking of that video game, it's worth noting that this repo is *not* public domain and is proprietary to me. However, I would happily strike a deal with someone who actually wanted to take the time to implement this in a tangible saleable medium.

## Video game implementation (hypothetical)

Anyway, I don't have much to say about the video game, except that you would probably start by playing 0-poker (in which every game is a draw), and then after a certain number of victory points unlock 1-poker, and victories would unlock things in the n-dimensional space of generalized hyperpoker such as hand size, card variety, and special rules like around-the-corner straights. These should be arranged intelligently so that you don't have to beat 2ⁿ things, but you would probably have to beat a lot of things. The poker simulator should also be quite good, on a basic level. Performant, high-definition, modern-style, and 2d (although "fake" 3d can be used for effects or whatever). (Ideally, all the graphics should be vector graphics, so that it can be scaled up arbitrarily and still look smooth.) You should be able to use keyboard, mouse, and controller, individually or in concert. This seems like a lot of work just to do basically well, which is largely why I haven't done it. I'm just too busy looking up playing card wikipedia pages.

Generalized hyperpoker should also be playable in real life, in principle. In fact, the main game I imagine coming out of hyperpoker is basically just texas hold 'em but you can make a 7-card straight.

## Rules

TODO: the rules and cards section are slowly merging, although the history and research sections are still distinct, which is really the important part.

This section concerns questions of how cards should be generalized, in addition to simple rules or numerical adjustments. Therefore, some things are marked as (arbitrary art need), where I predict some implemention of a generalization could (should?) require an infinite or arbitrarily-large amount of art effort. This probably could be dealt with using [procedural generation](https://en.wikipedia.org/wiki/Procedural_generation) of the relevant art assets, or perhaps with modern [AI art](https://en.wikipedia.org/wiki/Artificial_intelligence_visual_art) systems (although, in my experience, circa 2025, good luck trying to get the stock models to generate varied yet consistent things like face cards, especially of sufficient quality, complexity, and crispness). Either giving up on having infinite art or procedural generation are probably the way to go; the latter could be very rewarding, but extremely hard to get right and of course probably finite in the end anyway.

Any version of poker that's generalized to less than the current rules of poker is technically more-accurately referred to as hypopoker instead of hyperpoker, but whatever.

There is an ambiguity in whether the cards held in your hand are your "hand" or the combo you make with the cards is called your "hand". To remove ambiguity in this document, the former will be referred to as your "hole" (from texas hold 'em — where, ironically, you do not hold them) and the latter will be referred to as your "combo". Also, I will probably mess up and just write "hand" sometimes; try to figure those out from context.

It can be observed that ∞-poker would be unplayable in at least the respect that you would have to draw infinity cards, which would take forever. Maybe you could interpret this in some special way that would still allow you to play a game with it, like you just get to pick any cards out of a static selection of all of the cards (where the stock of each card is unlimited) — but since you also get to play an infinite number of cards, this would be difficult to bound as well. There is also the issue that ∞-number-cards poker has an infinite number of number cards available to choose from, but I suppose that's just a user interface issue.

### Quantity of deck, hand, river, etc

The number of cards in the deck, hole, combo, community cards, each phase (and how many phases) of reveal in the community cards if generalizing texas hold 'em, etc, can be generalized up or down (and are in real life, often!).

Generalizing the number of cards in the combo is a little interesting, because now there is a 7-straight potential, for example; but the poker hand rankings are based on cold mathematical calculation of the odds of each one anyway, so the procedure is determinate.

### Stripped decks

The cards in the deck can be generalized down from the normal 52, creating what is technically known as a "stripped deck".

### Numbered cards

The numbered cards instantly suggest generalizability, being numbers, and it can be done. Some interesting numbers are 0, 1 (can be treated distinct from aces eg for around-the-corner-straights or high card), pip values greater than 10, negative pip values, non-integer pip values, and funny numbers like π, e, and i (imaginary numbers — could also use quaternians etc if you understand them I guess).

The video game _Dungeons & Degenerate Gamblers_ uses many similar riffs on these concepts for blackjack cards.

### Face and special cards

The standard 52 deck is pretty close to being a non-stripped deck (in the sense discussed above), but technically a fuller deck of cards has another suit between J and Q, a knight or cavalier, C. That's for use in playing tarot games, specifically, which also unrelatedly adds all the tarot-exclusive trump cards. This up-generalization is a gimme, given that the english pattern was already stripped, compared to the tarot deck, and this unstrips it. See, for example, the rank listings in the decks listed here: https://en.wikipedia.org/wiki/Tarot#French-suited_decks

You can also add jokers in. I guess they're wild, maybe? Or maybe there are other rules for them. But since we don't have any other wild card and jokers are conventionally wild in various card games (including in poker, primarily video poker, in "joker's wild" aka "joker poker") this seems like a good use for them. (Unless they become top trumps like in Euchre? But is a top trump in poker just a high card? Or maybe a high card that even beats regular hands?) Anyway, there could be one joker (of which many copies of one joker is an obvious consequence), or many jokers. I know of some decks with two non-identical jokers. Unicode has three jokers: red, white, and black. https://en.wikipedia.org/wiki/Joker_(playing_card) seems to attest that some popular european games require three (identical?) jokers. Mention is made of a "blue joker" in Poland. https://en.wikipedia.org/wiki/Zwickern seems to require 6 jokers, 2 each of 3 types. There is at least one card game that allegedly uses like 12 different jokers, but I wasn't able to find much info about it.

You can also add the rules card and blank card? I'm not so sure about these. Maybe they're just a joker. Maybe it's more fun if they aren't. (I believe the video game _Dungeons & Degenerate Gamblers_ uses these; possibly also _Balatro_.)

_Balatro_ is a video game that is sort of like video poker but with many jokers that have many special effects.

Mistigris was allegedly an early name for jokers when they were added to poker, and mistigris means pussy cat so hey we could have a cat card...

I'm not sure if jokers should be suited or not. I guess by default they are unsuited. (Or maybe suited to a special star suit all their own.) Not clear to me what the benefit of suiting them would be. That's just another face card.

Speaking of which, you can just add more regular face cards, I guess. Mechanically, this is quite simple, because they all have values determinable from their position (also in many games they all have identical values). But the art here is a real question mark, unless you just reuse the kings or whatver. (arbitrary art need) There are also a lot of names of ranks of nobility, like viscount, you could plunder for face card rank names (although presumably they would rank under the king and queen, realistically, so, that could get confusing). And given English names, such as "jack", come to think of it. Eventually you'll run out of latin letters to be the symbols for the rank, after which, idk, you just start using other unicode characters. Or you do something boring like just making them K2, K3... . This is boring, but at least has the benefit of being sort of funny, in a way.

You can add the tarot. Or, rather, the trumps or "major arcana" of a tarot deck, which is already a playing card game for certain games. I am not sure how these would be of use in poker, besides of course in high card (and the fool could still excuse you from the hand). And maybe in forming a straight. Perhaps a trump beats all other conventional hands even as high card, thus ruining the entire game of poker? I have not actually played enough tarot games to know how having 20ish trumps even works.

There is an extended tarot but I don't like it because it adds the new tarot cards into the middle, ruining the order. However, with technology we could accomodate this. Or just extend the tarot upwards a different way. (arbitrary art need)

### Suits

You could add more suits. I don't think there's a canonical set of symbols for the additional suits. This is actually a pretty good brief survey of some five-suited decks: https://deckofshields.com/five-suit-decks/ This wikipedia page also mentions a deck that just stole leaf from german decks https://en.wikipedia.org/wiki/Five-suit_bridge and this one mentions a fifth karuta suit of wheels.

The face cards for the additional suits (unless you decide to be lazy and just reuse the face cards from the other suits (perhaps one randomly chosen from each), which would be reasonable) should be as distinct from each other as the face cards for the regular suits. Not much more, not much less. (arbitrary art need)

(Would be funny to make one suit that goes completely crazy, though.)

I don't think it would be right to use the latin suits (cups, etc) in conjunction with the germanic suits, given that they already correspond and thus perhaps are arguably "the same" suit in some way (just different renderings). Although you could argue that they were just used identically in their own parallel universes, so to speak. Actually, yeah, I've come round to this idea! It's the opposite argument I would make about, say, the German Ober versus the English Queen, but whatever. Not sure how they would be ordered, though. I guess all card games order the suits arbitrarily anyway, so this order doesn't matter much. It wouldn't make sense to make the spanish cups suit different from the italian cups suit, for example, but it does make sense to count the english clubs suit different from the german acorn suit even though they descend from the same thing. (Note: due to the english clover suit already having the name "clubs", the latin clubs suit must be "batons", which is also a pretty popular translation for them.)

My comments about the Ober and the suits suggest to me that I should commission Modern Linear: 1. versions of all the suits (easy; that's just 6 icons or whatever) (this is a true variant that creates more cards) 2. variants of all the face cards so you can play with the Ober instead of the Queen, for example (this is just a stylistic variant that doesn't affect gameplay). Previously I had thought these were all part of the same theme variable, and since Modern Linear is themed on the english pattern i thought I didn't have to consider those other things. And I still might change my mind back, of course.

Four-color suits (where eg diamonds gets a different color than hearts to make telling them apart more easy) is just an art-style/accessibility option, and will not be considered a new suit. (unless...? but nah probably not. unless there's some really fun game to be had if you have sub-suits made of colors.) I will note that presumably the four colors would be whatever four colors are used to print face cards, so red black blue and yellow — but that's basically just pretending we live in the olden days and can only use a limited number of inks... and pretending poorly at that, since who knows what would actually have been cheaper back in those times. A scheme that uses orange and red and black and dark blue is also attractive with its own logic, treating the colors as sort of subspecies of other colors. But, in general, I'm thinking the colors will be "epiphenomenal" for my games, and not matter in and of themselves. Feel free to pallette swap as you wish.

The order of suits is not consistent between card games. One of the most popular is english name order: clubs ♣️, diamonds ♦️, hearts ♥️, spades ♠️. That is convenient, although it does raise the question of what happens if you want to add more suits (perhaps they get inserted alphabetically into the current order based on their names as well?). However, I think there are various properties that determine a canonical order of suits, which I will ultimately go with.

Firstly, color. I think, for purely aesthetic reasons, an ordering of suits would not make a black suit touch a black suit nor a red suit touch a red suit. This narrows it down to exactly these possible patterns: all permutations of RBRB and BRBR. For instance, arbitrarily as an example, ♣️♦️♠️♥️. Admittedly, this is less of a concern in a four-color deck of suitably different colors (pun intended, although not very good).

Secondly, and more importantly, since this uniquely determines the suits, the graphical menmonic. The order is ♠️♥️♣️♦️ because there is one point, two lobes, three lobes, and four points. This also makes diamonds the most valuable suit, which kind of makes sense (although, then again, kind of not). Luckily, this comports with the color requirement. So, I think this will be the canonical order of suits as far as I'm concerned. This also immediately suggests a star ⭐ as a natural 5th suit. It has five points, you see! And then maybe the latin suits after that (possibly plus a wacky fifth suit of its own), and the german suits, and various obscure suits, and then random shapes and symbols... for some reason I feel I should mention "gear" here.

This graphical mnemonic establishes a correspondence between the numbers 1–5 and five suits. After the 5th suit the mnemonic breaks down pretty quickly, unless the 6th is hexagons (a powerful shape) or a flower with n pedals or a crown with n points etc, but at some point there's gonna have to be a suit symbol that isn't graphically related to a number like that, I think. Also, circles could be the 0th suit (0 points) or just another random suit; I've never been a huge fan of having a 0th element in things so I guess I wouldn't do that. I think _DDG_ uses circles for pips of a null suit (which makes sense in that game because the suits have powers, so a null suit pip does normal stuff but with no bonus). Having this order 1–5 doesn't actually determine what beats what. Is 1 the first highest suit or the first lowest suit? For myself, I'm partial to the idea of quantity, so I think, eg, 4>3, and the fourth suit should beat the third suit. This has the added benefit that additional added suits will beat eariler suits, which probably affords slightly more exciting possibilities than if the new suits that are added are worse and worse. So, spades would be the lowliest suit (like a humble ditch-digger, perhaps) and hearts would beat it, and hearts would be beaten in turn by clubs, and so on.

## Cards

### Overview

#### Iclonic sets

Due presumably to a latent mental illness, I find myself captivated by what I will call "iconic sets". In a colloquial sense of the term iconic, like how a celebrity is iconic of their medium if they are famous enough, sort of. To insist on this this definition unambiguously, I will use the term "iclonic" for it. To shorten "iclonic set", I will sometimes use the term "iclonis" (plural "iclonises"). Which I will occassionally misspell "iconis" (pl. "iconises") — but, hey, that isn't an English word yet either, so, let's just declare that to be a synonym of iclonis to keep ourselves safe. Also, I keep finding myself wanting to write "icloni" and "iconi", so I'm making those alternative plural forms as well.

Anyone can write text, in the sense of scribbling some stuff down, with or without some thought behind it; in fact there's so much bespoke text that we can never sensibly encode it, but only sets like Unicode and the latin alphabet are iclonic.

In the same way, anyone can make cards as tokens and gamepieces, with whatever you want on them; and, indeed, many people have, and this is good. But they aren't going to be as iclonic as playing cards!

the surprise of finding secret members and hidden structures

many people are so captivated by icloni. four humors etc. correspondences. opposites.

the curious case of why so many enlightenment thinkers are assigning each day of the calendar some guy or thing to thing about (I don't really feel the pull of this one)

The days of the week are an iclonic set, but you won't get any secret members there, because the days of the week are used so practically that these would never survive (i guess). Unless maybe you had a fictional story or game with light time-travel elements where you shove more days before the end of the week to prolong your chance to complete something, maybe. Introducing... Saturday... 2!

(should I explain the reference to the peggle 2 E3 presentation? hmm)

One thing about iclonic sets is that they all have for their members abstracta in the first place. This salt shaker in front of me as I write is not the member of any iclonic set. But salt might be. (Indeed, it's part of the "salt and pepper" iclonic set.) No particular token card that you carry around is part of an iclonic set; the card is an instance of a class (say, Three Of Diamonds) that is part of the iclonic set (playing cards).

Of course, this can get a little mixed up, and it is one of the little joyous amusing suprises in life (perhaps an "[improper heirarchy](https://www.youtube.com/watch?v=ar9WRwCiSr0)" joke as Tom 7 would say) when a *particular* thing ends up in an iclonic set, such as how the Rain Man in hanafuda is the particular man Ono no Michikaze, or how the face cards in the Paris pattern of playing cards are particular historical people (although that is less funny, because it itself forms a pattern).

A lot of iclonises, maybe all of them, are pretty much just made up. Conventional. Even if they are naturally occurring, our decision to group them together is usually somewhat arbitrary. For example: besides their names, the cardinal directions are fairly described as naturally occurring. However, the fact that we decided we *wanted* a set that has orthogonal axes instead of, say, six axes aligned to north, is still pretty much our arbitrary, conventional choice. There are a couple iclonises I think are completely non-conventional, like {true and false}. We could have invented a system like {true, kinda, and false}, but... get real. That one was given to us by God. And so with the primes, except for the question of whether 1 is a prime. But most of them, most icloni are just a whimsical collection of objects brought together by convention, like {salt and pepper} or the months of the year.

I think a lot of people become obsessed with icloni because they think they *aren't* conventional. The fact that you can map the four humors to the four cardinal directions helps you divine the will of God, in their mistaken view. But me? I just like 'em!

Being public domain really helps your iclonicity, in my view. I don't think it's a necessary condition (nor is it sufficient, for all you playing at home), but it does help — it's related to the idea that there are many tokens of this set being produced, and thus the set is very common.

Many people get obsessed with tracking down all the individual decks of cards made, or all the games that are actually played with cards, but those things don't interest me. (Except, of course, in that looking at all of the card games ever played helps me figure out what the cards are and do.) I suppose it's similar to how many people get obsessed with fonts (to the extent that font designer are making 100,000 identical helvetica fonts) but I'm more of a symbol obsessive and don't care much about the fonts. Just a different level of abstraction we find appealing, I suppose.

I'm unclear if the appeal of cards for cartomancy is also driven by the same underlying psychological attraction to cards that inspires people to obsess over and investigate them, and I don't know enough people like this to speculate. Those two bitter rival (or perhaps... lover?) camps, so divided in their attitudes, yet united in their love of the objects & perhaps iclonis.

### Research resources

I mainly relied on Wikipedia pages for my research here. There is a vast hobbyist blogosphere, some blogs of which are even still alive, filled with information on particular decks and card games, but due to my level of abstraction in this endeavor this is usually not very useful to me. I have also considered joining the international association of card games to read their journals.

I am also just aware of things by running into them in my life, and will mention these when appropiate, although likely they are not important. Here are some common acronyms I might use on their own (I will try to remember to always _italicize_ them) with no explanation, explained here:
* _DDG_: _Dungeons & Degenerate Gamblers_, a video game
* _B_: _Balatro_, a video game
* _DDGB_: _DDG_, and possibly also _B_ (I played a lot more of _DDG_ than _B_, so my memories of _B_ are often hazier)
* _I_: _Inscryption_, a video game

If I don't link to some source, you can pretty much just assume I'm reading it off wikipedia, and maybe corroborating it with some other sources. I may also give you a link to Wikipedia since this is a sketchy overview and that's step one to getting more information (before step 2, which is, idk, reading an actual book about it, maybe).

### Concepts


Ranks

Suits (and metasuits?)

Patterns (I'm not sure I understand this term nor how specific it is exactly)

#### Size and shape

I like the size and shape of standard playing cards. In history, cards have come in many shapes and sizes, but I would use the contemporary standard playing card size for these cards, and adapt other cards to that if need be.

#### Styles

Styles are kind of like "fonts", but for playing cards. It would be misleading for me to call them "fonts" because cards typically also have printed text on them, which uses an actual font. TODO: I should figure out the precise taxonomy of playing card elements. Is style sub-pattern or a general term that includes pattern? Should I specify "art style"? "Look and feel"? "Dress"?

Jokers usually have some wacky style chosen to express the individuality of the individual manifacturer. Sometimes they are identical or one is slightly different than the other (such as, being printed in color or having an extra logo) and might be higher or lower than the other in some card games that use them. They are usually based on jesters or clowns, but sometimes not.

##### Modern Linear
I don't know the term (if there is one) for the minimalist-ornate style the modern english pattern commonly gets printed with. Did Bicycle invent it? Sadly their website is pretty uninterested in showing samples. In the interest of clarity I'm going to call this very-popular card style "Modern Linear" (I won't consistently capitalize it, but it is a proper noun, my name for this particular style). I love modern linear. The other styles are ok, but I modern linear is like crack to me. In this document I will repeated muse about creating a full, french-suited, english-patterned, generalized hyper-poker deck, in modern linear style, which I would then place into the public domain.

Modern linear is probably based on the tradition of woodblock printing playing cards, even though those technological limitations no longer apply, but I'm just guessing on that.

Modern linear is the basis of most modern playing cards, and most companies that sell playing cards have their own particular flavor of Modern Linear.

I should decide if modern linear is more or less specific than english pattern. I have a deck of playing cards (swiss flag backs) that is basically Modern Linear but german suits. Is that German Modern Linear, or, like Modern Linear but German? I'm leaning towards the former.

### History (TODO)

Chinese money cards, probably, although no one is sure as far as I know.

Probably some really ye olde middle eastern cards I don't really know anything about.

Some old european playing cards that never really were in wide circulation

Regular playing cards & variants

The tarot & variants

The [Rider–Waite–Smith Tarot](https://en.wikipedia.org/wiki/Rider–Waite–Smith_Tarot) is a very nice tarot that has been very influential. It is latin-suited, and is largely used for mysticism. Its main infuriating idiosyncracy is swapping Justice and Strength (as is so often done in this modern world, har har) for its own perfideous reasons. I mean, presumably the deck still functions the same for actual games, which mostly just use the numerical value of the trump, but why would you ruin a perfectly good iclonis ordering like this?! (The answer is: spirituality reasons.) 

Animal tarot

Tarot Nouveau

As far as I know there is no Modern Linear rendition of the tarot. Guess I'll have to sink my savings into commissioning a full deck of face-card style tarot cards. Oh well!

Now that Minchiate has pointed it out: I have no idea why the classic tarot includes only 3 of the 4 cardinal virtues (an iclonic set! albeit one I don't really care about), eschewing Prudence but keeping Fortitude, Temperance, Justice.

Hanafuda cards (note that hanafuda cards canonically have 13 *suits* and 4 *ranks*, which is crazy but whatever). Also those crazy poem cards I guess. Also it's weird how the japanese had no playing cards until the portguese imported them or whatever even though they life right next to China.

I think there are asian regional variants of these cards, and maybe their own cards (descended from Chinese money cards), but I don't know much about them.

Jokers

Rules/blank cards?

More suits, colors, and jokers

The joker vs the fool (convergent evolution?)

I guess that's pretty much it.

### Various

Loteria isn't a card game exactly, but it's perfect for me.

I keep looking up Karnöffel because of the hogs in the video game _Inscryption_, and then I realize it's unsuitable for some reason (which reason I usually forget).

I thought I had discovered a new tarot-like set of cards in [Lenormand cards](https://en.wikipedia.org/wiki/Lenormand_cards), which are labelled things like "Rider" and "House". But these cards have already gone to the trouble of telling you what conventional playing card they correspond to, which I guess just makes them a themed deck of playing cards 🤷‍♂️. TODO: need a name for these. "Pattern", like spanish or french pattern? Then again, those associations could just be ignored or something (although I suppose they are already quite strong associations).

#### Extra sets

Billiard balls, especially pool balls. Pool is an interesting game because it's also quite amenable to generalization in various ways, and is already a complicated game that has been complixified multiple times — much like card games. The basic form of pool would be something like, just hitting a ball with a stick and trying to get it to go where you want. Even the fact that you have to hit a cue ball instead of the ball directly is a bit advanced. Trying to learn 8-ball pool (which is played with 15 balls, by the way; the 8 is just the most important one) is a hilarious process of trying to just hit the cue ball while you constaintly foul/scratch and aren't even thinking about the color of the balls yet. Anyhow, these also have ranks (numbers) and suits (solids-vs-stripes or color, based on the game I guess). These could be graphically adapted to playing cards.

The Uno cards are actually kind of iclonic, even though as far as I know Uno is still proprietary. Oddly enough, there is a correspondence between Uno special cards and 52's face cards, in the sense that they both exist extra to the number cards, but the most popular generic of Uno is the card game Crazy Eights, which just uses some number cards to be the special cards instead. I guess there are many of these "shedding" games, and maybe one corresponds closer. Anyway, I'm not sure what intellectual property protections apply to Uno. Obviously they have the trademark and presumably trade dress, but it's impossible to copyright the connect of "reverse" and the Uno Reverse icon is pretty simple, so presumably you could make French-suited uno-type cards and add them to a deck of playing cards without comment ("without comment", by which I mean "not misleading the consumer to think you are actually Uno, the proprietary product). This would probably be legal in the USA (this is not legal advice and I am not your attorney) but might be illegal in different regimes. I'm not sure if we can call the collection-of-game-mechanics presented by the branded-product Uno "uno" or if the law will force us to use some weird name like "nou" or "nuo" (or perhaps one of the shedding games already discussed), but games in the uno family are certainly known as unoids ("oo-noids" /ˈuː.nojdz/) or perhaps nuoids. (The company that makes Uno makes many Uno-branded unoids itself.) In the USA you can't copyright game mechanics and it's unlikely that they've patented them. Again, other countries may be different Anyway, the cards in question (with my unicode approximations of the symbols) are "Skip"(🛇), "Draw Two"(+2 ⧉), and "Reverse"(🔃︎). The deck also contains four "Wild" cards and four "Wild Draw Four", which should be depicted with the appropriate suits in a 2×2 grid. In Uno the suits are red, blue, yellow, green. Uno is played with a deck that is basically two standard decks, aces low (=1), no faces, no jokers, no tens. Plus four 0s (one of each suit); 8 skip, reverse, & +2 (two of each suit); 4 wilds; and 4 wild draw four. Maybe some day I will commission some french-suited modern linear unoid cards.

Various sources online, which might just be made up spam for all I know, or might be cribbing from some authorative source without credit, claim that when Merle Robbins invented Uno, based on Crazy Eights, he did so by by marking the king in a standard deck as uno reverse, and the queen as uno skip, and aces were wild. Presumably the jack was +2 but the sources don't list that. Weirdly, these sources do not mention that the uno rule of saying "uno" was probably taken from mau mau, which has a similar rule ("mau!"). I can only assume this rule was taken from mau mau and is not a parallel invention, just based on low base rates of people independently inventing that rule. Maybe the local variant of crazy eights had this rule absorbed from mau mau. Anyway, if true, this assertion plausibily establishes a canonical correspondence between the face cards and the uno special cards — although we could of course just ignore that and treat these as new cards instead.

There is another shedding game called Whot!, which seems maybe worth mentioning, given its shedding-type and strange deck.

Dice are iclonic, and they could be graphically adapted to playing cards (I'll call this gradaptable, for short) — both the normal pips of dice and the platonic solid dice — but I'm not really interested in that. (there are plenty of iclonic sets that could be graphically adapted to playing cards but are not particularly interesting to, like the four humors, the latin letters, etc).

The stock characters of the commedia dell'arte (hence: cda) are fairly iclonic, and could be adapted to playing cards. Some have been in the past! I would need to know a lot more about the characters in the commedia dell'arte. In particular, I would like to know if they form a closed set (by which I mean a finite known collection), since every time I see the cda mentioned it seems to be in conjunction with a new "stock character" thereof that I have never heard of before.

The american presidents would be a fun idea to create a tarot-like playing card game for. That's before you even get into trump/Trump jokes lol. I think the States (& perhaps also the territories) of the United States Of America are techincally an iclonic set, but I don't find them very interesting; perhaps they could be used as a play element in the Presidents card game.

Oh... honorary mention here to Justine Lai's painting series "Join Or Die", which depicts her and every president (is it every president? I've never been able to find the complete collection to substantiate that claim) in, um, congress. It's not really relevant to this card game idea but hey it's an iclonic set, good job Justine. Maybe she could be a card in the game. (I'm not sure if she actually wants attention for this or not, since she seems to have taken most of her web prescence, but that's possibly just incidental.) Uhhh history shows that odds are I'm never going to make this game I'm scheming about, btw. But I do scheme!

The pieces of chess are iclonic, and could be graphically adapted to playing cards. There is some overlap here, for instance in "king" and "queen". Also, I think this gets you to chinese chess, which actually also comes from the chinese money cards above? There's a convulted history here, I think. The iclonic set of chess pieces also includes fairy chess pieces.

Mah jong: seems iclonic, and gradptable. I don't know anything about mah jong, though. And I'm not super interested in it, although I wouldn't rule it out.

[Zener cards](https://en.wikipedia.org/wiki/Zener_cards) these seem good for this purpose. They are famous enough, and as simple shapes cannot be under copyright. I think _DDG_ uses these, possibly also _B_.

_DDGB_ have a lot of fun using things like the "get out of jail free" card from monopoly, and the "pot of greed" card from yu-gi-oh, and while these are fun and iconic, they are not part of a relevant iclonis so I'm not really going to consider them seriously.
