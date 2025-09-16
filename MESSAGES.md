---
layout: default
title: Messages
---

<h2 style="font-size: 42px; color: #00B03B; margin-bottom: 10px;">Choose a Number, Hubby 💚</h2>
<p style="font-style: italic; color: #32874E;">“This is for you, my love so sweet! 41 simple messages! Click on any number then scroll down. Do this every 2 months starting this September. So it'll September, December, May, and June!!”</p>

<div class="grid" id="button-grid"></div>
<div id="message-box"></div>

<style>
  .grid {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 12px;
    max-width: 900px;
    margin: auto;
  }

  .number-button {
    font-size: 28px;
    margin: 10px;
    padding: 20px 0;
    width: 100px;
    border: none;
    border-radius: 12px;
    cursor: pointer;
    color: white;
    transition: transform 0.2s;
    text-align: center;
  }

  .number-button:hover {
    transform: scale(1.08);
    box-shadow: 0 0 10px #00B03B;
  }

  #message-box {
    margin-top: 30px;
    font-size: 28px;
    font-style: italic;
    font-weight: 500;
    color: #98D7A5;
    min-height: 60px;
    padding: 20px;
    line-height: 1.6;
    opacity: 1;
    transition: opacity 0.3s ease;
  }
</style>

<script>
  const messages = {
    1: "Hi hubby! This is number 1. Have you been choosing the numbers in a chronological order or just randomly? I want you to listen to So High School. Imagine me singing it with my guitar. Maybe put your favorite lyrics on your post next time? Waaa binaon ka metten. I love you MWAH!",
    2: "I know this is random but you picked number 2 and that's the number of kids I want, hubby! So, I'll ask you to just randomly send me a number in my email, my my tiktok, my messenger or anywhere hubby. Don't give me context, put a number then send. It better not be more than 2 grrrrrr.",
    3: "Aaaa 3!! Hmm for the remaining time of the day, I want you to rest. But before you do, read the 76th chapter of your written story about us. Tell me about it? You never gave it to me hubby waaa but you know I'm psychic so I know it already. 😏",
    4: "How are you there? How's the Weather, hubby? I bet it's dry season cause I'm psychic and it's winter here when you picked this. Let me know if I'm right!! hehe. Ingat ka love ko, take care of yourself from the heat or from the rain. Mostly heat cause it's dry season and I'm psychic MHWAHHAWHAHAH.",
    5: "Hubby, hubby! This is your reminder to process your passport by the time you're 18. It will expire after ten years and I bet you'll already be with me before that happens. Better do it during vacation so you won't have much hassle and worries from school, yes? Once it's processed, set it aside!! I'm really excited to see you, hubby.",
    6: "I wrote this one just so you can remind your mermaid husband to go to the beach. Tell him to carve your names on a shell and let the ocean witness it. That way, your love for each other will be deeper than the depths of it. Maybe you want to do that as well my gorgeous pearl. I love you!",
    7: "Hubbyy since you picked 7, I bet it's a full moon. Stare at the moon tonight if it's visible where you are. Talk to it like you're talking to me. I'm on the other side of the world howling at it, my vampire. Close your eyes and say your wish hubby. Maybe our reunion? The moon listens to a longing, lonely heart, she always does.",
    8: "If you picked this number, it's telling me that you should cook yourself some noodles. DON'T put all the seasonings though! Be careful of your health my love.",
    9: "Hi hubby!! Do you still want to pursue dentistry or are you already on the pursuit of it? Maybe you're already a dentist while reading this! Which ever it is, I'm so proud of you! I'm always proud of my hubby. This is your Mr. Laciste speaking and giving you a kiss. MWAH",
    10: "'Letters side by side. An unchanged fate or a sign? Both! And time has tried.' Hubby, I wrote this simple haiku at a random 7pm where you said you'll eat and you'll make it quick hehe. Aaaa you're taking a bit long, my love. This haiku is about us, how Y and Z are beside on another and time may test what we have, but we won't give up, right? MWAH",
    11: " And as an honor to eleven, this is January 1, 2025 or 1/1/2025. My journal says 'the highlight for today is hubby Thirst trapping.' I told you this one time, and I quote the ending of my entry for that day; 'More memories to come Z'. It was the greatest way to start a year! I was so in love and I just wanted to love you everyday.",
    12: "Just here to remind you to wear the ring I gave you while your lucky charm (me) is not yet with you. Bring your ring everywhere, bring your hubby everywhere you go please. Like I always say, keep me close to you. Beside you and beside your heart.",
    13: "Technically I did the first pet question but put it in a higher number but depends which one you come across. Here's another pet question, my love and since it's Taylor Swift's favorite number, I have a cat question! Sooo me want 1 cat only na, yeaa. Now, I want you to decide if you want an orange tabby cat or we'll just trust the CDS 'cat distribution system' to give us any?",
    14: "Do you still have the rocks you collected the first time we went out together? Remember running away from the geese? You're so cute hehe. The photo I took of you is still my phones wallpaper, hubby. I'll never remove it. Duray pay maperdi detoy cellphone kon nga crack crack pay ketdin. Duray sabali to nga phone'n, isu latta ti wallpaper ko kasi it was our first time going out together. Us, only us together. I love you!!",
    15: "Your witchy and psychic hubby knows you're reading this right know and he wants to give you a kiss. Here's my mwah mwah https://drive.google.com/file/d/11obl6uTBY9WhmMp9bPf91k2-9yO0jkHE/view?usp=drivesdk.",
    16: "Hey! Eiram on the keyboard. Let me remind you to fix your mess up! No procrastinating alrighty? Get things done! Nyenyenye blehhh... Uhm, I love you hubby waaaa no no bipolar.",
    17: "Arf arf, hubby you want want golden retriever latta or there's another breed you want na? Tell me tell me cause me agree to whatever you want! Basta we'll have a cute cute doggie.",
    18: "Ahh, eighteen. The age I turn to the year I'm writing and making this. Hubby, do something special for me once you chose this. I want you to go outside and take the prettiest flower you can find that will look best if it's in my ear. Haan lang nga picture mo makitak ah!! You're my pretty flower—the prettiest in my eyessss! MWAH MWAH MWAH",
    19: "My birthday number! Hubby, you're always in my affirmations, manifestations, and my gratitudes to the universe. You are so special that you're the only thing I ask for during the celebration of my birth. I'm really grateful to have you, Zy!",
    20: "Hubby, I know you don't love Filipino shows, movies, songs, and whatnot but watch Miss Granny starred by Sarah Geronimo. I promise you, it's a great movie! Let's rewatch it together soon! Make it a movie night as well! A time for you to rest. I love you!",
    21: "We're almost together hubby. The day we'll be with each other is near. I'd like to know what'd be the first thing you say or do the second you see me so I can keep my hopes up for that day. Tell me please, I want to know.",
    22: "Do you ever believe in magic? If you ask me, I'd say yes. I've always believed in magic as a child. I think magic is an imagination that can manifest in this lifetime as long as it is nurtured with belief, reality, and your heart. 'Got to believe in magic' by David Pomeranz strengthened that perspective of mine. Have a listen hubby, not to make you believe in magic lol but just to have some faith in the universe because the universe led us to each other. That's such a magical thing.",
    23: "This'll just be a short message hubby. Write your favorite moment with me on your journal or your phone's notes. I always ask you to never forget me and through this, hopefully you won't forget my love for you. I love you so much, Zy!",
    24: "Have you read the first one I wrote about the moon, my vampire? If not, then now you know! Let me guess, it's a crescent moon right now hmm? Waaa I don't care. Whatever the phase the moon is, I howl you name to it every night. I'd love you for a thousand years, hubby. I won't get tired wishing at the moon for the day we'll say our vows.",
    25: "Idk about you but I think you should definitely rewatch Chick Girls again. Go laugh out loud! Be with your family or your friends or whoever you feel comfortable with—maybe alone? Laughter is the best medicine eh? Watch well, hubby!!",
    26: "By the moment you're reading this, I want you to know that I talk about you to lots of people. To my new friends, my coworkers, my classmates, my professors, and of course, the family members I trust. I wish you do the same, hubby. I love you so much. Know who to trust, yes? You must choose the right people to surround yourself with. Take care of yourself. Mwah",
    27: "Bonjour mon amour. Ton hubby t'aime! Put anything french in your notes if you see this. I already stopped learning because uhm yeaaa boring.. I don't even like french fries and that's not even french btw. The only good thing they've created was Miraculous ladybug and even that has turned bad after the first 3 seasons. BUT OH I love croissants of course. mwah mwah croissant!",
    28: "This one's your birth day number! How old are you na hubby? Has it been months, years or a decade when you chode this number? No matter the day, it's never too late to say that I love you and I still and will always do. I won't convince myself anymore that there's gonna be another life to have you. I won't convince myself that they'll be a story of another us because even in this lifetime, you'll have me.",
    29: "",
    30: "Hmmm.. Hubby ko! I want you to describe how we'll spend our first day together here in Canada. Be very very specific. Do your research about our place! I want to hear your whole plan and I'll make it happen 100%. Put it on email and send it once you find the time to do so. it's yajlaciste@gmail.com hubby loves",
    31: "This number is instructing you to tell your hubby to bakes some cookies. It's your hubby's first time baking and ALONE but it would definitely remind him of his sweet Zy. Give him a call as well if you can! I hope you can.. I'm sure you can so do it!",
    32: "Do you still have our photo booth photos? It's alright if not hubby but I hope you do just in case I lose mine. Keep it safe and soon, we'll hang those in our refrigerator that'll be filled with magnets of our adventures in the world.",
    33: "Hubby, I've always felt we weren't so close. Clearly cause it seems we hid secrets from each other. Can we please change that? You're my family and I want you to know everything about me. Promise me that once we're together, we'll be close than the sun is to mercury or how the moon is to the earth, yeaaa? Hehe mwah",
    34: "Are you excited hubby? You cooking dinner and me helping but actually bothering you. Then me wash wash dishes while you hug me from behind. I'm already picturing all these cute and fun things we'll do in our home. Patience is a virtue which I'm sure is!! I'll learn how to be patient for you hubby.",
    35: "This number just looks hmm uneasy to me so if you chose this, I want you to take a moment to clear your mind hubby. Put a 10 minute timer on your phone and just close your eyes. You can be in bed, you can be sitting, standing, basta anywhere SAFE!! Just close your eyes the whole time and when the timer runs out, jot down in a paper everything that came through. Do you feel better hubby? I want to know. I don't need any details of what's bothering you if you don't want to share. Only how you felt after wtiting.",
    36: "Hey hubby, I hope that you won't get tired of opening one number every 2 months and I also hope that you appreciate me for creating this for you. I'm trying so hard to finish this just before my flight to Canada and that's in 3 hours na. I really don't want you to forget me that's why I created this. Don't get tired please and don't open in advance! Open only on March, June, September and December, yes? HEHEHE I'LL TRUST YOU ON THAT",
    37: "Aaa I think there's too many of these which I made about moon. This time, try to name a constellation hubby. Hopefully you read this at June because if you did, try to look for my zodiac Scorpius at 8pm. It's pretty easy to spot, hubby. Once you spot it, you can look for yours! Libra is right beside it. That's just like us. From alphabet to constellations. OH YOU AND ME ARE DESTINED WAAA. edi wow hehehe MWAH ZY",
    38: "I know this may sound psychotic but this number just screams 11 to me because 3+8 is 11 uhmmm.. Anyways, you know a good song that has 11 in the title? Not just one, but two! It's 'Eleven eleven' by Conan Gray. This song reminds me so much of you hubby and yes, I wish for you at eleven eleven like you do too.",
    39: "Not that I'm so politically aware but I'm sure this number is picked after elections already. So, I'm curious hubby are there new leaders already in the Philippines? How are they? Who's the president? How about the senators? I want you to be politically aware for our country.",
    40: "Send me a message please. I put this in such a far number because I don't want to sound desperate for you but I am. I never told you this but hubby, it hurts me that it seems like you won't even miss me at all the last time I saw you. I know you were sick but you didn't even bother to give me a hug. Siak pay ti immay nga immarakop kanyam. For 5 weeks before that day, it seems like you were doing good, sooo good without me and I was happy for you but I was jealous cause I couldn't do the same. So please hubby, send me a message. Ask me how I am because it hurts feeling like you don't care for me.",
    41: "And for the last number, I want to look back during the time I blasted these songs every night because I see you everyday in school. Both by Gracie Abrams btw. First is 'Close to You'. And then it shifted to 'Risk' the second Hugo told me that you like me kasi isu inbaga ni classmate mo and that gave me the courage to send you a message. How I miss those day, Zy. I can't turn back time but listening to those songs makes me tear and remember those days. Oh and that's why 'Risk' was the first full song I tried to learn in the guitar. The video on my story was just a practice btw waaa I swear I'm better now!! I love you so much my Zyann."
  };

  const grid = document.getElementById("button-grid");

  for (let i = 1; i <= 41; i++) {
    const button = document.createElement("button");
    button.innerText = i;
    button.className = "number-button";
    button.style.backgroundColor = `hsl(140, 50%, ${30 + i}%`;
    button.onclick = () => {
      const box = document.getElementById("message-box");
      box.style.opacity = 0;
      setTimeout(() => {
        box.innerText = messages[i] || "No message yet.";
        box.style.opacity = 1;
      }, 150);
    };
    grid.appendChild(button);
  }
</script>
