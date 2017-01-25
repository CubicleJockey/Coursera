##### Rules

<pre>
Generic Rule Format:
--------------------
selector{
    property: value;
}

Generic Rule (Styled Heading):
------------------------------
h1{
    color: blue;
}
</pre>


#### Cascading Part Of CSS (Order)
* Browser default
* *External* style sheets
* *Internal* style (in the head section)
* *Inline* style (inside an HTML element)

#### Rule of precedence
* What if one selector is defined in two external files?
    * The rules from the most recent file have precedence
* What if one selector has more than one rule in the same file?
    * <pre>
        h1{
            color: green;
            font-family: Courier;
        }
        
        h1{
            font-family: Tahoma;
        }
        
       //This will make all h1 tags green and Tahoma.
    </pre>
    
    * The most recent rule has precedence
    
#### Prevent Overrides (Prevent Cascading)

* You can prevent later rules from taking precedent.
    * *!important*
    * <pre>
        h1{
            color: yellow;
            font-family: Courier !important;
        }
        
        h1{
            font-family: Times;
        }
        
        //This will make all h1 tags yellow and Courier no matter precendence.
    </pre>