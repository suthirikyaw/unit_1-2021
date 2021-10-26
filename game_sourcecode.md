```.py
import time
import Validation
import Instructions
import Date
import Ending

good_decision = 20
bad_decision = -20
score = 0
start_time = time.time()

print("[Due to some technical difficulties and some poor planning, some options are unavailable. Thank you for understanding :)]")
print("")
Instructions.Instructions()
time.sleep(4)
print("---------------------------------------------------------------------------------------------------------")
time.sleep(2)
print("[unknown] ....h-hello?....  >")
enter = input()
print("1. Hello? \n"
      "2. Who is this?")
dialogue = int(input(">> "))
dialogue = Validation.validationTwo(dialogue)
if dialogue == 1:
    print("[you] Hello?  \n")
elif dialogue == 2:
    print("[you] Who is this? \n")
time.sleep(2)
print("[unknown] oh..my god! Hello? Can you hear me?  >")
enter = input()
print("[you] Yes I can hear you....who is this? \n")
time.sleep(2)
print("[unknown] I can't believe this...how are you connected to my radio right now? >")
enter = input()
print("[you] I fix radios and electronics for fun. I just finished fixing this one and booted it up...only to come to your channel. \n")
time.sleep(2)
print("[unknown] Man, I thought I was going to die out here.... >")
enter = input()
print("1. Are you okay? (long intro) \n"
      "2. What happened? (short intro) ")
choice = int(input(">> "))
choice = Validation.validationTwo(choice)
if choice == 1:
    print("[you] Are you okay? \n")
    time.sleep(2)
    print("[unknown] Yeah...I think so. I'm not visibly bleeding. Or missing a limb. \n "
          "Maybe I hit my head and I'm hallucinating talking to someone on a radio that should've been destroyed.. >")
    enter = input()
    print("[you] I can assure you, I'm very real. \n")
    time.sleep(2)
    print("[unknown] That's exactly what a hallucination would say. >")
    enter = input()
    print("[you] Haha you seem fine to me....can you tell me what's happening? \n")
    time.sleep(2)
    print("[unknown] Right, yeah so I was out on my boat sailing and next thing I know I wake up on this shore. I think I'm stranded on an island. > ")
    enter = input()
    print("[you] You can't remember what happened in between? \n")
    time.sleep(2)
    print("[unknown] I remember the weather turning on me, I swear it was a nice day out to go on my boat. \n"
          " The rest...beats me. I don't even know if it's the same day or the next. > ")
    enter = input()
    print("[you] Its", Date.weekday(), "the", Date.date() + "th", "if that helps. \n")
    time.sleep(2)
    print("[unknown] So it's the next day. I must've passed out for quite a while. >")
    enter = input()
    print("[you] Can you remember your name? \n")
    time.sleep(2)
    print("[Miles] Fortunately I'm not that beaten up. I'm Miles. You? >")
    enter = input()
    name = input("I'm >> ")
    time.sleep(2)
    print(f"[Miles] Well even though this is the worse possible way to meet, It's nice to talk to you, {name}. >")
    enter = input()
    print("[you] You too, I guess. Is there anyway I can get you help? Do you have any idea where you might be? \n")
    time.sleep(2)
    print("[Miles] Not a clue. I've never seen this area before, I must've sailed quite a long way. >")
    enter = input()
    print("[you] This radio you're speaking on...do you have spare batteries? \n")
    time.sleep(2)
    print("[Mile] oh god no, I don't have any. It's also taken a hit so I'm not sure how long it'll be before it dies. >")
    enter = input()
    print("[you] Then we should hurry up and start finding ways to get help. \n")
    time.sleep(2)
    print("[Miles] The sun might be going down soon so making a fire might be my priority...or maybe I can do that after finding some food because I'm starving. What should I do? >")
    enter = input()
    print("1. Find food. \n"
          "2. Get wood to make a fire.")

elif choice == 2:
    print("[you] What happened? \n")
    time.sleep(2)
    print("[unknown] I don't remember all the details because my head still hurts but I was out on my boat sailing. It was sunny and the day was perfect... \n"
          "then the weather suddenly went south and before I knew it I woke up on this shore. >")
    enter = input()
    name = input("[you] ..well my name's >> ")
    print("[you] Can you remember yours? \n")
    time.sleep(2)
    print("[Miles] Thankfully I'm not that beaten up. I'm Miles. >")
    enter = input()
    print("[you] Miles, this radio you're talking on...do you have spare batteries? \n")
    time.sleep(2)
    print("[Miles] ...oh my god, I don't. It's also taken a hit so I'm not sure how long we can connect to each other. >")
    enter = input()
    print("[you] Is there any ways I can get you help? Do you know where you might be? \n")
    time.sleep(2)
    print("[Miles] I don't have a single clue. The only thing I can do is try an survive and wait for help. If there's any coming. >")
    enter = input()
    print("[you] Do you think you should gather some supplies? Food? \n")
    time.sleep(2)
    print("[Miles] The sun might be going down soon maybe making a fire should be priority....or I could do that after finding food. What should I do first? >")
    enter = input()
    print("1. Find food. \n"
          "2. Get wood to make a fire.")


choice1 = int(input(">> "))
choice1 = Validation.validationTwo(choice1)
if choice1 == 1:
    score += bad_decision
    print("[you] Maybe you should find some food while it's still light out. You can make a fire later. \n")
    time.sleep(2)
    print("[Miles] Yeah you're right, that sounds wise. > ")
    enter = input()
    print("[you] Where are you going to find it, though? \n")
    time.sleep(2)
    print("[Miles] Well the shores a place to start, I could try my luck with some animals. But there's also a pack of trees nearby. It might be a forest. >")
    enter = input()
    print("1. Explore the forest. \n"
          "2. Catch sea creatures. (unavailable)")
    choice2 = int(input(">> "))
    choice2 = Validation.validationTwo(choice2)
    if choice2 == 1:
        score += good_decision
        print("[you] Forests are full of things, you might have more luck finding food there. \n")
        time.sleep(2)
        print("[Miles] Off to the forest we go then. Hopefully rabid wild animals aren't one of them. >")
        enter = input()
        print("[you] I'm more worried about the creepy crawlies on the forest floor. \n")
        time.sleep(2)
        print("[Miles] Are you saying you'd rather meet a hostile wild animal than a small little bug? >")
        enter = input()
        print("1. I'd rather wrestle a huge lion bare-handed than have a creepy bug crawl up my leg. \n"
              "2. You're right, maybe a weird insect isn't worse than a feral animal. \n"
              "3. I'd light the forest on fire either way.")
        dialogue = input(">> ")
        dialogue = Validation.validationThree(dialogue)
        if dialogue == 1:
            time.sleep(2)
            print("[Miles] Wow, I've never been scared of bugs. Unless they're poisonous I'd love to keep it. >")
            enter = input()
            print("[you] You're weird. \n")
            time.sleep(2)
            print("[Miles] Not as weird as being scared of something a million times smaller than you. >")
            enter = input()
        elif dialogue == 2:
            time.sleep(2)
            print("[Miles] Yeah, and I wouldn't have the strength to face off a house cat much less a wild bear or something. >")
            enter = input()
        elif dialogue == 3:
            time.sleep(2)
            print("[Miles] That's a bit extreme. >")
            enter = input()
            print("[you] I think it's a very appropriate reaction. \n")

        print("[you] Anyways, have you entered the forest yet? \n")
        time.sleep(2)
        print("[Miles] Yeah, it's not as dense as I thought it would be. It's quite nice actually. >")
        enter = input()
        print("[you] Anything that's edible? \n")
        time.sleep(2)
        print("[Miles] I'm still looking around. Not an animal or fruit in sight yet. Wait >")
        enter = input()
        print("[you] Did you find anything? \n" )
        time.sleep(2)
        print("[Miles] I found a bunch of bushes. All of them had different little berry things on it. >")
        enter = input()
        print("[you] Does any one of them look familiar? You probably shouldn't be eating random fruit in forests. \n")
        time.sleep(2)
        print("[Miles] No, they're red, purple and green. None of them look like anything I've seen. But I'm so hungry. >")
        enter = input()
        print("[you] I really think you shouldn't eat any of it. \n")
        time.sleep(2)
        print("[Miles] I don't think they look that dangerous. What's the worst that could happen? >")
        enter = input()
        print("[you] Your death isn't the worst that could happen? \n")
        time.sleep(2)
        print(f"[Miles] Come on, {name} just pick a color. >")
        enter = input()
        print("1. Red \n"
            "2. Purple \n"
            "3. Green")
        choice3 = int(input(">> "))
        choice3 = Validation.validationThree(choice3)
        if choice3 == 1:
            score += good_decision
            print("[you] Red's usually the worst possible choice but maybe that's WHY you should eat red? \n")
            time.sleep(2)
            print("[Miles] That makes sense. Plus cherries are red and I love cherries. Bon Apetit. >")
            enter = input()
            print("[you] Are you good, Miles? \n")
            time.sleep(1)
            print("[Miles] .... >")
            enter = input()
            print("[you] Miles?? \n")
            time.sleep(1)
            print("[Miles] ....")
            time.sleep(1)
            print("[Miles] ...BOO. I'm just playing. Plus if it was poisonous it would take a while to kill me so. \n")
            enter = input()
            print("[you] How are you joking about something so serious right now?")
            time.sleep(2)
            print("[Miles] I didn't drop dead so might as well make the most out of a situation. I'd rather not think about how I could die out in the middle of nowhere on an island alone right now. >")
            enter = input()
            print("[you] You're right, I'm sorry. I just got worried. \n")
            time.sleep(2)
            print("[Miles] It's okay, I'm glad you're here or I'd go insane. >")
            enter = input()
            print("[Miles] Hey, the trees here are huge. I think I just got an idea. >")
            enter = input()
            print("[you] Are you thinking of climbing one? \n")
            time.sleep(2)
            print("[Miles] It looks doable. If I can climb the tallest one I can find maybe I can scope out whats around here. What do you say? >")
            enter = input()
            print("1. Climb the tree. \n"
                  "2. Don't climb the tree.")
            choice4 = int(input(">> "))
            choice4 = Validation.validationTwo(choice4)
            if choice4 == 1:
                score += good_decision
                print("[you] If you're sure you can get to the top safely, I say go for it.")
                time.sleep(2)
                print("[Miles] Alright, here goes....")
                time.sleep(1)
                print("[Miles] Got a good grip")
                time.sleep(1)
                print("[Miles] Doing fine so far...")
                time.sleep(1)
                print("[Miles] Almost there... >")
                enter = input()
                print("[you] Are you good, Miles?")
                time.sleep(2)
                print("[Miles] Yes, and I think I see something. Its a structure of some sort. A tower? >")
                enter = input()
                print("[you] A tower? Are you sure? Why would there be a random building in the middle of an island?")
                time.sleep(2)
                print(f"[Miles] Only one way to find out. What do you say, {name}?")
                enter = input()
                print("1. Go to the tower. \n"
                      "2. Don't go to the tower.")
                choice5 = int(input(">> "))
                choice5 = Validation.validationTwo(choice5)
                if choice5 == 1:
                    score += good_decision
                    print("[you] Why WOULDN'T you go to that tower? There might be people who can help you or anything else that can help you.")
                    time.sleep(2)
                    print("[Miles] I don't even know why I asked, it's obviously the right thing to do. Back down this tree we go. >")
                    enter = input()
                    print("[you] Do you think you'll make it there before the sun goes down?")
                    time.sleep(2)
                    print("[Miles] It doesn't look THAT far but we'll just have to see... hey don't you think a tower here sounds sketchy? >")
                    enter = input()
                    print("1. Maybe this is an island full of dark secrets and you're stumbling upon a really dangerous territory and someone will kill you for learning too much. \n"
                          "2. Nope sounds perfectly fine to be honest. \n")
                    dialogue = int(input(">>"))
                    dialogue = Validation.validationTwo(dialogue)
                    if dialogue == 1:
                        print(f"[Miles] Wow that's very reassuring, {name} >")
                        enter = input()
                        print("[you] You asked. \n")
                        time.sleep(3)
                    elif dialogue == 2:
                        print("[Miles] I feel like you don't fully believe that but for the sake of my sanity, I'll ignore it.")
                        enter = input()
                        print("[you] Whatever floats your boat, dude. I'm just happy there's a development. \n")
                        time.sleep(3)

                    print("[Miles] Finally, I see it. It's a tall tower, looks kind of unstable. The stairs are making me nervous. >")
                    enter = input()
                    print("[you] Are you chickening out? \n")
                    time.sleep(2)
                    print("[Miles] No, I've come this far. >")
                    enter = input()
                    print("[you] Are you good? \n")
                    time.sleep(2)
                    print("[Miles] Yeah, just trying not to look down. >")
                    enter = input()
                    print("[you] Be careful. \n")
                    time.sleep(2)
                    print("[Miles] Woah, look at the view. I entered the little house on top. I can see almost everything, must be why it's so high. >")
                    enter = input()
                    print("[you] There's no one there?")
                    time.sleep(2)
                    print("[Miles] Not a soul...it looks abandoned. Things are dusty and out of order. But LOOK THERE'S A RADIO AND A MONITOR HERE! >")
                    enter = input()
                    print("[you] WHAT? CHECK IT OUT RIGHT NOW! \n")
                    time.sleep(2)
                    print("[Miles] Please please please be working. >")
                    enter = input()
                    print("[you] Well???")
                    time.sleep(2)
                    print("[Miles] One more second...")
                    time.sleep(1)
                    print("[Miles] aaand GOT IT, IT'S STARTING.")
                    enter = input()
                    print("[you] Do you think you'll get anything? \n")
                    time.sleep(2)
                    print("[Miles] It's on and running but it's not picking up anything so far. >")
                    enter = input()
                    print("[you] Maybe it was too good to be true. \n")
                    time.sleep(2)
                    print("[Miles] Hey, don't be negative now. It might pick something up. >")
                    enter = input()
                    print("[you] I think the tower may be abandoned for a reason. \n")
                    time.sleep(2)
                    print("[Miles] Maybe...oh hello?? >")
                    enter = input()
                    print("[you] Did you get in contact with someone? \n")
                    time.sleep(2)
                    print("[Miles] ..can you please state your name? >")
                    enter = input()
                    print("[Miles] Miles Bonnet, sir. >")
                    enter = input()
                    print("[Miles] ..h.ow...did you end up...h..re Miles? >")
                    enter = input()
                    print("[Miles] I had a boating accident and was washed up here, sir. I don't even know where I am. >")
                    enter = input()
                    print("[Miles] there are emergency boats on the ....side of the island...near the ...cks...just beside them.. >")
                    enter = input()
                    print("[Miles] Hello, sir? On which side of the island? Near where? >")
                    print("ENDING INCOMPLETE. THANK YOU FOR PLAYING UP UNTIL THIS POINT.")
                    print(f"Score = {score} \n"
                          f"Time = {time.time() - start_time}")
                elif choice5 == 2:
                    score += bad_decision
                    print("[you] I don't think it's a good idea right now. You're starving anyways, you need to find more food and it might take too long.")
                    time.sleep(2)
                    print("[Miles] I don't know...I ate the berries so they should sustain me a bit. >")
                    enter = input()
                    print("[you] Whatever you say, you asked me for my opinion.")
                    time.sleep(2)
                    print("[Miles] Okay, you're right. I'll prioritize food and warmth first. Just let me get down this tree firs- WOAH >")
                    enter = input()
                    print("[you] MILES? ARE YOU OKAY?")
                    print("[Miles] AHHHHHHHHHH >")
                    enter = input()
                    print("[DISCONNECTED] >")
                    enter = input()
                    print("Maybe if Miles was a bit more careful he'd still be alive. Guess he just wasn't meant to survive :/ \n")
                    print("BAD ENDING: DON'T CLIMB ABNORMALLY TALL TREES. Thank you for playing.")

            elif choice4 == 2:
                score += bad_decision
                # complete this ending
                print("ENDING INCOMPLETE. THANK YOU FOR PLAYING IT UP UNTIL THIS POINT")
                print(f"Score = {score} \n"
                      f"Time = {time.time() - start_time}")
        elif choice3 == 2:
            score += good_decision
            print("[you] Purple seems safe enough. Good luck.")
            time.sleep(2)
            print("[Miles] Red and green looks too daunting. Bon Apetit.")
            enter = input()
            print("[you] Are you good, Miles?")
            time.sleep(1)
            print("[Miles] .... >")
            enter = input()
            print("[you] Miles?? ")
            time.sleep(1)
            print("[Miles] ....")
            time.sleep(1)
            print("[Miles] ...BOO. I'm just playing. Plus if it was poisonous it would take a while to kill me so.")
            enter = input()
            print("[you] How are you joking about something so serious right now?")
            time.sleep(2)
            print(
                "[Miles] I didn't drop dead so might as well make the most out of a situation. I'd rather not think about how I could die out in the middle of nowhere on an island alone right now. >")
            enter = input()
            print("[you] You're right, I'm sorry. I just got worried.")
            time.sleep(2)
            print("[Miles] It's okay, I'm glad you're here or I'd go insane. >")
            enter = input()
            print("[Miles] Hey, the trees here are huge. I think I just got an idea. >")
            enter = input()
            print("[you] Are you thinking of climbing one?")
            time.sleep(2)
            print(
                "[Miles] It looks doable. If I can climb the tallest one I can find maybe I can scope out whats around here. What do you say? >")
            enter = input()
            print("1. Climb the tree. \n"
                  "2. Don't climb the tree. (unavailable)")
            choice4 = int(input(">> "))
            choice4 = Validation.validationTwo(choice4)
            if choice4 == 1:
                score += good_decision
                print("[you] If you're sure you can get to the top safely, I say go for it.")
                time.sleep(2)
                print("[Miles] Alright, here goes....")
                time.sleep(1)
                print("[Miles] Got a good grip")
                time.sleep(1)
                print("[Miles] Doing fine so far...")
                time.sleep(1)
                print("[Miles] Almost there... >")
                enter = input()
                print("[you] Are you good, Miles?")
                time.sleep(2)
                print("[Miles] Yes, and I think I see something. Its a structure of some sort. A tower? >")
                enter = input()
                print("[you] A tower? Are you sure? Why would there be a random building in the middle of an island?")
                time.sleep(2)
                print(f"[Miles] Only one way to find out. What do you say, {name}?")
                enter = input()
                print("1. Go to the tower. \n"
                      "2. Don't go to the tower.")
                choice5 = int(input(">> "))
                choice5 = Validation.validationTwo(choice5)
                if choice5 == 1:
                    score += good_decision
                    print("[you] Why WOULDN'T you go to that tower? There might be people who can help you or anything else that can help you.")
                    time.sleep(2)
                    print("[Miles] I don't even know why I asked, it's obviously the right thing to do. Back down this tree we go. >")
                    enter = input()
                    print("[you] Do you think you'll make it there before the sun goes down?")
                    time.sleep(2)
                    print("[Miles] It doesn't look THAT far but we'll just have to see... hey don't you think a tower here sounds sketchy? >")
                    enter = input()
                    print("1. Maybe this is an island full of dark secrets and you're stumbling upon a really dangerous territory and someone will kill you for learning too much. \n"
                        "2. Nope sounds perfectly fine to be honest. \n")
                    dialogue = int(input(">>"))
                    dialogue = Validation.validationTwo(dialogue)
                    if dialogue == 1:
                        print(f"[Miles] Wow that's very reassuring, {name} >")
                        enter = input()
                        print("[you] You asked.")
                        time.sleep(3)
                    elif dialogue == 2:
                        print(
                            "[Miles] I feel like you don't fully believe that but for the sake of my sanity, I'll ignore it.")
                        enter = input()
                        print("[you] Whatever floats your boat, dude. I'm just happy there's a development.")
                        time.sleep(3)

                    print( "[Miles] Finally, I see it. It's a tall tower, looks kind of unstable. The stairs are making me nervous. >")
                    enter = input()
                    print("[you] Are you chickening out?")
                    time.sleep(2)
                    print("[Miles] No, I've come this far. >")
                    enter = input()
                    print("[you] Are you good?")
                    time.sleep(2)
                    print("[Miles] Yeah, just trying not to look down. >")
                    enter = input()
                    print("[you] Be careful.")
                    time.sleep(2)
                    print(
                        "[Miles] Woah, look at the view. I entered the little house on top. I can see almost everything, must be why it's so high. >")
                    enter = input()
                    print("[you] There's no one there?")
                    time.sleep(2)
                    print(
                        "[Miles] Not a soul...it looks abandoned. Things are dusty and out of order. But LOOK THERE'S A RADIO AND A MONITOR HERE! >")
                    enter = input()
                    print("[you] WHAT? CHECK IT OUT RIGHT NOW!")
                    time.sleep(2)
                    print(
                        "[Miles] Please please please be working. I'll stop being an atheist and worship whatever God there is out there. >")
                    enter = input()
                    print("[you] Well???")
                    time.sleep(2)
                    print("[Miles] One more second...")
                    time.sleep(1)
                    print("[Miles] aaand GOT IT, IT'S STARTING.")
                    enter = input()
                    print("[you] Do you think you'll get anything?")
                    # complete this ending
                    print("ENDING INCOMPLETE. THANK YOU FOR PLAYING UP UNTIL THIS POINT.")
                    time = time.time() - start_time
                    print(f"Your score = {score} \n"
                          f"Your time = {time.time() - start_time}")
                    Ending.ending(score, time)
                    print("1. Find player. \n"
                          "2. Display players. \n"
                          "3. End game.")
                    end = int(input(">> "))
                    if end == 1:
                        print("Enter the player username you want to find.")
                        name = input(">> ")
                        Ending.find(name)
                    elif end == 2:
                        Ending.display()
                    elif end == 3:
                        print("Thank you for playing.")
                elif choice5 == 2:
                    score += bad_decision
                    print("[you] I don't think it's a good idea right now. You're starving anyways, you need to find more food and it might take too long.")
                    time.sleep(2)
                    print("[Miles] I don't know...I ate the berries so they should sustain me a bit. >")
                    enter = input()
                    print("[you] Whatever you say, you asked me for my opinion.")
                    time.sleep(2)
                    print(
                        "[Miles] Okay, you're right. I'll prioritize food and warmth first. Just let me get down this tree firs- WOAH >")
                    enter = input()
                    print("[you] MILES? ARE YOU OKAY?")
                    print("[Miles] AHHHHHHHHHH >")
                    enter = input()
                    print("[DISCONNECTED] >")
                    enter = input()
                    print("Maybe if Miles was a bit more careful he'd still be alive. Guess he just wasn't meant to survive :/ \n")
                    print("BAD ENDING: FALLEN TO HIS DEATH. \n")
                    time = time.time() - start_time
                    print(f"Your score = {score} \n"
                          f"Your time = {time.time() - start_time}")
                    Ending.ending(score, time)
                    print("1. Find player. \n"
                          "2. Display players. \n"
                          "3. End game.")
                    end = int(input(">> "))
                    if end == 1:
                        print("Enter the player username you want to find.")
                        name = input(">> ")
                        Ending.find(name)
                    elif end == 2:
                        Ending.display()
                    elif end == 3:
                        print("Thank you for playing.")
            elif choice4 == 2:
                score += bad_decision
                # complete this ending
                print("ENDING INCOMPLETE. THANK YOU FOR PLAYING IT UP UNTIL THIS POINT. \n")
                time = time.time() - start_time
                print(f"Your score = {score} \n"
                      f"Your time = {time.time() - start_time}")
                Ending.ending(score, time)
                print("1. Find player. \n"
                      "2. Display players. \n"
                      "3. End game.")
                end = int(input(">> "))
                if end == 1:
                    print("Enter the player username you want to find.")
                    name = input(">> ")
                    Ending.find(name)
                elif end == 2:
                    Ending.display()
                elif end == 3:
                    print("Thank you for playing.")
        elif choice3 == 3:
            score += bad_decision
            print("[you] Green's always a positive colour. Green means good right? \n")
            time.sleep(2)
            print("[Miles] Makes sense. It does look a bit TOO green like it's glowing but maybe it's the extra nutrients. Bon Apetit. >")
            enter = input()
            print("[you] Are you good, Miles? \n")
            time.sleep(1)
            print("[Miles] .... >")
            enter = input()
            print("[you] Miles?? \n")
            time.sleep(1)
            print("[Miles] ....")
            time.sleep(1)
            print("[Miles] ...BOO. I'm just playing. Plus if it was poisonous it would take a while to kill me so. >")
            enter = input()
            print("[you] How are you joking about something so serious right now? \n")
            time.sleep(2)
            print("[Miles] I didn't drop dead so might as well make the most out of a situation. I'd rather not think about how I could die out in the middle of nowhere on an island alone right now. >")
            enter = input()
            print("[you] You're right, I'm sorry. I just got worried. \n")
            time.sleep(2)
            print("[Miles] Nah I understand, that was kinda dumb. But on the bright side I'm good for no W >")
            enter = input()
            print("[you] Miles, what was that? \n")
            time.sleep(2)
            print("[Miles] .... >")
            enter = input()
            print("[you] I swear if this is another joke. \n")
            time.sleep(2)
            print("[Miles] ....AH what the heck just happened? My mouth suddenly felt heavy and numb and I can barely sp...Ea >")
            enter = input()
            print("[you] MILES, can you not speak? Are you still there? Oh no oh no I told you not to eat the fruit. \n")
            time.sleep(2)
            print("[Miles] ..I'm fiNe..I'm ok...blood >")
            enter = input()
            print("[you] Did you say blood?? \n")
            time.sleep(2)
            print("[Miles] blood..from mOUTH.. >")
            enter = input()
            print("[you] Are you okay?? \n")
            time.sleep(2)
            print("[DISCONNECTED] >")
            enter = input()
            print("Sometimes green DOESN'T mean good :/ \n")
            print("BAD ENDING: POISONED BY BERRY. \n")
            time = time.time() - start_time
            print(f"Your score = {score} \n"
                  f"Your time = {time.time() - start_time}")
            Ending.ending(score, time)
            print("1. Find player. \n"
                  "2. Display players. \n"
                  "3. End game.")
            end = int(input(">> "))
            if end == 1:
                print("Enter the player username you want to find.")
                name = input(">> ")
                Ending.find(name)
            elif end == 2:
                Ending.display()
            elif end == 3:
                print("Thank you for playing.")
    elif choice2 == 2:
        print("UNAVAILABLE. Thank you for playing up until this point. \n")
        time = time.time() - start_time
        print(f"Your score = {score} \n"
              f"Your time = {time.time() - start_time}")
        Ending.ending(score, time)
        print("1. Find player. \n"
              "2. Display players. \n"
              "3. End game.")
        end = int(input(">> "))
        if end == 1:
            print("Enter the player username you want to find.")
            name = input(">> ")
            Ending.find(name)
        elif end == 2:
            Ending.display()
        elif end == 3:
            print("Thank you for playing.")


elif choice1 == 2:
    score += good_decision
    print("[you] You should probably search for some wood to keep you warm at night. \n")
    time.sleep(2)
    print("[Miles] Yeah, being hungry sounds better than being cold. Where should I start looking? There's a forest nearby as well. >")
    enter = input()
    print("1. Search along the shore. \n"
          "2. Search in the forest. (unavailable) ")
    choice2 = int(input(">> "))
    choice2 = Validation.validationTwo(choice2)
    if choice2 == 1:
        score += good_decision
        print("[you] You should search along the shore for driftwood. It's more convenient anyways. \n")
        time.sleep(2)
        print("[Miles] Okay, give me a second. >")
        enter = input()
        print("[you] Any luck? \n")
        time.sleep(2)
        print("[Miles] Yeah, I got some. Not as much as I would like but, wait, is that my boat?? >")
        enter = input()
        print("[you] The boat that you came with? \n")
        time.sleep(2)
        print("[Miles] Yeah, it's quite a while from here. But I see it, it looks absolutely destroyed. >")
        enter = input()
        print("1. You should go check it out. \n"
              "2. You should check it out later, focus on the wood. (unavailable)")
        choice3 = int(input(">> "))
        choice3 = Validation.validationTwo(choice3)
        if choice3 == 1:
            score += good_decision
            print("[you] You should go check it out. You might find something useful there. \n")
            time.sleep(2)
            print("[Miles] Yeah, you're right. I might be mistaken because its so small but it's worth finding out. >")
            enter = input()
            print("[you] You there yet? \n")
            time.sleep(2)
            print("[Miles] Almost. If I could find my fishing rod, or clothes or a flare.. >")
            enter = input()
            print("[you] You have a flare in there?? Quick find it, you never know who might come passing by! \n")
            time.sleep(2)
            print("[Miles] Yeah I'm here. Wow, how did it get all the way over here and I, all the way over there? It's strange... >")
            enter = input()
            print("[you] I guess it's just a plot hole you're gonna have to overlook. \n")
            time.sleep(2)
            print("[Miles] That sucks. Anyways the sides completely shattered by the rocks. It's basically snapped in two, I'll see what I can salvage. >")
            enter = input()
            print("[you] Find anything? \n")
            time.sleep(2)
            print("[Miles] I found some watery packed food, wet clothes , I can probably find some use for them... is that my flare??")
            enter = input()
            print("[you] You found a flare? Is it working? \n")
            time.sleep(2)
            print("[Miles] I don't know but I put it in a tightly sealed box so I know it's not wet. There's no way of knowing unless I use it. >")
            enter = input()
            print("[you] Well just take it, you never know. Is there anything else? \n")
            time.sleep(2)
            print("[Miles] My fishing rod's in two pieces, I can't find my bag. Must've washed away in the water. Isn't it weird I had my radio on me when I woke up? >")
            enter = input()
            print("[you] I guess it's just another plot hole we're going to have to overlook. \n")
            time.sleep(2)
            print("[Miles] hmm..there doesn't seem to be anything else. I'm trying not to step on any glass but I'm getting out now. >")
            enter = input()
            print("[you] Back to finding more wood. \n")
            time.sleep(2)
            print("[Miles] Hopefully my driftwood is still down there, hey wait a minute. Am I hallucinating or is there something in the water? >")
            enter = input()
            print("[you] This is a radio, Miles. I can't see. \n")
            time.sleep(2)
            print("[Miles] There's something moving in the water, like a big object. Hang on let me take a closer look. >")
            enter = input()
            print("[you] Could it be a boat?? \n")
            time.sleep(2)
            print("[Miles] It is! It's like getting closer, oh my god! It looks super far away but it's getting closer! >")
            enter = input()
            print("[you] You have really good eyesight. Is it REALLY far away? Could you use your flare? \n")
            time.sleep(2)
            print("[Miles] It's REALLY far away but aren't flares like super loud and bright? >")
            enter = input()
            print("[you] Yeah, it should be. Even though there's no reason why you shouldn't use a flare, I'm still going to have to choose right? \n")
            time.sleep(2)
            print("[Miles] Yes because I can't seem to make any decisions of my own. >")
            enter = input()
            print("1. Use the flare. \n"
                  "2. Don't use the flare. (unavailable)")
            choice4 = int(input(">> "))
            choice4 = Validation.validationTwo(choice4)
            if choice4 == 1:
                score += good_decision
                print("[you] Quick, use the flare to alert whoever it is on that boat! \n")
                time.sleep(2)
                print("[Miles] Okay! This better work! >")
                enter = input()
                print("[you] Woah that was pretty loud. Do you think they heard it? \n")
                time.sleep(2)
                print("[Miles] I don't know...I'm trying my best to see >")
                enter = input()
                print("[you] Well? \n")
                time.sleep(2)
                print("[Miles] I think that did it! They're coming! Woohoo! >")
                enter = input()
                print("[you] That's amazing, I'm so happy for you Miles! You have some extreme luck, what are the chances? \n")
                time.sleep(2)
                print("[Miles] Well you did pick the good ending. >")
                enter = input()
                print("[you] You're right. I'm amazing at making decisions. \n")
                time.sleep(2)
                print("[Miles] I guess I'll find you when I get back home. See ya! >")
                enter = input()
                print("Well that was quick.")
                print("GOOD ENDING: RESCUED BY A CONVENIENTLY PASSING BOAT.")
                print(f"Score = {score} \n"
                      f"Time = {time.time() - start_time}")

            elif choice4 == 2:
                print("UNAVAILABLE. Thank you for playing up until this point. \n")
                time = time.time() - start_time
                print(f"Your score = {score} \n"
                      f"Your time = {time.time() - start_time}")
                Ending.ending(score, time)
                print("1. Find player. \n"
                      "2. Display players. \n"
                      "3. End game.")
                end = int(input(">> "))
                if end == 1:
                    print("Enter the player username you want to find.")
                    name = input(">> ")
                    Ending.find(name)
                elif end == 2:
                    Ending.display()
                elif end == 3:
                    print("Thank you for playing.")

        elif choice3 == 2:
            score += bad_decision
            print("UNAVAILABLE. Thank you for playing up until this point. \n")
            time = time.time() - start_time
            print(f"Your score = {score} \n"
                  f"Your time = {time.time() - start_time}")
            Ending.ending(score, time)
            print("1. Find player. \n"
                  "2. Display players. \n"
                  "3. End game.")
            end = int(input(">> "))
            if end == 1:
                print("Enter the player username you want to find.")
                name = input(">> ")
                Ending.find(name)
            elif end == 2:
                Ending.display()
            elif end == 3:
                print("Thank you for playing.")

    elif choice2 == 2:
        print("UNAVAILABLE. Thank you for playing up until this point. \n")
        time = time.time() - start_time
        print(f"Your score = {score} \n"
              f"Your time = {time.time() - start_time}")
        Ending.ending(score, time)
        print("1. Find player. \n"
              "2. Display players. \n"
              "3. End game.")
        end = int(input(">> "))
        if end == 1:
            print("Enter the player username you want to find.")
            name = input(">> ")
            Ending.find(name)
        elif end == 2:
            Ending.display()
        elif end == 3:
            print("Thank you for playing.")
