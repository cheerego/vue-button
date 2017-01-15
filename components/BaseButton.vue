<script>
  export default{
    name: 'base-button',
    props: [],

    render(createElement) {
      return createElement(
        'a',
        {
          class: ['button', 'ripple'],
          on: {
            click: this.click
          }
        },
        this.$slots.default
      )
    },
    methods: {
      click(){
        this.$emit('click')
      }
    }
  };
</script>
<style scoped>
  a.button {
    display: inline-block;
    line-height: 1;
    text-align: center;
    white-space: nowrap;
    cursor: pointer;
    user-select: none;
    border: none;
    border-radius: 2px;
    position: relative;
    padding: 8px 30px;
    margin: 10px 1px;
    font-size: 14px;
    font-weight: 500;
    text-transform: uppercase;
    letter-spacing: 0;
    will-change: box-shadow, transform;
    transition: box-shadow 0.2s cubic-bezier(0.4, 0, 1, 1), background-color 0.2s cubic-bezier(0.4, 0, 0.2, 1), color 0.2s cubic-bezier(0.4, 0, 0.2, 1);
    text-decoration: none;
    background: transparent;
    background-color: #EEEEEE;
    color: rgba(0, 0, 0, 0.87);
  }

  a.button:active {
    box-shadow: 0 4px 5px 0 rgba(0, 0, 0, 0.14), 0 1px 10px 0 rgba(0, 0, 0, 0.12), 0 2px 4px -1px rgba(0, 0, 0, 0.2);
  }

  a.button.default {
    background-color: #EEEEEE;
    color: rgba(0, 0, 0, 0.87);
  }

  a.button.primary {
    background-color: #009688;
    color: rgba(255, 255, 255, 0.84);
  }

  a.button.success {
    background-color: #4caf50;
    color: rgba(255, 255, 255, 0.84);
  }

  a.button.info {
    background-color: #03a9f4;
    color: rgba(255, 255, 255, 0.84);
  }

  a.button.warning {
    background-color: #ff5722;
    color: rgba(255, 255, 255, 0.84);
  }

  a.button.danger {
    background-color: #f44336;
    color: rgba(255,255,255, 0.84);
  }

  .ripple {
    position: relative;
    overflow: hidden
  }
/**/
  .ripple:after {
    content: "";
    display: block;
    position: absolute;
    width: 100%;
    height: 100%;
    top: 0;
    left: 0;
    pointer-events: none;
    background-image: radial-gradient(circle, #000 10%, transparent 10.01%);
    background-repeat: no-repeat;
    background-position: 50%;
    transform: scale(10, 10);
    opacity: 0;
    transition: transform .5s, opacity 1s
  }

  .ripple:active:after {
    transform: scale(0, 0);
    opacity: .2;
    transition: 0s
  }
</style>
