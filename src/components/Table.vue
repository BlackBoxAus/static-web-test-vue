<template>
  <div class="client-container">
    <div class="info-panel">
      <div>
        <h4>Clients</h4>
        <p>This table contains client information</p>
      </div>
      <div class="client-details">
        <button v-on:click="clientAlert">Add a client</button>
      </div>
    </div>

    <div class="table-container">
      <table>
        <thead>
          <tr>
            <th>Client Name</th>
            <th>Project</th>
            <th>Member</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="client in clients" :key="client.id">
            <td>{{ client.name }}</td>
            <td>{{ client.project }}</td>
            <td>{{ client.member }}</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>

<script>
export default {
  name: "DataTable",
  data() {
    return {
      clients: [
        {
          id: 487,
          name: "John Holland",
          project: "Wearne Lookout",
          member: "2 members",
        },
        {
          id: 512,
          name: "Brisbane Council",
          project: "George Sqaure Station",
          member: "11 members",
        },
        {
          id: 874,
          name: "Brisbane Council",
          project: "Charlotte Street",
          member: "17 members",
        },
      ],
    };
  },
  methods: {
    clientAlert() {
      alert("Cannot add a client right now. Please try later.");
    },
  },
};
</script>

<style lang="scss" scoped>
.client-container {
  padding: 0.2rem;
  width: 50%;
  box-shadow: rgba(0, 0, 0, 0.12) 0px 1px 3px, rgba(0, 0, 0, 0.24) 0px 1px 2px;
  border-radius: 4px;

  .info-panel {
    display: flex;
    margin-top: 0.5rem;

    justify-content: space-between;
  }

  .table-container {
    line-height: 1.25rem;

    table {
      margin-top: 0.5rem;
      text-align: left;
      border: 1px solid #c0c0c0;
      background-color: #f3f3f3;
      border-collapse: collapse;
      width: 100%;

      tr,
      td,
      thead {
        padding: 2px;
        border: 1px solid #e0e0e0;
      }
      thead {
        background-color: #e0e0e0;
      }
    }
  }

  .client-details {
    button {
      background-color: #212121;
      color: white;
      outline: none;
      border-radius: 4px;
      border: none;
      height: 2rem;
      text-align: center;
      width: 8rem;
      font-size: 1rem;
      cursor: pointer;

      &:hover {
        background-color: #484848;
      }
    }
  }
}
</style>