# app2
Basic App that displays an image and two buttons under the image.
And giving app internet permissions.

when you click on the 1st button you will see a message
and
when you click on the 2nd button you will redirected into another website.

Learning : Explict and Implicit intents in Android Studio 


code:

     val buttonwishlist=findViewById<Button>(R.id.button)

        buttonwishlist.setOnClickListener {
            Toast.makeText(applicationContext, "Added to wishlist", Toast.LENGTH_SHORT).show()

        }

        //implict functions

        val webbutton=findViewById<CardView>(R.id.web)

        webbutton.setOnClickListener {
            val intent=Intent(Intent.ACTION_VIEW)
            intent.data= Uri.parse("https://www2.hm.com/en_in/productpage.1124657002.html")
            startActivity(intent)
        }
