<template>
    <div class="w-full">
    <div class="w-3/4 mx-auto rounded-full overflow-hidden">
      <link
        rel="stylesheet"
        href="https://maxcdn.bootstrapcdn.com/bootstrap/3.4.1/css/bootstrap.min.css"
      />
      <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"></script>
      <script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.4.1/js/bootstrap.min.js"></script>
      <div
        id="ProgressBar"
        class="progress-bar"
        role="progressbar"
        aria-valuenow="70"
        aria-valuemin="0"
        aria-valuemax="100"
        style="width: 100%"
      >
      <p id="Percentage" class="text-center h-fit m-auto"></p>
      </div>
    </div>
  </div>
</template>

<script>
import CurPros from '@/content/data.txt'
export default {
  mounted() {
    const a = document.getElementById('ProgressBar')
    const b = document.getElementById('Percentage')
    // const today = new Date();
    // const date = today.getFullYear()+'-'+(today.getMonth()+1)+'-'+today.getDate();
    // const dateTime = date;
    const percentage = (CurPros / 45) * 100
    console.log(percentage)
    b.innerHTML = percentage.toFixed(0) + "%"
    a.style.width = percentage + "%"
  }
}
</script>