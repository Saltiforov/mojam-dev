<template>
  <section id="item__info">
    <div class="container-s item__info">
      <img src="/point-big.svg" alt="point" class="item__info-point">
      <div class="item__info-socials">
        <img src="/social-networks/facebook.png" alt="facebook">
        <img src="/social-networks/linkedIn.png" alt="linkedIn">
        <img src="/social-networks/twitter.png" alt="twitter">
      </div>
      <p class="item__info-description subtitle">
        As a <span>UX/UI Designer</span>, your responsibility is the user. You should have solid skills in research,
        strategy,
        prototyping, interaction design, and architecture. You’ll be heavily involved in the project process and will
        set standards for how people should interact with digital environments. <br>
        <br>
        We are a small team of wildly skilled creatives with a lot of range who love to take on big challenges for the
        chance to reap even bigger successes. As a vital member of our web development team, you'll have a huge impact
        on crafting the digital presence of both the Interactive Agency and our internal clients. <br>
        <br>
        The Interactive Agency collaborates with Products in different regions to build a regionally relevant
        interaction experience between users and games and provides deep expertise in the web environment. <br>
        <br>
        If you're aching to flex your creative and rational muscles, we want you to join us.
      </p>
      <div class="item__info-block">
        <h3 class="item__info-block-title title afterText">What will you do?</h3>
        <ul class="item__info-block-list">
          <li class="subtitle">Participate in all phases of the project life cycle</li>
          <li class="subtitle">Creatively solve problems at all levels of detail: from the big picture (ideation) to the
            nuts and bolts
          </li>
          <li class="subtitle">Create UI design concepts</li>
          <li class="subtitle">Collaborate on wireframe prototypes to explore interactive behaviors and front-end
            technological capabilities
          </li>
          <li class="subtitle">Present rationale for design decisions internally and to clients</li>
          <li class="subtitle">Apply engaging visual styles to wireframes and conceptual prototypes</li>
          <li class="subtitle">Translate complex operations into intuitive interfaces and interactions</li>
          <li class="subtitle">Drive the development and communication of design guidelines, patterns, and libraries
          </li>
        </ul>
      </div>
      <div class="item__info-block" style="padding-top: 1.3rem;">
        <h3 class="item__info-block-title title afterText">What are we looking for?</h3>
        <ul class="item__info-block-list looking-list">
          <li class="subtitle">3+ years of experience as a User Experience Designer, Interaction Designer, Art Director,
            or similar role working with web applications or software products
          </li>
          <li class="subtitle">Digital agency experience or experience with a SaaS product company preferred</li>
          <li class="subtitle">Demonstrated skill applying best UI design principles and practices</li>
          <li class="subtitle">Experience with toolsets: Figma, Adobe Creative Suite</li>
          <li class="subtitle">Confidence, strong communication and the ability to discuss, explain and brainstorm with
            team members for UX/UI solutions
          </li>
          <li class="subtitle">Demonstrated ability to gather feedback from peers and stakeholders and incorporate to
            improve the final product
          </li>
          <li class="subtitle">A fearless and positive attitude</li>
          <li class="subtitle">Strong UI/UX experience with a deep knowledge of best practices and user expectations
          </li>
          <li class="subtitle">A fearless and positive attitude</li>
          <li class="subtitle">Upper-Intermediate or higher level of English</li>
        </ul>
      </div>
      <div class="item__info-button">
        <button class="button__orange">Показать нам свое CV</button>
      </div>
    </div>
  </section>
</template>
<style lang="scss">
#item__info {
  width: 100%;
  height: 141rem;
  position: relative;
}

.item__info {
  padding-top: 7.2rem;

  &-point {
    position: absolute;
    left: 13rem;
    top: 9rem;
    width: 12.9rem;
  }

  &-socials {
    display: flex;
    justify-content: flex-end;
    align-items: center;

    img {
      width: 2rem;
      margin-left: 1.6rem;
    }
  }

  &-description {
    padding-top: 2.6rem;

    span {
      color: $green;
      font-weight: 600;
    }
  }

  &-block {
    padding-top: 3rem;

    &-list {
      padding-top: 3rem;
      padding-left: 12rem;
      width: 55rem;

      li {
        list-style-type: inherit;
        padding-bottom: 1.8rem;
      }
    }
  }

  &-button {
    display: flex;
    justify-content: center;
    margin-top: 4rem;
    margin-right: 11rem;
  }
}

@media screen and (max-width: 460px) {
  #item__info {
    height: 100%;
  }
  .item__info {
    &-socials {
      padding: 22.4rem 0 24rem;

      img {
        width: 8rem;

        &:nth-child(2) {
          padding: 0 6.4rem;
        }
      }

    }

    &-point {
      display: none;
    }

    .subtitle {
      font-size: 5.6rem;
      line-height: 6.4rem;
      padding-bottom: 8rem;
    }

    &-description {
      padding-bottom: 17.6rem;
    }

    &-block-list {
      width: 100rem;
      margin: auto;
      padding-bottom: 14.4rem;
    }

    .looking-list {
      padding-bottom: 22.8rem;
    }

    &-button {
      padding-bottom: 33.6rem;
    }
  }
}
</style>
