<template>
  <div class="main">
    <div class="countdown">
      <table>
        <tr class="numbers">
          <td class="table-margin"></td>
          <td :class="days === 0 ? 'reached' : ''" class="days">{{ days }}</td>
          <td :class="days === 0 && hours === 0 ? 'reached' : ''">
            {{ hours }}
          </td>
          <td
            :class="days === 0 && hours === 0 && minutes === 0 ? 'reached' : ''"
          >
            {{ formatTime(minutes) }}
          </td>
          <td
            :class="
              days === 0 && hours === 0 && minutes === 0 && seconds === 0
                ? 'reached'
                : ''
            "
          >
            {{ formatTime(seconds) }}
          </td>
          <td class="table-prison"> en prison</td>
          <td class="table-margin"></td>
        </tr>
        <tr class="labels">
          <td class="table-margin"></td>
          <td>jour{{ days > 1 ? "s" : "" }}</td>
          <td>heure{{ hours > 1 ? "s" : "" }}</td>
          <td>minute{{ minutes > 1 ? "s" : "" }}</td>
          <td>seconde{{ seconds > 1 ? "s" : "" }}</td>
          <td class="table-prison"></td>
          <td class="table-margin"></td>
        </tr>
      </table>
    </div>
  </div>
</template>

<script>

export default {
    name: "CountDown",
    props: {
        crime: {
            type: String,
            required: true,
        },
    },
    data: function () {
        return {
            currentTime: this.computeTime(parseInt(this.crime)),
        };
    },
    watch: {
        crime: function(val) {
            this.currentTime= this.computeTime(parseInt(val));
        },
    },
  computed: {
    seconds() {
      return Math.floor((this.currentTime / 1000) % 60);
    },
    minutes() {
      return Math.floor((this.currentTime / 1000 / 60) % 60);
    },
    hours() {
      return Math.floor((this.currentTime / (1000 * 60 * 60)) % 24);
    },
    days() {
      return Math.floor(this.currentTime / (1000 * 60 * 60 * 24));
    },
  },
  methods: {
    formatTime(value) {
      if (value < 10) {
        return "0" + value;
      }
      return value;
    },
    computeTime(value) {
        const ratio = 331/13000000;
        return value*ratio*24*60*60*1000;
    },
  },
};
</script>

<style scoped>
.main {
  display: flex;
  justify-content: center;
  width: 100%;
  margin: 10px 0 0;
}

.countdown {
  display: flex;
  flex-direction: column;
  width: 800px;
}

.numbers {
  font-size: 50px;
  color: red;
  vertical-align: bottom;
}

.reached {
  color: green !important;
}

@media (max-width: 1250px) {
  .numbers {
    font-size: 40px;
  }
}

.labels {
  font-size: 20px;
}

.days {
  font-size: 80px;
  color: brown;
  vertical-align: bottom;
  line-height: 80px;
}

.table-margin {
  width: 50px;
}

.table-prison {
  width: 210px;
}

@media (max-width: 1250px) {
  .table-margin {
    width: 0px;
  }
}
</style>
