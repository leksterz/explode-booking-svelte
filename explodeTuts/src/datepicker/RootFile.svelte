<script>
  import DatePicker from "./DatePicker.svelte";

  let currentDate = new Date();

  const onDateChange = (d) => {
    currentDate = d.detail;
  };
</script>

<style>
  body {
    text-align: center;
  }
</style>

<body>
  <h3>Select Your Session Date</h3>
  <DatePicker
    on:datechange={onDateChange}
    selected={currentDate}
    isAllowed={(date) => {
      const millisecs = date.getTime();
      if (millisecs + 25 * 3600 * 1000 < Date.now()) return false;
      if (millisecs > Date.now() + 3600 * 24 * 10 * 1000) return false;
      return true;
    }} />
</body>
<!--
  // setInterval(() => {
  //   currentDate = new Date(currentDate.getTime() + 24 * 3600 * 1000);
  // }, 1000);

  // const isAllowed = date => {
  //   const millisecs = date.getTime();
  //   if (millisecs + 25 * 3600 * 1000 < Date.now()) return false;
  //   if (millisecs > Date.now() + 3600 * 24 * 30 * 1000) return false;
  //   return true;
  // };
-->
