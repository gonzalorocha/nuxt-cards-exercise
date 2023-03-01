<template>
  <button
    @click="onClick"
    :class="[
      'bg-blue',
      'text-white',
      'w-32',
      'h-13',
      'rounded-3xl',
      'justify-center',
      'items-center',
      'text-2xs',
      'font-semibold',
      'flex',
      'flex-row',
      'gap-2',
      'uppercase',
      className,
    ]"
  >
    {{ text }}
    <Icon name="Arrow" :width="20" :height="20" />
  </button>
</template>

<script>
import cn from "classnames";
import Icon from "~/components/ui/Icon";

export default {
  name: "Button",
  props: {
    text: {
      type: String,
      required: true,
    },
    className: {
      type: String,
      default: "",
    },
    onClick: {
      type: Function,
      required: true,
    },
  },
  components: {
    Icon,
  },
  computed: {
    buttonClasses() {
      return cn(
        "bg-blue",
        "text-white",
        "w-32",
        "h-13",
        "rounded-3xl",
        "justify-center",
        "items-center",
        "text-2xs",
        "font-semibold",
        "flex",
        "flex-row",
        "gap-2",
        "uppercase",
        this.className
      );
    },
  },
};
</script>
