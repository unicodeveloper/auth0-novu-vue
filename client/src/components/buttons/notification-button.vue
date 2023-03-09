<template>
  <div>
    <NotificationCenterComponent
      :subscriberId="subscriberId"
      :applicationIdentifier="applicationIdentifier"
      :sessionLoaded="sessionLoaded"
      :placement="popover"
      :styles="styles"
      :backendUrl="backendUrl"
      :socketUrl="socketUrl"
      v-slot="slot"
    >
    </NotificationCenterComponent>
  </div>
</template>

<script>
export default {
  data() {
    return {
      applicationIdentifier: "wLXel7MBnUEt",
      subscriberId: "on-boarding-subscriber-id-123",
      backendUrl: "https://dev.api.novu.co",
      socketUrl: "wss://dev.ws.novu.co",
      message: "",
      popover: "bottom-start",
      styles: {
        bellButton: {
          dot: {
            "> rect": {},
            left: "15%",
          },
          root: {
            "> svg": { minWidth: "45px", height: "45px" },
            width: "50px",
            height: "50px",
          },
        },
      },
    };
  },
  methods: {
    sessionLoaded() {
      console.log("Session loaded!");
    },
  },
};
</script>
