<template>
    <div class="container table animate__animated animate__zoomIn">
        <h4 class="container">BMI range</h4>
        <hr>
         <table class="container highlight">
        <thead>
          <tr>
              <th>Body mass index</th>
              <th>Weight Status</th>
          </tr>
        </thead>
        <tbody>
          <tr class="below">
            <td>Below 18.5</td>
            <td>Underweight</td>
          </tr>
          <tr class="normal">
            <td>18.5 — 24.9</td>
            <td>Normal</td>
          </tr>
          <tr class="warning">
            <td>25.0 — 29.9</td>
            <td>Overweight</td>
          </tr>
          <tr class="danger">
            <td>30.0 and Above</td>
            <td>Obese</td>
          </tr>
        </tbody>
      </table>
    </div>
</template>

