<template>
  <va-date-picker v-model="single" show-other-months first-weekday="Monday" class="display-1 h-[270px] overflow-hidden mt-[10px] w-full"/>
</template>

<script>
const datePlusDay = (date, days) => {
  const d = new Date(date)
  d.setDate(d.getDate() + days)
  return d
}
const nextWeek = datePlusDay(new Date(), 7)

export default {
  data () {
    return {
      single: new Date(),
      multiple: [new Date(), nextWeek],
      range: { start: new Date(), end: nextWeek },
    }
  },
}
</script>
<style>
.va-button, .va-day-picker__weekday, .va-date-picker-cell__day {
    font-size: 18px !important;
    font-weight: 100;
}
.va-date-picker-header__text{
    display: flex;
    align-items: flex-start;
    margin: 10px;
}
.va-date-picker__header{
    margin: 0 auto;
    width: 340px;
}
.va-icon{
    font-size: 22px !important;
    padding: 20px;
    font-weight: 900;
}
</style>