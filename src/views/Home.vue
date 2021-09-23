<template>
  <div class="page-wrapper">
    <div class="card-content">
      <div class="card-section card-top">
        <h1 class="title">Join our community</h1>

        <h2 class="small-title">30-day, hassle-free money back guarantee</h2>

        <p>Gain access to our full library of tutorials along with expert code reviews.
          Perfect for any developers who are serious about honing their skills.</p>
      </div>

      <div class="card-bottom">
        <div class="card-section bottom-left">
          <h2 class="small-title">Monthly Subscription</h2>

          <p class="price-line">$29 <span>per month</span></p>

          <p>Full access for less than &dollar;1 a day</p>

          <a href="#" class="cta-btn">Sign Up</a>
        </div>
        <div class="card-section bottom-right">
          <h2 class="small-title">Why Us</h2>

          <ul>
            <li>Tutorials by industry experts</li>
            <li>Peer & expert code review</li>
            <li>Coding exercises</li>
            <li>Access to our GitHub repos</li>
            <li>Community forum</li>
            <li>Flashcard decks</li>
            <li>New videos every week</li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { mapState } from 'vuex'

export default {
  head() {
    return {
      title: {
        inner: 'Home'
      },
      meta: [
        {
          name: 'description',
          content: `${this.appTitle} home page`,
          id: 'desc'
        }
      ]
    }
  },
  computed: mapState('app', ['appTitle'])
}
</script>

<style lang="scss" scoped>
@import '@/theme/variables.scss';

.page-wrapper {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 40px;

  .card-content {
    //width: 45%;
    max-width: 635px;
    border-radius: 8px;
    background: $light;
    box-shadow: 0 15px 30px rgba(0, 81, 171, 0.148847);

    .title,
    .small-title {
      font-weight: 700;
    }

    .title {
      font-size: 24px;
      line-height: 28px;
      letter-spacing: -0.3px;
      color: $primaryColor1;

      @media (max-width: 767px) {
        font-size: 20px;
        line-height: 23px;
        letter-spacing: -0.25px;
      }
    }

    .small-title {
      font-size: 18px;
      line-height: 21px;
      letter-spacing: -0.225px;
    }

    .cta-btn {
      display: inline-block;
      margin-top: 26px;
      width: 100%;
      text-align: center;
      line-height: 19px;
      padding: 15px 0 14px;
      background: $primaryColor2;
      color: $light;
      font-weight: 700;
      border-radius: 5px;
      box-shadow: 0 10px 10px rgba(0, 0, 0, 0.0973011);
    }

    .card-section {
      padding: 40px;
    }

    .card-top {
      .small-title {
        margin: 24px 0 11px;
        color: $primaryColor2;

        @media (max-width: 767px) {
          font-size: 15px;
          line-height: 20px;
          letter-spacing: -0.1875px;
        }
      }

      p {
        color: $neutralColor2;
      }
    }

    .card-bottom {
      display: flex;
      align-items: stretch;
      background: $primaryColor1;
      color: $light;
      border-radius: 0 0 8px 8px;

      @media (max-width: 767px) {
        flex-direction: column;
      }

      .card-section {
        width: 50%;

        @media (max-width: 767px) {
          width: 100%;
        }
      }

      .bottom-left {
        .price-line {
          display: flex;
          align-items: center;
          margin: 18px 0 4px;
          font-size: 32px;
          font-weight: 700;
          line-height: 37px;
          letter-spacing: -0.4px;

          span {
            margin-left: 11px;
            font-size: 16px;
            line-height: 26px;
            font-weight: 400;
            letter-spacing: -0.2px;
            mix-blend-mode: normal;
            opacity: 0.5;
          }
        }
      }

      .bottom-right {
        background: rgba($light, .15);

        ul {
          margin: 18px 0 0;
          list-style: none;
          padding: 0;

          li {
            font-family: $textFont;
            font-size: 14px;
            line-height: 20px;
            letter-spacing: -0.175px;
            mix-blend-mode: normal;
            opacity: 0.75;
          }
        }
      }
    }
  }
}
</style>
