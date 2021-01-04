<template>
  <v-container>
    <v-row class="text-center">
      <v-col class="mb-4">
        <h1 class="display-2 font-weight-bold mb-3">Data Table</h1>
        <v-card dark>
          <v-select
            v-model="FilterStatus"
            :items="statusFilterList"
            label="Status"
            clearable
          ></v-select>
          <v-data-table
            dense
            :headers="headers"
            :items="filteredItems"
            style="color: orange"
            :items-per-page="10"
            :search="search"
            :custom-filter="customFilter"
            class="elevation-1"
          >
            <template v-slot:[`item.status`]="{ item }">
              <tr
                :style="{
                  color:
                    item.status === 'FILLED'
                      ? 'green'
                      : item.status === 'UNFILLED'
                      ? 'red'
                      : item.status === 'PARTIALLY FILLED'
                      ? 'yellow'
                      : 'unset',
                }"
              >
                <td>
                  {{ item.status }}
                </td>
              </tr>
            </template>
          </v-data-table>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "HelloWorld",

  data() {
    return {
      search: "",
      FilterStatus: "ALL",
      statusFilterList: [
        "ALL",
        "NEW ORDER",
        "EXEC PENDING",
        "FILLED",
        "UNFILLED",
        "PARTIALLY FILLED",
      ],
      headers: [
        { text: "Order ID", value: "order_id" },
        { text: "Application Source", value: "application_source" },
        { text: "Status", value: "status" },
        { text: "Trading Venue", value: "trading_venue" },
        { text: "Broker Deal Code", value: "broker_deal_code" },
        { text: "Side", value: "side" },
        { text: "Security Ticker", value: "security_ticker" },
        { text: "Order Size [Contracts]", value: "order_size" },
        { text: "Amount", value: "amount" },
        { text: "Price-Buy", value: "price_buy" },
        { text: "Price-Sell", value: "price_sell" },
        { text: "Timestamp", value: "time_stamp" },
      ],
      list: [
        {
          order_id: "1111",
          application_source: "RobotFX",
          status: "NEW ORDER",
          trading_venue: "B3 Exchange",
          broker_deal_code: "ABCB",
          side: "BUY",
          security_ticker: "DOLV20",
          order_size: "250,000,00",
          amount: "?",
          price_buy: "-",
          price_sell: "-",
          time_stamp: "7/29/2019 12:04",
        },
        {
          order_id: "2222",
          application_source: "RobotFX",
          status: "EXEC PENDING",
          trading_venue: "B3 Exchange",
          broker_deal_code: "ABCB",
          side: "BUY",
          security_ticker: "DOLV20",
          order_size: "250,000,00",
          amount: "?",
          price_buy: "-",
          price_sell: "-",
          time_stamp: "7/29/2019 12:04",
        },
        {
          order_id: "3333",
          application_source: "RobotFX",
          status: "FILLED",
          trading_venue: "B3 Exchange",
          broker_deal_code: "ABCB",
          side: "BUY",
          security_ticker: "DOLV20",
          order_size: "250,000,00",
          amount: "?",
          price_buy: "-",
          price_sell: "-",
          time_stamp: "7/29/2019 12:04",
        },
        {
          order_id: "4444",
          application_source: "RobotFX",
          status: "FILLED",
          trading_venue: "B3 Exchange",
          broker_deal_code: "ABCB",
          side: "BUY",
          security_ticker: "DOLV20",
          order_size: "250,000,00",
          amount: "?",
          price_buy: "-",
          price_sell: "-",
          time_stamp: "7/29/2019 12:04",
        },
        {
          order_id: "5555",
          application_source: "RobotFX",
          status: "UNFILLED",
          trading_venue: "B3 Exchange",
          broker_deal_code: "ABCB",
          side: "BUY",
          security_ticker: "DOLV20",
          order_size: "250,000,00",
          amount: "?",
          price_buy: "-",
          price_sell: "-",
          time_stamp: "7/29/2019 12:04",
        },
        {
          order_id: "12351",
          application_source: "RobotFX",
          status: "FILLED",
          trading_venue: "B3 Exchange",
          broker_deal_code: "ABCB",
          side: "BUY",
          security_ticker: "DOLV20",
          order_size: "250,000,00",
          amount: "?",
          price_buy: "-",
          price_sell: "-",
          time_stamp: "7/29/2019 12:04",
        },
        {
          order_id: "12352",
          application_source: "RobotFX",
          status: "PARTIALLY FILLED",
          trading_venue: "B3 Exchange",
          broker_deal_code: "ABCB",
          side: "BUY",
          security_ticker: "DOLV20",
          order_size: "250,000,00",
          amount: "?",
          price_buy: "-",
          price_sell: "-",
          time_stamp: "7/29/2019 12:04",
        },
        {
          order_id: "12353",
          application_source: "RobotFX",
          status: "PARTIALLY FILLED",
          trading_venue: "B3 Exchange",
          broker_deal_code: "ABCB",
          side: "BUY",
          security_ticker: "DOLV20",
          order_size: "250,000,00",
          amount: "?",
          price_buy: "-",
          price_sell: "-",
          time_stamp: "7/29/2019 12:04",
        },
        {
          order_id: "12354",
          application_source: "RobotFX",
          status: "PARTIALLY FILLED",
          trading_venue: "B3 Exchange",
          broker_deal_code: "ABCB",
          side: "BUY",
          security_ticker: "DOLV20",
          order_size: "250,000,00",
          amount: "?",
          price_buy: "-",
          price_sell: "-",
          time_stamp: "7/29/2019 12:04",
        },
        {
          order_id: "12355",
          application_source: "RobotFX",
          status: "PARTIALLY FILLED",
          trading_venue: "B3 Exchange",
          broker_deal_code: "ABCB",
          side: "BUY",
          security_ticker: "DOLV20",
          order_size: "250,000,00",
          amount: "?",
          price_buy: "-",
          price_sell: "-",
          time_stamp: "7/29/2019 12:04",
        },
      ],
    };
  },
  methods: {
    customFilter(value, search, item) {
      return (
        item != null &&
        search != null &&
        item.dealcode
          .toLocaleLowerCase()
          .indexOf(search.toLocaleLowerCase()) !== -1
      );
    },
  },
  computed: {
    filteredItems() {
      if (this.FilterStatus === "ALL") {
        return this.list;
      }
      return this.list.filter((i) => i.status === this.FilterStatus);
    },
  },
};
</script>
