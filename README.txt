Note, week 4 is a copy of nucampsiteWk3, not nucampsiteWk3InClassAssnmt.

The ...InClassAssnmt contains code that links the Reserve Campsite button to a form, whereas the nucampsiteWk3 does not.



    <script>
        /*  This is the jquery code for a separate pause and separate play button.
        $(function() {
            $(".carousel").carousel( { interval: 2000 } );
            $("#carouselPause").click(function(){
                $(".carousel").carousel("pause");
            });
            $("#carouselPlay").click(function(){
                $(".carousel").carousel("cycle");
            });
        });
        */
        
        /* This is the jquery code for a single button that toggles between play and         
        pause. */
        $(function() {
            $(".carousel").carousel( { interval: 200 } );
            $("#carouselButton").click(function(){
                if ($("#carouselButton").children("i").hasClass("fa-pause")) {
                    $(".carousel").carousel("pause");
                    $("#carouselButton").children("i").removeClass("fa-pause");
                    $("#carouselButton").children("i").addClass("fa-play");
                } else {
                    $(".carousel").carousel("cycle");
                    $("#carouselButton").children("i").removeClass("fa-play");
                    $("#carouselButton").children("i").addClass("fa-pause"); 
                }
            });
        });   
    </script>



<!-- These are the play and pause buttons side by side 
                        <div class="btn-group" id="carouselButton">
                            <button class="btn btn-danger btn-sm" id="carouselPause">
                                <i class="fa fa-pause"></i>
                            </button>
                            <button class="btn btn-danger btn-sm" id="carouselPlay">
                                <i class="fa fa-play"></i>
                            </button>
                        </div>
                        -->
                        
                        <!-- This is a single button that can toggle between play and pause -->
                        <button class="btn btn-danger btn-sm" id="carouselButton">
                            <i class="fa fa-pause"></i>
                        </button>

>>>Note the id="carouselButton" in the html linked to the jquery (and it also links to CSS).