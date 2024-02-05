<script setup>
defineProps({
  width: {
    type: Number,
    required: true
  },
  height: {
    type: Number,
    required: true
  }
})
</script>

<template>
  <svg
    :width=" width "
    :height="height "
    viewBox="0 0 100 51"
    fill="currentColor"
    xmlns="http://www.w3.org/2000/svg"
  >
    <rect width="100" height="51" fill="none" />
    <rect width="1280" height="4751" transform="translate(-94 -64)" fill="none" />
    <path d="M78.4862 0H88.4463L68.526 50.3981H57.3707L78.4862 0Z" fill="#213547" />
    <path
      d="M43.8566 43.4344L59.2723 7.75334H44.6123V0.645569H68.1892V7.61119L52.7735 43.2922H68.1892V50.4H43.8566V43.4344Z"
      fill="#213547"
    />
    <path
      d="M23.7052 0.645569H38.7259C43.7946 0.645569 47.5961 1.68804 50.1305 3.77299C52.6649 5.85794 53.932 8.91428 53.932 12.942V17.8464C53.932 21.8741 52.6649 24.9305 50.1305 27.0154C47.5961 29.1004 43.7946 30.1428 38.7259 30.1428H33.9044V50.4H23.7052V0.645569ZM38.7259 23.0351C40.3949 23.0351 41.6311 22.6797 42.4347 21.9689C43.3001 21.2581 43.7328 20.0498 43.7328 18.3439V12.4445C43.7328 10.7386 43.3001 9.53028 42.4347 8.81951C41.6311 8.10873 40.3949 7.75334 38.7259 7.75334H33.9044V23.0351H38.7259Z"
      fill="#213547"
    />
    <path
      d="M1.0355 29.5027L0 20.5469L10.7569 15.3642L24.159 9.60318V20.5469L8.21437 26.8728L24.159 33.1988V38.885L1.0355 29.5027Z"
      fill="#213547"
    />
    <path
      d="M99.0096 29.1788L100 20.3688L89.7112 15.2704L76.8925 9.60318V20.3688L92.1431 26.5917L76.8925 32.8147V38.4084L99.0096 29.1788Z"
      fill="#213547"
    />
  </svg>
</template>

<style scoped>
* {
  margin: 0;
  padding: 0;
}

svg {
  width: 5rem;
  height: 5rem;

}

path {
  fill: var(--vt-c-purple-light);
}


@media (prefers-color-scheme: dark) {
  path {
    fill: var(--vt-c-pink-light);
  }
}



</style>
