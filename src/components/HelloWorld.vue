<template>
  <v-container>
    <v-row class="text-center">
      <v-col class="mb-4">
        <h1 class="display-2 font-weight-bold mb-3">Data Table</h1>
        <v-data-table
          dark
          dense
          :headers="headers"
          :items="data"
          :items-per-page="10"
          class="elevation-1"
        ></v-data-table>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "HelloWorld",

  data() {
    return {
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
      data: [
        {
          order_id: '1111',
          application_source: 'RobotFX',
          status: 'NEW ORDER',
          trading_venue: 'B3 Exchange',
          broker_deal_code: 'ABCB',
          side: 'BUY',
          security_ticker: 'DOLV20',
          order_size: '250,000,00',
          amount: '?',
          price_buy: '-',
          price_sell: '-',
          time_stamp: '7/29/2019 12:04',
        },
        {
          order_id: '1111',
          application_source: 'RobotFX',
          status: 'NEW ORDER',
          trading_venue: 'B3 Exchange',
          broker_deal_code: 'ABCB',
          side: 'BUY',
          security_ticker: 'DOLV20',
          order_size: '250,000,00',
          amount: '?',
          price_buy: '-',
          price_sell: '-',
          time_stamp: '7/29/2019 12:04',
        },
        {
          order_id: '1111',
          application_source: 'RobotFX',
          status: 'NEW ORDER',
          trading_venue: 'B3 Exchange',
          broker_deal_code: 'ABCB',
          side: 'BUY',
          security_ticker: 'DOLV20',
          order_size: '250,000,00',
          amount: '?',
          price_buy: '-',
          price_sell: '-',
          time_stamp: '7/29/2019 12:04',
        },
        {
          order_id: '1111',
          application_source: 'RobotFX',
          status: 'NEW ORDER',
          trading_venue: 'B3 Exchange',
          broker_deal_code: 'ABCB',
          side: 'BUY',
          security_ticker: 'DOLV20',
          order_size: '250,000,00',
          amount: '?',
          price_buy: '-',
          price_sell: '-',
          time_stamp: '7/29/2019 12:04',
        },
        {
          order_id: '1111',
          application_source: 'RobotFX',
          status: 'NEW ORDER',
          trading_venue: 'B3 Exchange',
          broker_deal_code: 'ABCB',
          side: 'BUY',
          security_ticker: 'DOLV20',
          order_size: '250,000,00',
          amount: '?',
          price_buy: '-',
          price_sell: '-',
          time_stamp: '7/29/2019 12:04',
        },
        {
          order_id: '1111',
          application_source: 'RobotFX',
          status: 'NEW ORDER',
          trading_venue: 'B3 Exchange',
          broker_deal_code: 'ABCB',
          side: 'BUY',
          security_ticker: 'DOLV20',
          order_size: '250,000,00',
          amount: '?',
          price_buy: '-',
          price_sell: '-',
          time_stamp: '7/29/2019 12:04',
        },
        {
          order_id: '1111',
          application_source: 'RobotFX',
          status: 'NEW ORDER',
          trading_venue: 'B3 Exchange',
          broker_deal_code: 'ABCB',
          side: 'BUY',
          security_ticker: 'DOLV20',
          order_size: '250,000,00',
          amount: '?',
          price_buy: '-',
          price_sell: '-',
          time_stamp: '7/29/2019 12:04',
        },
        {
          order_id: '1111',
          application_source: 'RobotFX',
          status: 'NEW ORDER',
          trading_venue: 'B3 Exchange',
          broker_deal_code: 'ABCB',
          side: 'BUY',
          security_ticker: 'DOLV20',
          order_size: '250,000,00',
          amount: '?',
          price_buy: '-',
          price_sell: '-',
          time_stamp: '7/29/2019 12:04',
        },
        {
          order_id: '1111',
          application_source: 'RobotFX',
          status: 'NEW ORDER',
          trading_venue: 'B3 Exchange',
          broker_deal_code: 'ABCB',
          side: 'BUY',
          security_ticker: 'DOLV20',
          order_size: '250,000,00',
          amount: '?',
          price_buy: '-',
          price_sell: '-',
          time_stamp: '7/29/2019 12:04',
        },
        {
          order_id: '1111',
          application_source: 'RobotFX',
          status: 'NEW ORDER',
          trading_venue: 'B3 Exchange',
          broker_deal_code: 'ABCB',
          side: 'BUY',
          security_ticker: 'DOLV20',
          order_size: '250,000,00',
          amount: '?',
          price_buy: '-',
          price_sell: '-',
          time_stamp: '7/29/2019 12:04',
        },
      ],
    };
  },
};
</script>
