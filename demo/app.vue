<template>
  <div>
    <full-calendar class="test-fc" 
      :events="fcEvents" 
      first-day='1' locale="fr"
      @changeMonth="changeMonth"
      @eventClick="eventClick"
      @dayClick="dayClick"
      @moreClick="moreClick">
        <template slot="fc-body-card" slot-scope="slotProps" >
          <p>{{ slotProps.event.title }} test</p>
          <p>{{ slotProps.event.start }}</p>
        </template>
    </full-calendar>
  </div>
</template>
<script>
let demoEvents = [
    {
      title    : 'aaaaa',
      start    : '2018-12-25',
      end      : '2018-12-27',
      cssClass : 'family'
    },
    {
      title : 'Lunfel 726-727',
      start : '2018-12-26',
      end : '2018-12-27',
      cssClass : ['home', 'work']
    },
    {
      title : 'Lunfel 2/27-2/28',
      start : '2018-12-27',
      end : '2018-12-28'
    },
    {
        title : 'Lunfel 2/27-2/28',
        start : '2018-12-27',
        end : '2018-12-28'
    },
    {
        title : 'Lunfel 2/27-2/28',
        start : '2018-12-27',
        end : '2018-12-28'
    },
    {
        title : 'Lunfel 2/26-3/05',
        start : '2018-12-26',
        end : '2017-03-05'
    },
    {
        title : 'Lunfel 1/27-1/28',
        start : '2018-12-27',
        end : '2018-12-28'
    },
    {
        title : 'Lunfel 1/27-2/2',
        start : '2018-11-27',
        end : '2018-12-02'
    },
    {
        title : 'Lunfel 3/27-3/28',
        start : '2018-12-27',
        end : '2018-12-28'
    },
  ];

export default {
	data () {
		return {
          name:'Sunny!',
          fcEvents : demoEvents
        }
	},
  methods : {
    'changeMonth' (start, end, current) {
      // console.log('changeMonth', start.format(), end.format(), current.format())
    },
    'eventClick' (event, jsEvent, pos) {
       console.log('eventClick', event, jsEvent, pos)
    },
    'dayClick' (day, jsEvent) {
      console.log('dayClick', day, jsEvent)
    },
    'moreClick' (day, events, jsEvent) {
      console.log('moreCLick', day, events, jsEvent)
    }
  },
  components : {
    'full-calendar' : require('src/fullCalendar')
  }
}
</script>
<style lang='scss'>
  .app{
    color:green;
  }
  .family{
    background: red!important;
  }
</style>