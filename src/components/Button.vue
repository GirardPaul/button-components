<script setup>
import { ref } from "vue";

defineProps({
  variant: String,
  size: {
    type: String,
    default: "md",
  },
  disableShadow: {
    type: Boolean,
    default: false,
  },
  disabled: {
    type: Boolean,
    default: false,
  },
  startIcon: String,
  endIcon: String,
  color: {
    type: String,
    default: "default",
  },
});
</script>

<template>
  <button
    type="button"
    class="btn"
    :class="[
      variant,
      size,
      color,
      disableShadow ? 'disableShadow' : '',
      disabled ? 'disabled' : '',
    ]"
  >
    <template v-if="startIcon">
      <div class="flex space-between align-center">
        <span class="material-icons mr-9">{{ startIcon }}</span>
        <span><slot></slot></span>
      </div>
    </template>
    <template v-else-if="endIcon">
      <div class="flex space-between align-center">
        <span><slot></slot></span>
        <span class="material-icons ml-9">{{ endIcon }}</span>
      </div>
    </template>
    <template v-else>
      <slot></slot>
    </template>
  </button>
</template>

<style scoped>
.mr-9 {
  margin-right: 9px;
}
.ml-9 {
  margin-left: 9px;
}
.flex {
  display: flex;
}
.space-between {
  justify-content: space-between;
}

.align-center {
  align-items: center;
}
.sm {
  height: 32px;
  padding: 6px 12px;
}
.md {
  height: 36px;
  padding: 8px 16px;
}
.lg {
  height: 42px;
  padding: 11px 22px;
}
.btn {
  background-color: #e0e0e0;
  border-radius: 6px;
  font-size: 14px;
  color: #3f3f3f;
  font-weight: 500;
  width: auto;
  border: none;
  cursor: pointer;
  box-shadow: 0px 2px 3px rgba(51, 51, 51, 0.2);
}

.outline {
  border: 1px solid #3d5afe;
}

.outline:hover,
.outline:focus,
.text:hover,
.text:focus {
  background: rgba(41, 98, 255, 0.1) !important;
}

.btn:hover,
.btn:focus {
  background-color: #aeaeae;
}

.text,
.outline {
  color: #3d5afe !important;
  background: transparent !important;
  box-shadow: none;
}

.disableShadow,
.disabled {
  box-shadow: none !important;
}

.disabled {
  color: #9e9e9e !important;
  cursor: default;
}

.disabled:hover,
.disabled:focus {
  background-color: #e0e0e0 !important;
}

.text.disabled:hover,
.text.disabled:focus {
  background-color: transparent !important;
}

.btn.primary {
  background-color: #2962ff;
  color: #fff;
}
.btn.primary:hover,
.btn.primary:focus {
  background-color: #0039cb;
}
.btn.secondary {
  background-color: #455a64;
  color: #fff;
}
.btn.secondary:hover,
.btn.secondary:focus {
  background-color: #1c313a;
}
.btn.danger {
  background-color: #d32f2f;
  color: #fff;
}
.btn.danger:hover,
.btn.danger:focus {
  background-color: #9a0007;
}
</style>
