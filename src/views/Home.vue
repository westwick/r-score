<template>
  <div class="home">
    <div class="header">
      <div class="title">Your relationship with <span>Sara</span></div>
      <div class="tot-score">-15</div>
      <div class="subnav">
        <p>Overview</p>
        <p>Goals</p>
        <p>History</p>
      </div>
    </div>
    <div class="feed">
      <div class="today feed-card">
        <p class="card-title">Today</p>
        <div class="card-content">
          <div class="male gender-section">
            <p class="gender-title">Mark</p>
            <div class="f finance"><i class="fa fa-money" aria-hidden="true"></i> Bought groceries ($45), car oil change ($30)</div>
            <div class="f favor"><i class="fa fa-gift" aria-hidden="true"></i> Gave back massage (+10)</div>
          </div>
          <div class="female gender-section">
            <p class="gender-title">Sara</p>
            <p class="f finance"><i class="fa fa-money" aria-hidden="true"></i> Coffee run ($12.40)</p>
            <p class="f favor"><i class="fa fa-gift" aria-hidden="true"></i> Made Breakfast (+10), Dishes (+10), Dropped off package at fedex (+5)</p>
          </div>
        </div>
      </div>
      <div class="the-past feed-card">
        <div class="card-content">
          <div class="day-section first">
            <p class="card-title">Yesterday <span>Sep 3, 2020</span> <span class="change">-15</span></p>
            <div class="gender-wrap">
              <div class="male gender-section">
                <p class="gender-title">Mark</p>
                <div class="f finance"><i class="fa fa-money" aria-hidden="true"></i> 2 Finances <i class="fa fa-caret-down" aria-hidden="true"></i></div>
                <div class="f favor"><i class="fa fa-gift" aria-hidden="true"></i> 3 Favors <i class="fa fa-caret-down" aria-hidden="true"></i></div>
              </div>
              <div class="female gender-section">
                <p class="gender-title">Sara</p>
                <p class="f finance"><i class="fa fa-money" aria-hidden="true"></i> 2 Finances <i class="fa fa-caret-down" aria-hidden="true"></i></p>
                <p class="f favor"><i class="fa fa-gift" aria-hidden="true"></i> 1 Favor <i class="fa fa-caret-down" aria-hidden="true"></i></p>
              </div>
            </div>
          </div>
          <div class="day-section">
            <p class="card-title">Tuesday <span>Sep 2, 2020</span> <span class="change">-5</span></p>
            <div class="gender-wrap">
              <div class="male gender-section">
                <p class="gender-title">Mark</p>
                <div class="f finance"><i class="fa fa-money" aria-hidden="true"></i> 0 Finances <i class="fa fa-caret-down" aria-hidden="true"></i></div>
                <div class="f favor"><i class="fa fa-gift" aria-hidden="true"></i> 0 Favors <i class="fa fa-caret-down" aria-hidden="true"></i></div>
              </div>
              <div class="female gender-section">
                <p class="gender-title">Sara</p>
                <p class="f finance"><i class="fa fa-money" aria-hidden="true"></i> 0 Finances <i class="fa fa-caret-down" aria-hidden="true"></i></p>
                <p class="f favor"><i class="fa fa-gift" aria-hidden="true"></i> 2 Favors <i class="fa fa-caret-down" aria-hidden="true"></i></p>
              </div>
            </div>
          </div>
          <div class="day-section last">
            <p class="card-title">Monday <span>Sep 1, 2020</span> <span class="change">+5</span></p>
            <div class="gender-wrap">
              <div class="male gender-section">
                <p class="gender-title">Mark</p>
                <div class="f finance"><i class="fa fa-money" aria-hidden="true"></i> 3 Finances <i class="fa fa-caret-down" aria-hidden="true"></i></div>
                <div class="f favor"><i class="fa fa-gift" aria-hidden="true"></i> 1 Favor <i class="fa fa-caret-down" aria-hidden="true"></i></div>
              </div>
              <div class="female gender-section">
                <p class="gender-title">Sara</p>
                <p class="f finance"><i class="fa fa-money" aria-hidden="true"></i> 2 Finances <i class="fa fa-caret-down" aria-hidden="true"></i></p>
                <p class="f favor"><i class="fa fa-gift" aria-hidden="true"></i> 0 Favors <i class="fa fa-caret-down" aria-hidden="true"></i></p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from "@/components/HelloWorld.vue";

export default {
  name: "Home",
  // components: {
  //   HelloWorld
  // }
};
</script>

<style lang="scss">
.home {
  width: 400px;
  height: 750px;
  overflow: scroll;
  background: #fff;
  text-align: left;
  border-radius: 6px;
}
.header {
  background: #f8f8f8;
  padding: 16px;
  position: relative;
}
.title {
  font-size: 20px;
  color: #111;
  font-weight: bold;

  span {
    color: #e16190;
  }
}
.subnav {
  display: flex;
  font-size: 14px;
  padding: 16px 0 0;
  
  p {
    padding-right: 24px;
    color: #888;
    margin: 0;

    &:first-child {
      font-weight: bold;
      color: #666;
    }
  }
}
.feed {
  padding: 16px;

  .feed-card {
    box-shadow: 0 1px 3px rgba(0,0,0,0.12), 0 1px 2px rgba(0,0,0,0.24);
    border-left: 3px solid #e16190;
    padding: 8px;
    margin-bottom: 16px;

    .card-content {
      font-size: 14px;
      p {
        margin: 0;
      }
    }

    p.card-title {
      color: #e16190;
      text-transform: uppercase;
      font-size: 11px;
      margin: 0 0 16px;

      span {
        color: #888;
        padding-left: 16px;
      }
    }
  }
}
.feed-card.the-past {
  border-left: 3px solid #7ec0ec;
  
  p.card-title {
    color: #7ec0ec;
    position: relative;
  }
}
.gender-section {
  .gender-title {
    font-weight: bold;
    color: #666;
  }
  .f {
    color: #999;
  }
}
.gender-section.male {
  margin-bottom: 16px;
}
.female {
  text-align: right;
}
.day-section {
  margin-top: 16px;
  border-bottom: 1px solid #e8e8e8;

  .female {
    margin-bottom: 16px;
  }

  &.first {
    margin-top: 0;
  }

  &.last {
    border-bottom: none;
  }
}
.gender-wrap {
  display: flex;
  justify-content: space-between;
}
.fa-money {
  color: #98de2f;
}
.fa-gift {
  color: #be2fde;
  margin-left: 1.5px;
  margin-right: 1.5px;
}
.tot-score {
  position: absolute;
  top: 16px;
  right: 16px;
  border-radius: 12px;
  z-index: 2;
  background: #e16190;
  padding: 2px 8px;
  color: #fff;
  font-weight: bold;
  font-size: 18px;
}
.change {
  text-align: center;
  position: absolute;
  right: 0;
  padding: 2px 6px !important;
  border-radius: 3px;
  background: #7ec0ec;
  color: #fff !important;
  font-weight: bold;
  font-size: 12px;
}
</style>
