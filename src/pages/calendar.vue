<style>
.fc-day-sun a {
  color: red;
  text-decoration: none;
}

.fc-day-sat a {
  color: blue;
  text-decoration: none;
}
</style>
<script>
import FullCalendar from '@fullcalendar/vue3'
import dayGridPlugin from '@fullcalendar/daygrid'
import interactionPlugin from '@fullcalendar/interaction'
import googleCalendarPlugin from '@fullcalendar/google-calendar';

export default {
  components: {
    FullCalendar // make the <FullCalendar> tag available
  },
  data() {
    return {
      calendarOptions: {
        plugins: [ dayGridPlugin, interactionPlugin, googleCalendarPlugin],
        initialView: 'dayGridMonth',
        dateClick: this.handleDateClick,
        locale: 'ko',
        googleCalendarApiKey : "AIzaSyArjiSM6R8xSHSFOz5IlJ3FvLLUpHT7m3s",
        eventSources :[ 
            {
                googleCalendarId : 'ko.south_korea#holiday@group.v.calendar.google.com'
                , color: 'white'   // an option!
                , textColor: 'red' // an option!
                , className : "ko_event"
            } 
        ],
        events: [
            {
                id: 1,
                title: 'Test1',
                start: '2023-11-14',
                end: '2023-11-15'
            },
            {
                id: 2,
                title: 'Test2',
                start: '2023-11-14',
                end: '2023-11-16'
            }
        ]
      }
    }
  },
  methods: {
    handleDateClick: function(arg) {
      confirm('date click! ' + arg.dateStr)
    }
  }
}
</script>
<template>
    <div class="content">
        <FullCalendar :options="calendarOptions" />
    </div>
</template>