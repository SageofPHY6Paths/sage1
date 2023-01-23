---
# Mr. Green Jekyll Theme (https://github.com/MrGreensWorkshop/MrGreen-JekyllTheme)
# Copyright (c) 2022 Mr. Green's Workshop https://www.MrGreensWorkshop.com
# Licensed under MIT

layout: default
# main page (index.html)
---
{%- include multi_lng/get-pages-by-lng.liquid pages = site.posts -%}

{%- if page.img %}
  {%- if site.data.conf.others.home.header_img_with_img_tag == true -%}
    {%- capture home_img_tag -%} <img src="{{ page.img }}" /> {%- endcapture -%}
    {%- capture home_img_background_style -%} style="height: unset;" {%- endcapture -%}
  {% else %}
    {%- capture home_img_background_style -%} style="background-image:url('{{ page.img }}');" {%- endcapture -%}
  {%- endif -%}
{%- endif -%}

<div class="multipurpose-container home-heading-container">
  <div class="home-heading" {{ home_img_background_style }}>
    {{ home_img_tag }}
    <div class="home-heading-message">
      {{ site.data.owner[lng].home.top_header_line1
        | replace: site.data.conf.main.brand_replace, site.data.owner[lng].brand
        | replace: site.data.conf.main.greetings_replace, site.data.lang[lng].constants.greetings
        | replace: site.data.conf.main.welcome_replace, site.data.lang[lng].constants.welcome }}
      {%- if site.data.owner[lng].home.top_header_line2 %}
        <br>
        {{ site.data.owner[lng].home.top_header_line2
          | replace: site.data.conf.main.brand_replace, site.data.owner[lng].brand
          | replace: site.data.conf.main.greetings_replace, site.data.lang[lng].constants.greetings
          | replace: site.data.conf.main.welcome_replace, site.data.lang[lng].constants.welcome }}
      {% endif -%}
    </div>
  </div>
  <div class="home-intro-text markdown-style">
    {{ content }}
  </div>
</div>

{%- if lng_pages.size > 0 and site.data.conf.others.home.new_posts %}
<div class="multipurpose-container new-posts-container">
  <h1>{{ site.data.lang[lng].home.new_posts_title }}</h1>
  <ul class="new-posts">
  {%- for _post in lng_pages limit: site.data.conf.others.home.new_posts_count_limit -%}
    <li>
      {%- assign page_title = _post.title -%}
      {%- include util/auto-content-post-title-rename.liquid title = page_title -%}
      {%- include multi_lng/get-localized-long-date-format.liquid date = _post.date -%}
      <a href="{{ site.baseurl }}{{ _post.url }}">{{ page_title }}
        <span>{{ _post.date | date: out_date_format }}</span>
      </a>
    </li>
  {% endfor -%}
    <li>
      {%- include multi_lng/get-page-by-layout.liquid layout = 'archives' -%}
      <a href="{{ site.baseurl }}{{ layout_page_obj.url }}">{{ site.data.lang[lng].home.new_posts_show_more_button }}</a>
    </li>
  </ul>
</div>
{% endif -%}

- [Physics](#physics)
- [Atheism](#atheism)
- [Veganism](#veganism)
- [Others](#others)

### Physics

>“Fundamental physics is like the top of the physics mountain. Just because you reached the top doesn't mean you already reached every other point on the mountain. But people are more excited about reaching the top than reaching any point in the middle.”

>“Our universe gave up its love for compact Lie groups because it wanted some dynamics, without which the universe would be boring. If the spacetime symmetry was SO(4) instead of SO(3,1) there will be no time.”

>“Humanity matured only recently. **Unfortunately** by maturing they understood how insignificant they are in this universe.”

>“Philosophy has the best questions humanity can come up with, but unfortunately those questions can never be answered concretely. Whereas in **science** we have questions which are nearly as interesting as in philosophy but these can be concretely answered.”

>“The only deference between physicists like Newton and monks is that the former renounce worldly pursuits to devote themselves fully to understand the world deeper but the later devote oneself fully to believe in lies told by their ancestors.”

>“I think the fundamental laws of physics exist both in the abstract mathematical realm (like numbers, sets, functions etc.) and physical realm (like spacetime, particles etc.). So, the fundamental laws of physics are the only equations that exist in physical reality.”

>“The universe is not human centric. It's mathematics centric. If something governs the entire universe it's a mathematical expression rather than some god who thinks exactly like humans.”

>“Contemplating about the size of the universe is one of the simplest medicine for arrogance.”

>“When there is more symmetry there will be more beauty. Humans only have an approximate parity symmetry (like our heart will go to right in the mirror). But the laws of physics are much more symmetrical and therefore beautiful. The laws of physics have Lorentz covariance. It is a very large symmetry group. <a href="https://en.wikipedia.org/wiki/Noether%27s_theorem" target="_blank">Noether's theorem</a> says that because of Lorentz covariance we have 4 momemtum conservation, angular momentum conservation and Conservation of CoM (center-of-momentum) velocity. Even the most beautiful human beings are ugly in front of the laws of physics.”

>“The laws of physics are peak beauty in real life. There are somethings in mathematics which are even more beautiful but that is not physical beauty.”

>“Most depressing things about reality:<br>
1) Scepticism<br>
2) Universe and laws of physics are independent of good and bad and the unimaginable suffering that is happening in the universe<br>
3) Animal suffering<br>
4) Human suffering<br>
5) Death and human lifespan<br>
6) Unobservable universe<br>
7) Human reproduction procedure<br>
8) Fragility of human body in front of cosmic forces<br>
9) Inefficient energy acquiring by humans. Instead of digestion, Penrose process should be there.<br>
10) Economic inequality and the trade-off between efficiency and equality.”

>“When you achieve permanent post-nut clarity you will probably study theoretical physics or mathematics or go on a journey reduce suffering in the world.”

>“Theology is not only inferior to physics when it comes to understanding the origin of the universe, it is not even a valid approach. Physicists haven't understood this problem completely. But they are doing constant progress. Of course religious people will say that we don't need to work hard to understand this problem and the answer is there in their book. Though physicists haven't reached a conclusion on this problem, they know enough to say that the religious answer is stupid. Unlike physics religion is not doing any progress. It started at the 0 level and became stagnant. Physics is already so far above religion that religion will should not even be compared to religion and this is not even the limit to physics. Physics will continue to increase its level. There is another approach other than physics for this problem, philosophy. But their progress is negligible (on this particular problem, they are doing great in the fields of ethics etc) in front of physics' progress.”

### Atheism

>“I hate all religions but I love all religious people just like I hate all diseases but I love all people with diseases. I always wish good things to the religious people just like I wish good things to people with diseases. But unfortunately these religions are so powerful diseases that people who suffer from them can't even comprehend what I just said and they think that I hate them and they in turn hate me.”

>“Religion for all it's arrogance, has produced nothing even be remotely comparable to things that science has produced.”

>“I think the probability that God exists is close to 0 (like 10^-5), if your definition of God contains consciousness. If your definition is one of the specific god of major religions then it's exactly 0 (for they are inconsistent nonsense). If your definition is as simple as god=reality or laws of physics (like in pantheism), then I can guarantee that it exists (probability=1). But I thing we should not use the word "god" for impersonal philosophical ideas.”

>“Religious people who are against blasphemy are hypocrites. They think that their religions can mock us atheists, but also think that atheists mustn't mock their religions.” (<a href="https://en.wikipedia.org/wiki/Hinduism" target="_blank">ॐ</a>: <a href="https://www.sacred-texts.com/hin/rigveda/rv07006.htm" target="_blank">Rig Veda 7.6.3</a>, <a href="https://vedabase.io/en/library/bg/7/15/" target="_blank">Bhagavad Gita 7.15</a>, <a href="https://vedabase.io/en/library/bg/7/25/" target="_blank">Bhagavad Gita 7.25</a>, <a href="https://vedabase.io/en/library/bg/9/12/" target="_blank">Bhagavad Gita 9.12</a>; <a href="https://en.wikipedia.org/wiki/Christianity" target="_blank">✝</a>: <a href="https://biblehub.com/psalms/14-1.htm" target="_blank">Psalm 14:1</a>, <a href="https://biblehub.com/romans/1-21.htm" target="_blank">Romans 1:21</a>, <a href="https://www.skepticsannotatedbible.com/int/long.html" target="_blank">check more</a>; <a href="https://en.wikipedia.org/wiki/Islam" target="_blank">☪</a>: <a href="https://quran.com/en/2/13" target="_blank">Al-Baqara 13</a>, <a href="https://quran.com/8/55" target="_blank">Al-Anfal 55</a>, <a href="https://www.skepticsannotatedbible.com/quran/int/long.html" target="_blank">check more</a>)

>“Let us put aside the question whether the Hindu gods and Abrahamic god exist and assume, for the sake of argument, that they exist. Even then I would not give them any respect, I would rather respect great people like Einstein, Hilbert, Russell than them. They are fictional characters made up by primitive people whose imagination is so limited that **the greatest possible beings in their imagination** are **arrogant, foolish, irresponsible and evil**.”

>“The god of the Abrahamic ~~faith~~ fiction doesn't want people to be good, **he only wants people to be stupid**. If you blindly believe that he exists without any logical reason then you will be sent to heaven, but if you do the logical thing by not believing him until the judgement day when he appears then he will send you to hell even if you believe him when you see him. So he has hatred for intelligent people. It does make sense that such a foolish and arrogant God will be angry at intelligent people for he couldn't even find a decent method of sending information (which he thought was important but actually isn't) to people. We mere non omniscient beings can simply think of many highly efficient ways (better than sending messengers who won't even make sure their scripture is written before they die) this information can be sent to the people without even using any magic just by using science. Luckily it is all just fiction and that god doesn't exist, otherwise the universe would have been even more meaningless than it already is.”

>“As a child I used to think that criticising religions is immoral. If a scientific theory which has large amount of evidence can be criticised, why shouldn't we criticise religions (which are dogmatic and have no evidence) ? I think we explain the fact that many religions like the <a href="https://en.wikipedia.org/wiki/Abrahamic_religions" target="_blank">Abrahamic religions</a> have punishments for apostacy using the evolution of religions somewhat similar to the evolution by <a href="https://en.wikipedia.org/wiki/Natural_selection" target="_blank">natural selection</a>. In the beginning some religions will have strict apostacy laws and some won't have. Over time people will leave and criticise the religions without any apostacy laws. Understanding their reasons even more people will leave until those religions finally go extinct and only religions with apostacy laws will survive. I wonder how Hinduism and Buddhism survived this long without apostacy laws. Some great people like Socrates, Giordano Bruno etc were killed because of these blasphemy laws and some others like Galileo Galilei were punished.”

>“Newton had logically valid excuses for not being an atheist. He thought animals were too complex to be formed naturally. Later Charles Darwin introduced evolution by natural selection. But later Lord Kelvin argued that the Sun had to be between 20 and 100 million years old, based on the assumption that the Sun's energy source was gravitational contraction. This time was too short for evolution to occur. The discovery in 1903 that radioactive decay releases heat led to Kelvin's estimate being challenged, and Ernest Rutherford famously made the argument in a 1904 lecture attended by Kelvin that this provided the unknown energy source Kelvin had suggested, but the estimate was not overturned until the development in 1907 of radiometric dating of rocks. It was only when thermonuclear fusion was recognised in the 1930s that Thomson's age paradox was truly resolved. But after that there are no more excuses to believe in religions.”

>“Before the Copernican Revolution humans were literally thinking that they are the centre of the universe. This anthropocentrism is still very much present in humanity. Of course it is decreasing as time goes on, in Hindusim and other religions that came before like Ancient Egyptian religion the gods were very much like humans. Even in the early polytheistic Judaism, Yahweh was just a national god. Only later did the creators of the Abrahamic ~~faith~~ fiction realise that expecting God to look like a human might be too much humanocentrism and changed him to be a bodyless individual. But they still haven't changed the way their god thinks. He thinks very much like the human looking gods that were created before. To be even more clear the religions mentioned previously are not even anthropocentric, they were ethnocentric, they thought that their ethnic group was the centre of the universe not even humanity. Today we know how insignificant humanity (let alone their ethnic group) is from a cosmic perspective. Some people like Einstein who understood this believed that, God can only be something like the equations of physics, something that is completely beyond humans and he called it a **cosmic religion**. Even though ideologically I agree with Einstein I think we should not use the words God (since for 1000s of years it used to describe evil, arrogant, foolish imaginary beings) or religion (since for 1000s of years it was used to describe dogmatic belief about the conditions of afterlife) just to distance us from their popular meanings.”

>“Belief in a single religion is already very stupid, but believing that all religions are true is peak stupidity. Even as a child I was shocked to see the <a href="https://en.wikipedia.org/wiki/Brahma_Kumaris" target="_blank">Brahma Kumaris</a> believing all religions are true.”

>“If an intelligent person wants to believe in a religion, he has to distort it ("mental gymnastics") to the extent that it no longer looks like a religion.”

>“Many humans like the mysterious nature of religions. Curiosity about mysterious things is great to have. But most humans cannot understand real mysterious things like quantum physics, general relativity, black holes etc. So they cope with this by believing in obviously false fiction that is called religion. The mysteries of religion are not just false compared to the mysteries of science they are inferior even if both were true. Humans should stop funding their religions and should start funding science which is doing the real work of finding these mysterious things instead of making up lies like religions do. As as a side product of finding these mysterious truths, science has also done much good to humanity like vaccines, transportation, mobile phones, internet etc.

>“The wiser you are the less religious you will be. The converse is false.”

>“Religion is the best example to show that the Aristotelian view of man as a rational animal is wrong. Mankind evolved to survive, reproduce, and pass more of their genes on to the next generation, not to understand the nature of reality. Those of us who are **liberated from the chains of evolution** and are striving to understand the universe are an exception not a typical man.”

>“Religion is for the fools by the fools.”

>“Saying that if you are not religious then you are immoral is same as if you are not a butcher then you are not animal rights activist. Only fools can utter such nonsensical statements.”

>“Your children are not born to be brainwashed by you into your religion. They have the right to be not brainwashed.”

>“Religions are a mixture of pseudoscience and pseudophilosophy.”

>“As long as majority humans believe in religions, I would be ashamed to be a human.”

>“I (and many others) can make many religions which can be overall considered good (I mean the evilness caused by lying is negligible if that religion gives superior morality, health tips etc to humanity). But unfortunately in all the religions made by humans who lived centuries ago the good part is negligible compared to the evil they cause.”

>“In the 21st century a scientist who calls himself religious is in confusion. He can either be religious or scientist not both.”

>“If string theory is true then there is no need for a personal God since it can explain everything. If string theory is false even then there is no personal god because such being (if existed) would definitely not select a theory that is less beautiful than string theory as the ultimate theory.”

>“Although both <a href="https://en.wikipedia.org/wiki/Abrahamic_religions" target="_blank">Abrahamic religions</a> (<a href="https://en.wikipedia.org/wiki/Judaism" target="_blank">✡</a>,<a href="https://en.wikipedia.org/wiki/Christianity" target="_blank">✝</a> & <a href="https://en.wikipedia.org/wiki/Islam" target="_blank">☪</a>) and <a href="https://en.wikipedia.org/wiki/Indian_religions" target="_blank">Indian religions</a> (<a href="https://en.wikipedia.org/wiki/Hinduism" target="_blank">ॐ</a>,<a href="https://en.wikipedia.org/wiki/Jainism" target="_blank">ꣽ</a>,<a href="https://en.wikipedia.org/wiki/Buddhism" target="_blank">☸︎</a> & <a href="https://en.wikipedia.org/wiki/Sikhism" target="_blank">☬</a>) are inherently evil, we should note that the Abrahamic religious are more evil than the Indian religions. But Indian religions have more pseudo-scientific nonsense that the Abrahamic religions.”

>“The difference between (<a href="https://en.wikipedia.org/wiki/Hinduism" target="_blank">ॐ</a>, <a href="https://en.wikipedia.org/wiki/Judaism" target="_blank">✡</a>,<a href="https://en.wikipedia.org/wiki/Christianity" target="_blank">✝</a> & <a href="https://en.wikipedia.org/wiki/Islam" target="_blank">☪</a>) and (<a href="https://en.wikipedia.org/wiki/Jainism" target="_blank">ꣽ</a>,<a href="https://en.wikipedia.org/wiki/Buddhism" target="_blank">☸︎</a>) is that the former are created by **horny fools** who knew nothing about the universe whereas the later are created by **kind fools** (<a href="https://en.wikipedia.org/wiki/The_Buddha#Historical_person" target="_blank">Gautama</a>, <a href="https://en.wikipedia.org/wiki/Parshvanatha#Historicity" target="_blank">Parshvanatha</a>, <a href="https://en.wikipedia.org/wiki/Mahavira#Historical_Mahavira" target="_blank">Mahavira</a>) who knew nothing about the universe. The latter people were fools because science and philosophy was not advanced enough in their times for them not to be fools, but the former people would have been fools even today.”

>“The Kalam cosmological argument is a bad argument. Causality needs the laws of physics. Even if laws of physics exist, some types of laws of physics don't allow causality. If closed timelike curves exist, (classical gravity allows them but whether quantum gravity does or doesn't is not yet known) that proves that causality is not present.
>
>Most likely answer: I think the cause should always be in the past light cone of an event and for a first moment of time there is no past light cone and as such it doesn't need a cause and it is meaningless to talk about it's cause.
>
>Some other less likely (but still much more probable than those silly religions claiming the cause is a person/persons) answers:
>
>1) Even neglecting it's speciality of being the first moment of time, it could be causeless like random quantum fluctuations.
>
>2) Laws of physics don't respect causality at the Planck scale (at the beginning of the universe and at the centre of black holes).
>
>3) It is also possible that retrocauality in the early universe can explain how the universe began.”

>“Religion is the most unproductive thing humanity has ever invented. Science is the most productive thing humanity has ever discovered (of course it is not a mere human invention).”

>“Caste system is like a branch of a tree. If you cut the branch it will again grow. You need to the remove the entire roots of the tree and these roots are nothing but Hinduism.”

>“Abrahamic religions are global nonsense (it is the same in all places like global symmetries). Hinduism is a gauge nonsense (it depends on position [like your town/village] similar to gauge symmetries as different villages have different beliefs and rituals).”

>“Some people think that religious books should be given respect by everyone. There are many examples where people were killed just because they burned some religious book. I think atheists shouldn't do such things, instead they should peacefully approach and explain the religious people why their religion is false using logic. If you do such things the religious will hate atheists and from then on they will never even try to listen to the logical arguments for atheism. This is a huge loss to the atheist movement. That being said, even simple punishments for such blasphemy like slapping once will be wrong, let alone murdering or arresting people. Many science textbooks like General Relativity by Robert Wald, The Quantum Theory of Fields by Weinberg, String Theory by Polchinski etc are **infinitely** superior to these religious books and I still believe that it is not immoral to disrespect these science books by burning or any other thing.”

>“The fact that there are still people believing in religion, pseudoscience, astrology etc is a disgrace to our species.”

>“Caste system is like a branch of Hinduism. If you cut down the branch it will again grow. To eradicate caste system the only way is to remove Hinduism.”

>“In debates with atheists, Christians at least use logic even if said logic is improper. Unfortunately, Hindu's don't even use logic.”

### Veganism

>“If humane slaughter is not an oxymoron, like humane slavery, then humane is no longer a positive ethical attribute.”

>“The existence of animal agriculture is depressing and disgusting. We have the necessary technology to live without the barbarically cruel animal agriculture. In fact abolishing animal agriculture is better for our health, the environment, and biodiversity. In spite of everything I still believe that people are not evil at heart. Most people do evil things without realizing how abhorrent the things they do are. Cognitive dissonance is the main cause of this. Germans back in the day didn't realize that holocaust was evil. They knew killing people unnecessarily was wrong. But they also believed holocaust was necessary (the Final Solution to the Jewish Question). This is cognitive dissonance.”

>“Any normal human (that is someone who doesn't have serious diseases like Smith-Lemli-Opitz syndrome) who is not a vegan is immoral. Let us hope that in the future, such people will not be the majority.”

>“The biggest sins done by an average human being in recent times are 1) consuming meat and dairy products, 2) brainwashing children in the name of religion, 3) inequality among people based on stupid arbitrary parameters like caste, race, nation, language, gender, wealth etc.”

>“I believed that humans are steadily improving their ethical standards until I learned about factory farming. Judging by aggregate suffering we as a species have reached new lows in terms of ethics. Factory farming is less than a century old. When humans started to understand after world war II that other people also have some moral worth and should not be exploited, they did good things like decolonisation etc, but their innate cruel nature could not be suppressed and they increased the exploitation of animals exponentially. And they also successfully brain washed themselves to think that this is not at all evil.”

>“Each day the majority of humans live as non vegans humanity strays farther from the path of cosmic salvation. If a highly intelligent species comes and sees what we are doing to the voiceless animals then they will definitely think that we are **pathetic barbarians** just like how we think about humans who lived more than a century ago who did not think slavery and colonisation are evil. At least nowadays the tiny fraction of people who understood carnism is evil are talking against it. During slavery and colonisation the tiny fraction of people who understood that it was evil never stopped others from doing it. Only after the people who were oppressed started violent fights for their freedom they stopped exploiting them. Unfortunately animals can't start violent fights for their freedom.”

>“To be a wise man, you need to be both a vegan and an atheist.”

>“Philosophically scepticism is even more deeply depressing than animal agriculture. I have hope that through hard work we can abolish animal agriculture. Mere human activists can achieve this in few centuries. But defeating scepticism is beyond human capabilities. Even an omnipotent being will be incapable of doing anything in front of Gödel's second incompleteness theorem.”

### Others

>“Lust has successfully blinded humans so that they never realize how ugly sex is. We should not be "subject to the common frailties of mankind" and follow the example of Newton to minimize these animalistic desires that are present in humans.”

>“If humans had only one gender, like the <a href="https://dragonball.fandom.com/wiki/Namekian" target="_blank">Namekians</a> in the Dragon Ball franchise, humans would have by now become a galactic civilisation.”

― Sage of PHY6 Paths
