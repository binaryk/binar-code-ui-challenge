<template>
  <div class="body">
    <div class="header">LEGACY</div>
    <div class="content">
      <div class="left-side">
        <div class="order-info"> 
          <div class="order-customer">Hi
            <div class="bold-john">John!</div>
            <br>Your order is in transit
          </div>
          <div class="order-date">
            <div class="delivery-date">Delivery Date</div>
            <div class="date-month">JUN</div>
            <div class="date-day">16</div>
            <div class="time">4:00 - 7:00 PM</div>
          </div>
          <div class="order-address">
            <div class="address-image">
              <img
                src="https://dashboard.givelegacy.com/img/thanks-review/ion-location%20-%20Ionicons@3x.png"
              >
            </div>
            <div class="order-address-text">
              <div class="shipping-address">SHIPPING ADDRESS:</div>
              <div class="shipping-address-text">166 CENTRAL AVENUE
                <br>APT #1A, NY, 11221
              </div>
            </div>
          </div>
        </div>
        <div class="order-status">
          <div class="status-title">ORDER STATUS</div>
          <div class="order-way-1">
            <div class="image-status">
              <img src="https://dashboard.givelegacy.com/img/thanks-review/checked.png">
              <img
                height="40"
                class="full-line"
                src="https://dashboard.givelegacy.com/img/thanks-review/full-line.png"
              >
            </div>
            <div class="order-way-text">Order Confirmed
              <div class="order-way-text-small">Mon, Jun 19th, 4:33 PM</div>
            </div>
          </div>
          <div class="order-way-1">
            <div class="image-status">
              <img src="https://dashboard.givelegacy.com/img/thanks-review/unchecked.png">
              <img
                class="full-line"
                height="40"
                src="https://dashboard.givelegacy.com/img/thanks-review/dotted-line@2x.png"
              >
            </div>
            <div class="order-way-text">Kit on the way
              <div class="order-way-text-small">Mon, Jun 19th, 6:21 PM</div>
            </div>
          </div>
          <div class="order-way-1">
            <div class="image-status">
              <img src="https://dashboard.givelegacy.com/img/thanks-review/unchecked.png">
              <img
                class="full-line"
                height="40"
                src="https://dashboard.givelegacy.com/img/thanks-review/dotted-line@2x.png"
              >
            </div>
            <div class="order-way-text">Kit delivered to you
              <div class="order-way-text-small">Mon, Jun 19th, 6:21 PM</div>
            </div>
          </div>
          <div class="order-way-1">
            <div class="image-status">
              <img src="https://dashboard.givelegacy.com/img/thanks-review/unchecked.png">
              <img
                class="full-line"
                height="40"
                src="https://dashboard.givelegacy.com/img/thanks-review/dotted-line@2x.png"
              >
            </div>
            <div class="order-way-text">Kit on the way back
              <div class="order-way-text-small">Mon, Jun 19th, 6:21 PM</div>
            </div>
          </div>
          <div class="order-way-1">
            <div class="image-status">
              <img src="https://dashboard.givelegacy.com/img/thanks-review/unchecked.png">
              <img
                class="full-line"
                height="40"
                src="https://dashboard.givelegacy.com/img/thanks-review/full-line.png"
              >
            </div>
            <div class="order-way-text">Kit received
              <div class="order-way-text-small">Mon, Jun 19th, 6:21 PM</div>
            </div>
          </div>
          <div class="order-way-1">
            <div class="image-status">
              <img src="https://dashboard.givelegacy.com/img/thanks-review/checked.png">
            </div>
            <div class="order-way-text">Results ready
              <div class="order-way-text-small">Mon, Jun 19th, 6:21 PM</div>
            </div>
          </div>
        </div>
        <div class="divider">
          <img
            class="divider-object"
            src="https://dashboard.givelegacy.com/img/thanks-review/long-line.png"
          >
        </div>
        <div class="client-id">
          <div class="client-id-image">
            <img
              width="32"
              src="https://dashboard.givelegacy.com/img/thanks-review/user%20-%20FontAwesome@3x.png"
            >
          </div>
          <div class="client-id-text">
            Client ID
            NF765678767876
          </div>
        </div>
        <div class="client-id">
          <div class="client-id-image">
            <img
              width="32"
              src="https://dashboard.givelegacy.com/img/thanks-review/local_phone%20-%20material@3x.png"
            >
          </div>
          <div class="client-id-text">ADVISOR PHONE
            <br>0-967-754-553-45
          </div>
        </div>
      </div>
      <div class="right-side">
        <div class="map-image">
          <img
            class="icon-image-shipping"
            src="https://files.slack.com/files-pri/TBTTBCTGE-FPT1TGYRW/screenshot_2019-10-25_at_13.29.45.png"
          >
        </div>
      </div>
    </div>
    <div class="footer">
      <div class="footer-icons">
        <img
          class="icon-image"
          src="https://dashboard.givelegacy.com/img/thanks-review/facebook%20-%20FontAwesome.svg"
        >
        <img
          class="icon-image"
          src="https://dashboard.givelegacy.com/img/thanks-review/instagram%20-%20FontAwesome.svg"
        >
        <img
          class="icon-image"
          src="https://dashboard.givelegacy.com/img/thanks-review/social-twitter%20-%20simple-line-icons.svg"
        >
        <img
          class="icon-image"
          src="https://dashboard.givelegacy.com/img/thanks-review/linkedin%20-%20FontAwesome.svg"
        >
        <div class="footer-text">Privacy. Quality. Security</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.body {
  display: flex;
  flex-direction: column;
  background-color: rgba(209, 215, 228, 0.72);
}

.header {
  display: flex;
  justify-content: center;
  font-size: 1.8em;
}

.content {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  background-color: #141e33;
  color: rgba(209, 215, 228, 0.72);
  margin: 70px;
  margin-bottom: 15px;
  margin-top: 30px;
  padding: 10px;
  border-radius: 10px;
  box-shadow: 3px 3px 5px 0px rgba(0, 0, 0, 0.09);
}

.left-side {
  display: flex;
  flex-wrap: wrap;
}

.right-side {
}

.order-info {
  display: flex;
  flex-direction: column;
  margin: 30px;
  margin-left: 10px;
}

.order-customer {
    display: flex;
    flex-direction: column;
    align-items: flex-start;  
    color: white;
    margin: 10px;
    margin-bottom: 25px;
}

.order-date {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
    }

.delivery-date {
  font-weight: bold;
}

.date-month {
  font-size: 83px;
  color: white;
  font-weight: bold;
  margin-bottom: -20px;
}

.date-day {
  font-size: 83px;
  color: white;
  font-weight: bold;
  margin-left: 5px;
}

.time {
  font-size: 20px;
  color: white;
  margin-left: 5px;
}

.order-address {
  margin-top: 50px;
  font-size: 14px;
  width: 250px;
}

.address-image {
  float: left;
  margin-left: 10px;
  margin-right: 10px;
}

.order-address-text {
}

.order-status {
  display: flex;
  flex-direction: column;
  margin-top: 30px;
  font-size: 12px;
}

.status-title {
  margin-top: 10px;
  font-weight: bold;
}

.order-way-1 {
  display: flex;
  margin-top: 10px;
}

.full-line {
  margin-top: 5px;
  align-self: center;
}

.order-way-text {
  float: right;
  margin-left: 10px;
  color: white;
  font-weight: 500;
}

.order-way-text-small {
  font-weight: normal;
  color: rgba(209, 215, 228, 0.72);
  font-size: 9px;
}

.image-status {
  display: flex;
  flex-direction: column;
  align-items: baseline;
}

.client-id {
  display: flex;
  margin: 10px;
  font-size: 14px;
  width: 200px;
  margin-top: 40px;
}

.client-id-image {
  float: left;
  margin: 8px;
}

.client-id-text {
}

.divider {
  width: 100%;
  margin-left: 15px;
}

.divider-object {
  width: -webkit-fill-available;
  height: 2.95px;
}

.map-image {
  margin: 15px;
}

.footer {
  display: flex;
  flex-direction: column;
}

.footer .footer-icons {
  padding: 15px;
  margin-left: auto;
  margin-right: auto;
  margin-bottom: 15px;
}

.footer-text {
  font-size: 13px;
}

.icon-image {
  margin: 8px;
}

.icon-image-shipping {
  border-radius: 2%;
}

.bold-john {
  font-weight: bold;
  display: contents;
}

.shipping-address {
  font-weight: bold;
  font-size: 14px;
}

.shipping-address-text {
  color: white;
  font-size: 12px;
}

@media only screen and (max-width: 768px) {
  .content {
    flex-direction: column;
    margin: 0;
    margin-top: 25px;
    padding: 0;
  }
  .left-side {
    flex-direction: column;
  }
  .icon-image-shipping {
    width: 100%;
  }
  .order-info {
    margin: 0;
    width: 100%;
    align-items: center;
  }
  .order-status {
    margin: auto;
    margin-bottom: 20px;
  }
  .order-way-1 {
    flex-direction: column-reverse;
    width: 150px;
  }
  .order-way-text {
    margin: auto;
  }
  .image-status {
    align-items: center;
  }
  .client-id {
    margin: auto;
  }
  .map-image {
    margin: 0;
    margin-bottom: -5px;
  }
  .order-customer {
    margin: 25px;
  }
}

@media (min-width: 768px) and (max-width: 1281px) {
  .icon-image-shipping {
    /* display: none; */
    width: 100%;
  }
}

@media (max-width: 1281px) {
  .divider {
    display: none;
  }
}
</style>
