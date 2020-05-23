<script>
import { Line } from "vue-chartjs";
export default {
  name: "HelloWorld",
  props: {
    msg: String
  },
  extends: Line,
  data: () => ({
    options: {
      responsive: true,
      maintainAspectRatio: false,
      legend: {
        display: true,
        position: "top",
        align: "start",
        labels: {
          boxWidth: 0,
          fontSize: 22,
          padding: 20,
          fontStyle: "bold",
          fontFamily: "Arial",
          fontColor: "#B0B0B0"
        }
      },
      scales: {
        xAxes: [
          {
            gridLines: {
              display: false
            }
          }
        ],
        yAxes: [
          {
            gridLines: {
              display: false
            },
            ticks: {
              display: false
            }
          }
        ]
      }
    }
  }),
  mounted() {
    // Overwriting base render method with actual data.
    this.renderChart(
      {
        labels: [
          "January",
          "February",
          "March",
          "April",
          "May",
          "June",
          "July",
          "August",
          "September",
          "October",
          "November",
          "December"
        ],
        datasets: [
          {
            label: "Daily Turnips Prices",
            backgroundColor: "rgba(220,220,220,0.42)",
            borderColor: "#f76a8c",
            // width: "81%",
            fill: true,
            data: [40, 20, 12, 39, 10, 40, 39, 80, 40, 20, 12, 11]
          }
        ]
      },
      this.options
    );
  }
};
</script>
