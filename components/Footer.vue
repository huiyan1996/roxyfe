<template>
    <div class="container-fluid p-5 footerWrapper">
        <b-row>
            <b-col sm="12" md="6">
                <div class="footerTitle">
                    <img class="footerLogo" src="~/assets/images/rose.png" alt="Logo">
                    <h6>ROSYFOXY</h6>
                </div>
                <div class="footerDescription">
                    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam at dignissim nunc, id maximus ex. Etiam nec dignissim elit, at dignissim enim. </p>
                </div>
            </b-col>
            <b-col sm="12" md="6">
                <b-row class="sitemaps">
                    <b-col cols="6" lg="4">
                        <ul>
                            <li><a href="#">About Us</a></li>
                            <li><a href="#">Product</a></li>
                            <li><a href="#">Terms & Condition</a></li>
                            <li><a href="#">Privacy Policy</a></li>
                        </ul>
                    </b-col>
                    <b-col>
                        <ul>
                            <li><a href="#">Shop</a></li>
                            <li><a href="#">Contact Us</a></li>
                            <li><a href="#">Help</a></li>
                        </ul>
                    </b-col>
                </b-row>
            </b-col>
        </b-row>
    </div>
</template>

<script>
export default {
  name: 'FooterSection',
  props: [],
  data() {
    return {
        sitemapList: [
            {
                title: 'About Us',
                hyperlink: '#'
            },
            {
                title: 'Product',
                hyperlink: '#'
            },
            {
                title: 'Terms & Condition',
                hyperlink: '#'
            },
            {
                title: 'Privacy Policy',
                hyperlink: '#'
            },
            {
                title: 'Shop',
                hyperlink: '#'
            },
            {
                title: 'Contact',
                hyperlink: '#'
            },
            {
                title: 'Help',
                hyperlink: '#'
            },
        ],
    }
  },
  methods: {
  },
  mounted() {
  }
}
</script>

<style lang="scss" scoped>
.footerWrapper {
    background-color: #E9E9EA;
    color: #4A4949;
    
    .footerTitle {
        height: 25px;
        display: flex;
        align-items: center;
        h6 {
            letter-spacing: 3px;
            margin-top: 5px;
        }
        .footerLogo {
            height: 100%;
            object-fit: contain;
            margin-right: 5px;
        }
    }

    .footerDescription {
        display: flex;
        width: 90%;
        margin-top: 15px;
    }

    .sitemaps {
        display: flex;
        width: 90%;

        ul {
            list-style: none;
            padding: 0px;

            li {
                a {
                    color: #4A4949;
                }
            }
        }
    }
}
</style>