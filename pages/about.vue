<template>
  <v-container class="mt-12">
    <v-layout class="mt-12" fill-height column justify-center align-center>
      <v-card flat color="transparent">
        <v-card-title class="display-2 font-weight">About</v-card-title>
        <v-card-text class="subtitle-1 font-weight">{{blurb}}</v-card-text>
        <v-card-text class="subtitle-1 font-weight">{{p1}}</v-card-text>
        <v-card-text class="subtitle-1 font-weight">{{p2}}</v-card-text>
        <v-card-text class="subtitle-1 font-weight">{{p3}}</v-card-text>
        <v-card-text class="subtitle-1 font-weight">{{p4}}</v-card-text>
        <v-card-text class="subtitle-1 font-weight">{{p5}}</v-card-text>
        <v-card-text class="subtitle-1 font-weight">{{p6}}</v-card-text>
        <v-card-text class="subtitle-1 font-weight">{{p7}}</v-card-text>
        <v-card-actions>
          <v-btn tile outlined color="primary" class="ma-1" nuxt to="/">return</v-btn>
        </v-card-actions>
      </v-card>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      blurb: `My grandpa actually named me 'Lin' (pronounced l-unh') 20 some years ago when I was born. I asked him about what it meant a few years ago. He said I was named after the "Qilin", a Chinese mythological chimera with the head of a dragon, the antlers of a deer, the hooves of a horse, and a scaled body. The 'Qi' and 'Lin' is a marriage of 'male' and 'female', respectively. The appearance of a Qilin usually signified the birth or death of a benevolent ruler.`,
      p1: `People often ask me how I came to live in Leo, Indiana. I always give them the short answer, but there is much more that I have always wanted to say. My grandfather would send my uncles across the ocean to escape a post-war, communist Vietnam. Several attempts at the journey were made, but often times it would end with them jumping ship and running back home to a disappointed father or several weeks in a prison cell. Who could blame them? How could you ask that of a 12 year old boy? Eventually, one of my uncles was able to make the voyage. Because of him, my parents were able to immigrate to a small town in Fort Wayne, Indiana. My father, and the majority of my family, stepped on American soil with less than $400 USD and the clothes on their backs. They spoke no English. Here, I was born alongside my brother and five cousins. `,
      p2: `While we always had food on the table, many sacrifices had to be made. My mother worked a minimum wage job at a dry cleaning service. My father worked for $2 a day at a Chinese buffet, washing dishes and only able to say: "are you done" and "thank you". Today, my mother owns her own nail salon. My father owns his own restaurant after working his way to become a regional manager at Panda Express. Although they were able to prosper, the chemical damage to my mother's hands are irreversible. My father is diabetic and his body is destroyed from the rigor of restaurant work and 80 hour work weeks driving around the midwest. He told me stories of how he would bite his own hand while driving just to stay awake when he was called out to failing stores.`,
      p3: `As the first-born son of the family, I shouldered much of the burden when my parents could not. My parents often bought me computers to play with when they could not spare time from work. I attended a public school, graduated with honors and a 3.9 GPA, and was accepted to major in Computer Science at Purdue University. For a very long time, I knew little about the world when I was occupied with attending school in a small town and immigrant parents who knew nothing of how to prepare a child for college. We had no roots in this foreign land and no clear direction, only a duty to provide for the family.`,
      p4: `Today, I am an upperclassman in Computer Science with the honor of Dean's List and an internship at a Fortune 500 company. My cousin James is also attending Purdue University for Computer Science with an internship at Procter & Gamble as a freshman. My oldest cousin, Judy, has completed her pre-pharmacy degree and is a year into her pharmacy program. This year, my brother has just been accepted into Purdue University with a full-ride scholarship and my cousin Michael accepted a full-ride at Indiana University. My cousin Tracy is graduating with a dual degree in Business and Economics from UC Irvine.`,
      p5: `Much of my family struggled with depression, anxiety, and even continue to battle imposter syndrome today. Coming home to an empty house, cooking dinner, and doing AP Calculus homework was a normal day. For many star students in college, especially one like Purdue University, AP Calculus was a trivial task. But for us, it was a great challenge. None of us had any clear direction or advice in preparing for higher education. We simply applied ourselves in the best way we knew how and we all hold a special kind of pride in our achievements.`,
      p6: `Personally, I had struggled with the Asian values of my family and the American ideals of my peers. I still struggle with it today, but I also began to embrace both sides. The struggle that my family has gone through has given me the strength to confront many of the challenges that I face. For that, I am eternally grateful. Just like my namesake, I am someone who is of multiple, diverse parts. I like to think that it makes me that much stronger.`,
      p7: `I hope this was resonating for anyone with a similar experience. Remember to take care of yourself, the old world Asian mindset isn't one that is always openly supportive. Feel free to contact me even if you just want someone to relate with.`
    };
  }
};
</script>
