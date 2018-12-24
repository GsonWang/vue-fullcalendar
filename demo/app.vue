<template>
  <div>
    <full-calendar
      class="test-fc"
      :events="fcEvents"
      first-day="1"
      locale="fr"
      @changeMonth="changeMonth"
      @eventClick="eventClick"
      @dayClick="dayClick"
      @moreClick="moreClick"
    >
      <template slot="fc-body-card" class="test-fc-item" slot-scope="slotProps">
        <span style="height: 15.2px;">{{ slotProps.event.title}}</span>
        <span style="height: 15.2px;">{{ slotProps.event.desc }}</span>
      </template>
    </full-calendar>
  </div>
</template>
<script>
let demoEvents = [
  {
    title: "RC68A",
    desc: "灯光测试",
    start: "2018-12-09",
    end: "2018-12-10",
    cssClass: ["test-fc-item", "green"],
    data: {
      name: "RC68A",
      excetDataStart: "2018-12-09",
      excetDataEnd: "2018-12-10",
      excetTimeEnd: "09:00",
      excetTimeEnd: "11:00",
      engineName: "李文军",
      place: "灯光实验室"
    }
  },
  {
    title: "RC68A",
    desc: "灯光测试",
    start: "2018-12-09",
    end: "2018-12-10",
    cssClass: ["test-fc-item", "green"],
    data: {
      name: "RC68A",
      excetDataStart: "2018-12-09",
      excetDataEnd: "2018-12-10",
      excetTimeEnd: "09:00",
      excetTimeEnd: "11:00",
      engineName: "李文军",
      place: "灯光实验室"
    }
  },
  {
    title: "RC68A",
    desc: "灯光测试",
    start: "2018-12-09",
    end: "2018-12-10",
    cssClass: ["test-fc-item", "green"],
    data: {
      name: "RC68A",
      excetDataStart: "2018-12-09",
      excetDataEnd: "2018-12-10",
      excetTimeEnd: "09:00",
      excetTimeEnd: "11:00",
      engineName: "李文军",
      place: "灯光实验室"
    }
  },
  {
    title: "RC68A",
    desc: "灯光测试",
    start: "2018-12-09",
    end: "2018-12-10",
    cssClass: ["test-fc-item", "green"],
    data: {
      name: "RC68A",
      excetDataStart: "2018-12-09",
      excetDataEnd: "2018-12-10",
      excetTimeEnd: "09:00",
      excetTimeEnd: "11:00",
      engineName: "李文军",
      place: "灯光实验室"
    }
  },
  {
    title: "RC68A",
    desc: "排放测试",
    start: "2018-12-12",
    end: "2018-12-14",
    cssClass: ["test-fc-item", "blue"],
    data: {
      name: "RC68A",
      excetDataStart: "2018-12-12",
      excetDataEnd: "2018-12-14",
      excetTimeEnd: "09:00",
      excetTimeEnd: "11:00",
      engineName: "李文军",
      place: "灯光实验室"
    }
  },
  {
    title: "RC68A",
    desc: "排放测试",
    start: "2018-12-15",
    end: "2018-12-17",
    cssClass: ["test-fc-item", "red"],
    data: {
      name: "RC68A",
      excetDataStart: "2018-12-15",
      excetDataEnd: "2018-12-17",
      excetTimeEnd: "09:00",
      excetTimeEnd: "11:00",
      engineName: "李文军",
      place: "灯光实验室"
    }
  },
  {
    title: "RC68A",
    desc: "EMC测试",
    start: "2018-12-23",
    end: "2018-12-27",
    cssClass: ["test-fc-item"],
    data: {
      name: "RC68A",
      excetDataStart: "2018-12-23",
      excetDataEnd: "2018-12-27",
      excetTimeEnd: "09:00",
      excetTimeEnd: "11:00",
      engineName: "李文军",
      place: "灯光实验室"
    }
  },
  {
    title: "RC68A",
    desc: "外场性能测试",
    start: "2018-12-20",
    end: "2018-12-23",
    cssClass: ["test-fc-item"],
    data: {
      name: "RC68A",
      excetDataStart: "2018-12-20",
      excetDataEnd: "2018-12-23",
      excetTimeEnd: "09:00",
      excetTimeEnd: "11:00",
      engineName: "李文军",
      place: "灯光实验室"
    }
  }
];

export default {
  data() {
    return {
      name: "Sunny!",
      fcEvents: demoEvents
    };
  },
  methods: {
    changeMonth(start, end, current) {
      // console.log('changeMonth', start.format(), end.format(), current.format())
    },
    eventClick(event, jsEvent, pos) {
      console.log("eventClick", event, jsEvent, pos);
    },
    dayClick(day, jsEvent) {
      console.log("dayClick", day, jsEvent);
    },
    moreClick(day, events, jsEvent) {
      console.log("moreCLick", day, events, jsEvent);
    }
  },
  components: {
    "full-calendar": require("src/fullCalendar")
  }
};
</script>
<style lang='scss'>
.app {
  color: green;
}

.test-fc-item {
  height: auto !important;
  display: flex;
  justify-content: space-between;
  flex-direction: column;
}

.green {
  color: #fff !important;
  background: green !important;
}
.blue {
  color: #fff !important;
  background: blue !important;
}
.red {
  color: #fff !important;
  background: red !important;
}
</style>