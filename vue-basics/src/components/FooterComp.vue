<template>
  <div id="postsContainer">
    <div v-for="post in posts" :key="post.id">
      <h2> {{ post.title }} </h2>
      <h4> {{ post.description }} </h4>
      <p> {{ post.content }} </p>
    </div>
  </div>
  <footer>I am the footer</footer>
</template>

<script>
export default {
  name: 'postsContainer',
  data() {
    return {
      posts: [
        {
          id: 0,
          title: 'The Hennessey Venom F5 Roadster is a 300mph hairdryer',
          description: 'Need to whip that barnet into shape pronto? Hennessey\'s 1,817bhp F5 Roadster should do the trick',
          content: `Wig wearers of the world look away now, for this is the blustery new 300+mph Hennessey Venom F5 Roadster. Good grief. 

Hennessey says the Roadster is “nearly identical mechanically” to the F5 coupe, with the carbon-fibre tub meaning just “minor adjustments” were needed to ensure that the open-roofed variant was as stiff as the hard-top. 

That means bringing the noise is the now-familiar 6.6-litre twin-turbo V8 that has been aptly titled Fury. A total of 1,817bhp is sent to the rear wheels through a seven-speed single-clutch semi-auto gearbox, meaning the F5 Roadster has all the tools to break Hennessey’s own ‘world’s fastest convertible’ record. For reference, that was the 265.6mph top speed set by the Venom GT Spyder, and we know that the F5 coupe has already been up in that ballpark during testing but is yet to attempt a run at its reported 311mph top end.`,
        },
        {
          id: 1,
          title: 'Embracer Group, the company forging one IP portfolio to rule them all, explained',
          description: 'The Swedish holding company doesn’t own quite everything that’s not Activision or EA, but it’s getting there',
          content: `The Embracer Group is a doozy of a media company. It’s 11 parent companies in a massive trench coat that are themselves composed of several more parent companies that own publishers and developers and the rights to video game franchises both AAA and indie. Earlier today, it added a bunch more companies to its roster including Limited Run Games, Maneater developer Tripwire Interactive, and the intellectual property rights to parts of The Lord of the Rings and The Hobbit universes.

To list all of Embracer Group’s companies and assets would take an unreasonable amount of time and space and would get kinda boring. So here are the high points in the company’s portfolio.`,
        },
        {
          id: 2,
          title: 'Who’s in your corner? An introduction to flag marshals',
          description: 'It happens in an instant. The usual harmony of synchronized downshifts turns to cacophony, followed by the nails-on-chalkboard screeching of metal sliding across pavement, and then the tell-tale plume of dust that a rider has careened off the racetrack. ',
          content: `It’s just another day in the tower for a flag marshal, and while each crash and incident on the racetrack are unique, the practiced protocol remains the same. With several years of experience waving flags at racetracks on both coasts, I get lots of questions from curious riders. What exactly does a flag marshal do? Are there qualifications to become a flag marshal? Do they get paid? How can I get started?
          The answers to those questions are as diverse as the racetracks, riding disciplines, rider skill levels, and localities involved. `,
        },
      ],
    };
  },

};

</script>

<style scoped>
footer {
  background-color: #42b983;
  padding: 200px 30px;
  color: white;
}
#postsContainer {
  display:flex;
  flex-direction: row;
  justify-content: space-between;
}
#postsContainer div {
   margin: 3em;
   padding: 1em;
   width: 100%;
}

#postsContainer div:hover {
   transition: 200ms all ease;
   outline: 8px solid #f2faf6;
}
</style>
