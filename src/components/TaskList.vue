<template>
  <div>
    <ul>
      <li>
        <div class="form-check">
          <label class="form-check-label">
            <input class="checkbox" type="checkbox" /> For what reason would it
            be advisable.</label
          >
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "TaskList",
};
</script>

<style scoped>
.form-check {
  margin: 10px 0;
  background: #f7f7f7;
  padding: 15px;
}
</style>