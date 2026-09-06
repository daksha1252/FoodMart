<template>
  <section class="newsletter">
    <div class="newsletter__content">
      <div class="newsletter__text">
        <h2 class="newsletter__title">
          Get <span>25% Discount</span>
          <br />
          on your first
          <br />
          purchase
        </h2>

        <p class="newsletter__description">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Dictumst
          <br />
          amet, metus, sit massa posuere maecenas. At tellus ut nunc amet vel
          <br />
          egestas.
        </p>
      </div>

      <form class="newsletter__form">
        <div class="newsletter__field">
          <label for="name">Name</label>

          <input id="name" type="text" placeholder="Name" />
        </div>

        <div class="newsletter__field">
          <label for="email">Email</label>

          <input id="email" type="email" placeholder="abc@mail.com" />
        </div>

        <label class="newsletter__checkbox">
          <input type="checkbox" />
          <span>Subscribe to the newsletter</span>
        </label>

        <button type="submit" class="newsletter__button">Submit</button>
      </form>
    </div>
  </section>
</template>
