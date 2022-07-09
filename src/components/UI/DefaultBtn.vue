<template>
  <div>
    <button class="default-btn" type="button">Написать</button>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.default-btn {
  display: inline-block;
  padding: 15px 35px;

  font-size: 18px;
  font-weight: 600;
  letter-spacing: 1.25px;
  text-transform: uppercase;
  text-shadow: 0 0 10px rgba(255, 255, 255, 0.75);
  color: #fff;

  cursor: pointer;
  outline: none;
  background-color: rgba(0, 0, 0, 0.5);
  border: 2px solid #fd0202;
  border-radius: 4px;

  transition: all 0.3s ease;
}
.default-btn:hover {
  background-color: #fd0202;
}
</style>
