function isBusinessPage(){

  var returnVar = false;

  if($(".rn-brokerage-page").length > 0){

    returnVar = true;
  }

  if($(".rn-mortgage-page").length > 0){

    returnVar = true;
  }

  if($(".rn-franchising-page").length > 0){

    returnVar = true;
  }

  if($(".rn-insurance-page").length > 0){

    returnVar = true;
  }

  if($(".rn-settlement-page").length > 0){

    returnVar = true;
  }

  if($(".rn-relocation-page").length > 0){

    returnVar = true;
  }

  return returnVar;
}



// GLOBAL CONTACT FORM
// ------------------------------------------------------------------------
function openHsContact(){

  $(".rn-contact-modal-mask").css("display","block");
  $(".rn-hs-contact-modal").css("display","flex");

  var paddingTop = 20;

  $(".rn-hs-contact-modal").css("top", paddingTop + "px");
}

function closeHsContact(){

  
  $(".rn-contact-modal-mask").css("display","none");
  $(".rn-hs-contact-modal").css("display","none");


}

function siteHeaderNav(){

  var navMenu, 
      navMenuButton;

  navMenuButton = $('#rnSiteHeaderNavButton');
  navMenu = $('#rnSiteHeaderNavMenu');

  navMenuButton.on('click', function(e) {

    navMenuButton.toggleClass('is-active');
    navMenu.slideToggle();
    e.preventDefault();
  });

  if(isBusinessPage()){

    // If on business page, show business nav expanded in mobile nav
    $("#rnNavBusinesses").addClass("is-active");
  }

  // toggle mobile business nav
  $("#rnNavBusinessesBtn").on("click",function(e){

    $("#rnNavBusinesses").toggleClass('is-active');

    e.preventDefault();
  });



  // Make the whole business nav item clickable
  $("#rnNavBusinesses .rn-business-btn-wrapper").on("click",function(event){

    var url = $(this).find(".rn-wrapper a").attr("href");

    document.location.href = url;
    //window.open(url, "_blank");
  });
}


function siteGlobal(){

  siteHeaderNav();

  // ----- ENCODE EMAIL FOR INFO ------

  // Email obfuscator script 2.1 by Tim Williams, University of Arizona
  // Random encryption key feature by Andrew Moulden, Site Engineering Ltd
  // This code is freeware provided these four comment lines remain intact
  // A wizard to generate this code is at http://www.jottings.com/obfuscator/
  var coded = "TxC2@L24FgFqVTXFg.X24";
  var key = "XYDAe1CG9zn20g5hNiRHMdlPmFI6BSJx8W3vLrTwkcE7O4afQKyuoUsZVbqpjt";
  var shift = coded.length;
  var link="";

  for (i=0; i<coded.length; i++) {
    if (key.indexOf(coded.charAt(i))==-1) {
      ltr = coded.charAt(i)
      link += (ltr)
    }
    else {     
      ltr = (key.indexOf(coded.charAt(i))-shift+key.length) % key.length
      link += (key.charAt(ltr))
    }
  }

  // ----------

  // Top header info email
  $(".rn-info-email-parent").append("<a title='Send an email to HomeServices of America' href='mailto:" + link + "' class='rn-email-icon'><i class='rni-mail-fill' aria-hidden='true'></i>" + link + "</a>");

  // Nav info email - this is also used on insurance page
  $(".rn-navinfo-email-parent").append("<a title='Send an email to HomeServices of America' href='mailto:" + link + "'>" + link + "</a></div>");
  
  // adding icons to mobile nav
  $(".rn-mobile-contact .rn-navinfo-email-parent a:last-child").prepend("<i class='rni-mail-fill' aria-hidden='true'></i>");

  // CMS strips out javascript in href, so adding here

  $(".rn-contact-form-btn").on("click", function(event){

    event.preventDefault();

    openHsContact();
  });



  // Contact Forms

  // Close contact when modal background is clicked
  $(".rn-hs.rn-contact-modal-mask").on("click", function(event){

    closeHsContact();
  });

  $("#rnHsContact .button").on("click", function(event){

    event.preventDefault();
    
    var subject = $("#rnHsContact").data("subject");
    

    // ----- ENCODE EMAIL FOR CONTACT (LIZ) ------
    //var coded = "ADeADYDb@rlVswsj8DTsw.TlV";
    //var key = "4kiINzfFLcrAXYvqm1wunEQoCgODG0eMy6Tjd3p8RVZ7KbUhl2t9xJHsWaBP5S";

    // INFO

    // Email obfuscator script 2.1 by Tim Williams, University of Arizona
    // Random encryption key feature by Andrew Moulden, Site Engineering Ltd
    // This code is freeware provided these four comment lines remain intact
    // A wizard to generate this code is at http://www.jottings.com/obfuscator/
    var coded = "TxC2@L24FgFqVTXFg.X24";
    var key = "XYDAe1CG9zn20g5hNiRHMdlPmFI6BSJx8W3vLrTwkcE7O4afQKyuoUsZVbqpjt";
    var shift=coded.length;
    var toEmail ="";

    for (i=0; i<coded.length; i++) {

        if (key.indexOf(coded.charAt(i))==-1) {
          ltr = coded.charAt(i)
          toEmail += (ltr)
        }
        else {     
          ltr = (key.indexOf(coded.charAt(i))-shift+key.length) % key.length
          toEmail += (key.charAt(ltr))
        }
    }

    
    
    // ------------

    // First Name
    var firstNameLabel = $("label[for='first_name']").html();
    var firstName = document.getElementById("rnFormFirstName").value;

    // Last Name
    var lastNameLabel = $("label[for='last_name']").html();
    var lastName = document.getElementById("rnFormLastName").value;

    // Company Name
    var companyNameLabel = $("label[for='company_name']").html();
    var companyName = document.getElementById("rnFormCompany").value;

    // Business Address
    var businessAddressLabel = $("label[for='business_address']").html();
    var businessAddress = document.getElementById("rnFormBusinessAddress").value;

    // City
    var cityLabel = $("label[for='city']").html();
    var city = document.getElementById("rnFormCity").value;

    // State
    var stateLabel = $("label[for='state']").html();
    var state = document.getElementById("rnFormState").value;

    // Zip
    var zipLabel = $("label[for='zip']").html();
    var zip = document.getElementById("rnFormZip").value;

    // Phone
    var phoneLabel = $("label[for='phone']").html();
    var phone = document.getElementById("rnFormPhone").value;

    // Email
    var emailLabel = $("label[for='user_email']").html();
    var email = document.getElementById("rnFormEmail").value;

    // Are you a franchise?
    var franchiseLabel = $("label[for='franchise']").html();
    var franchise = $('input[name="franchise"]:checked').val();

    // Which brand
    var brandLabel = $("label[for='brand']").html();
    var brand = document.getElementById("rnFormBrand").value;

    // How can we help you?
    var helpLabel = $("label[for='help']").html();
    var help = document.getElementById("rnFormHelp").value;

    if($(".rn-franchising-page").length > 0){

      document.location.href = "mailto:" + toEmail + "?subject="
          + encodeURIComponent(subject)
          + "&body="+encodeURIComponent(firstNameLabel) + "%20"
          + encodeURIComponent(firstName) + "%0D%0A"
          + encodeURIComponent(lastNameLabel) + "%20"
          + encodeURIComponent(lastName) + "%0D%0A"
          + encodeURIComponent(emailLabel) + "%20"
          + encodeURIComponent(email) + "%0D%0A"
          + encodeURIComponent(franchiseLabel) + "%20"
          + encodeURIComponent(franchise) + "%0D%0A"
          + encodeURIComponent(brandLabel) + "%20"
          + encodeURIComponent(brand) + "%0D%0A"
          + encodeURIComponent(helpLabel) + "%20"
          + encodeURIComponent(help) + "%0D%0A";

    }else{

      document.location.href = "mailto:" + toEmail + "?subject="
          + encodeURIComponent(subject)
          + "&body="+encodeURIComponent(firstNameLabel) + "%20"
          + encodeURIComponent(firstName) + "%0D%0A"
          + encodeURIComponent(lastNameLabel) + "%20"
          + encodeURIComponent(lastName) + "%0D%0A"
          + encodeURIComponent(companyNameLabel) + "%20"
          + encodeURIComponent(companyName) + "%0D%0A"
          + encodeURIComponent(businessAddressLabel) + "%20"
          + encodeURIComponent(businessAddress) + "%0D%0A"
          + encodeURIComponent(cityLabel) + "%20"
          + encodeURIComponent(city) + "%0D%0A"
          + encodeURIComponent(stateLabel) + "%20"
          + encodeURIComponent(state) + "%0D%0A"
          + encodeURIComponent(zipLabel) + "%20"
          + encodeURIComponent(zip) + "%0D%0A"
          + encodeURIComponent(phoneLabel) + "%20"
          + encodeURIComponent(phone) + "%0D%0A"
          + encodeURIComponent(emailLabel) + "%20"
          + encodeURIComponent(email) + "%0D%0A"
          + encodeURIComponent(franchiseLabel) + "%20"
          + encodeURIComponent(franchise) + "%0D%0A"
          + encodeURIComponent(brandLabel) + "%20"
          + encodeURIComponent(brand) + "%0D%0A"
          + encodeURIComponent(helpLabel) + "%20"
          + encodeURIComponent(help) + "%0D%0A";

    }

    document.getElementById("rnHsContact").reset();

    closeHsContact();

  });


}

function siteHomeScroll() {

  // Anchor link for main button
  $("#rnHomeLeadBtn a").on("click", function(event){

      event.preventDefault();

      var target = $(this).data('target');

      $('html, body').animate({scrollTop: $("." + target).offset().top}, 600);

    });
}

function siteHomeCallout(){

  // For businesses on home page, make whole square clickable
  $(".rn-home-companies .rn-business").on("click",function(event){

    var url = $(this).find(".rn-business-btn").attr("href");

    document.location.href = url;

  });
}

function siteHomeBlog2(){

  $.ajax({

      url: "https://blog.homeservices.com/wp-json/wp/v2/posts?_embed&per_page=2",
      success: function(data) {
        
        var blogContainer = "<div id='rnHomeBlogContainer' class='feed-container'></div>";

        $('#rnBlog').append(blogContainer);

        $(data).each(function(k, v) {
            
          var blogPosts, d, date, day, days, err, excerpt, img, link, month, monthname, months, title, weekday, year;
          if (v) {
            excerpt = v.excerpt.rendered;
            title = v.title.rendered;
            link = v.link;
            
            blogPosts = "<div class='rn-home-blog-post'><a target='blank' class='rn-button' href='" + link + "' title=''><div class='rn-blog-title'>" + title + "</div> <div class='rn-blog-arrow'><i class='rn-icon-angle-right-medium'></i></div></a></div>";
       

            $('#rnHomeBlogContainer').append(blogPosts);
          } else {
            return;
          }
        });
      },
      cache: false
    });
}

function siteSubMapGrid(){

  //copy divs containing logos and put in the rn-map div

  $(".rn-locations .rn-logos .rn-map-location").clone().appendTo(".rn-map");

  $( ".rn-map .rn-map-location" ).each(function( index ) {

    var x = $( this ).data("x");
    var y = $( this ).data("y");

    if(x == 0 && y == 0){

      $(this).css("display","none");
    }

    var xPercent = (x/940) * 100;
    var yPercent = (y/590) * 100;

    $(this).css("top",yPercent+"%");
    $(this).css("left",xPercent+"%");

    // remove text - not needed for red dot hover
    $(this).find(".rn-logo-info h4").remove();
    $(this).find(".rn-logo-info p").remove();

    // If dot is grouped - only 1 group for now
    if($(this).find(".rn-group-0").length > 0){

      // add red map dot with rn-dot-0 class
      $(this).append("<div class='rn-map-dot rn-dot-0'></div>");

      // add group of logos
      //var $groupDiv = $(this).find(".rn-group-0");

      //$(this).find(".rn-logo").addClass("rn-logo-group");

      // Add the arrow that is part of the pop up box on red dot hover - add left to make room
      $(this).find(".rn-logo").prepend("<div class='rn-arrow left'></div>");

    }else if($(this).find(".rn-group-brokerage").length > 0){

        // add red map dot with rn-dot-0 class
      $(this).append("<div class='rn-map-dot rn-dot-0'></div>");

      // add group of logos
      //var $groupDiv = $(this).find(".rn-group-0");

      //$(this).find(".rn-logo").addClass("rn-logo-group");

      // Add the arrow that is part of the pop up box on red dot hover - add left to make room
      $(this).find(".rn-logo").prepend("<div class='rn-arrow'></div>");


    }else{

      // Add the arrow that is part of the pop up box on red dot hover
      $(this).find(".rn-logo").prepend("<div class='rn-arrow'></div>");

      // add red map dot
      $(this).append("<div class='rn-map-dot'></div>");
    }

    

  });

  // removing here with js instead of css because the grid lines use nth(x)
  $(".rn-no-grid").remove();


  $(".rn-map-location").on("click",function(event){

    var url = $(this).find(".rn-logo-info a").attr("href");

    //document.location.href = url;
      window.open(url, "_blank", 'noopener');
  });


  $(".rn-mortgage-lender").on("click",function(event){

    var url = $(this).find(".rn-box-reveal a").attr("href");

    //document.location.href = url;
    window.open(url, "_blank");
  });


  // Mobile State dropdown
  $("#rnStateDropdown").on("change", function(event){

    var state = $(this).val();

    // turn off all logos
    $(".rn-logos >li").css("display","none");

    // turn on logos for state selected
    $(".rn-logos ."+state).css("display","flex");
  });

  // For grouped dots, show multiple dots selected when rolling over one
  $(".rn-dot-0").on("mouseover", function(event){

    $(".rn-dot-0").addClass("rn-map-dot-hover");
  });

  // For grouped dots, rollout
  $(".rn-dot-0").on("mouseout", function(event){

    $(".rn-dot-0").removeClass("rn-map-dot-hover");
  });
}

function initInsuranceCarriersSlider(){

  

    $('.rn-insurance-page #rnSlickSlider').slick({
        
        autoplay: true,
        autoplaySpeed: 500000,
        speed: 300,
        arrows: true,
        slidesToShow: 5,
        slidesToScroll: 1,
        dots: false,
        infinite: true,
        cssEase: 'ease-out',
        responsive: [{

            breakpoint: 500,
            settings: { slidesToShow: 1}

          },{

            breakpoint: 600,
            settings: { slidesToShow: 2}

          },{

            breakpoint: 700,
            settings: { slidesToShow: 3}

          },{

            breakpoint: 800,
            settings: { slidesToShow: 4}

          }]

      });

  
}


function initRelocationTestimonialsSlider(){

 
  $('.rn-relocation-page #rnSlickSlider').slick({
        
        autoplay: true,
        autoplaySpeed: 500000,
        speed: 300,
        arrows: true,
        slidesToShow: 1,
        slidesToScroll: 1,
        dots: true,
        infinite: true,
        cssEase: 'ease-out'

  });
}

function siteSubPage(){

  siteSubMapGrid();

  initInsuranceCarriersSlider();

  $(".rn-franchising-page .rn-form-phone").prepend("<i class='rni-phone-fill' aria-hidden='true'></i>");

  // For non mobile, show the curve anchor link on rollover - used on about and careers page
  if (window.matchMedia('(min-width: ' + mobileBreakpoint + 'px)').matches)
  {

    $(".rn-down-arrow-container >ul >li").on("mouseover",function(event){

      $(".rn-down-arrow-container >ul >li").removeClass("rn-curve-on");
      $(".rn-down-arrow-container >ul >li").addClass("rn-curve-off");

      $(this).removeClass("rn-curve-off");
      $(this).addClass("rn-curve-on");
    });

    $(".rn-down-arrow-container >ul >li").on("mouseout",function(event){

      $(this).removeClass("rn-curve-on");
      $(this).addClass("rn-curve-off");

      $(".rn-down-arrow-container >ul >li:first-child").removeClass("rn-curve-off");
      $(".rn-down-arrow-container >ul >li:first-child").addClass("rn-curve-on");
    });

  }

    // sub page anchor buttons
    $(".rn-anchor-btn").on("click", function(event){

      event.preventDefault();

      var target = $(this).data('target');

      $('html, body').animate({scrollTop: $("." + target).offset().top}, 600);

    });


    var firstNameLabel = "First Name";
  var lastNameLabel = "Last Name";

  $("#rnSubFormFirstName").attr("placeholder", firstNameLabel);
  $("#rnSubFormLastName").attr("placeholder", lastNameLabel);

  $("#rnSubForm .button").on("click", function(event){

    event.preventDefault();

    
    
    // Interested In
    var interestLabel = $('#rnSubFormInterest option:eq(0)').html();
    var interest = $('#rnSubFormInterest option:selected').html();

    // First Name
    //var firstNameLabel = $("label[for='first_name']").html();
    
    var firstName = document.getElementById("rnSubFormFirstName").value;

    // Last Name
    //var lastNameLabel = $("label[for='last_name']").html();
    
    var lastName = document.getElementById("rnSubFormLastName").value;

    // ----- ENCODE EMAIL FOR CONTACT (LIZ) ------
    //var coded = "ADeADYDb@rlVswsj8DTsw.TlV";
    //var key = "4kiINzfFLcrAXYvqm1wunEQoCgODG0eMy6Tjd3p8RVZ7KbUhl2t9xJHsWaBP5S";

    // INFO

    // Email obfuscator script 2.1 by Tim Williams, University of Arizona
    // Random encryption key feature by Andrew Moulden, Site Engineering Ltd
    // This code is freeware provided these four comment lines remain intact
    // A wizard to generate this code is at http://www.jottings.com/obfuscator/
    var coded = "TxC2@L24FgFqVTXFg.X24";
    var key = "XYDAe1CG9zn20g5hNiRHMdlPmFI6BSJx8W3vLrTwkcE7O4afQKyuoUsZVbqpjt";
    var shift=coded.length;
    var toEmail ="";

    for (i=0; i<coded.length; i++) {

        if (key.indexOf(coded.charAt(i))==-1) {
          ltr = coded.charAt(i)
          toEmail += (ltr)
        }
        else {     
          ltr = (key.indexOf(coded.charAt(i))-shift+key.length) % key.length
          toEmail += (key.charAt(ltr))
        }
    }


    // ----------

    var subject = interest + ": " + $("#rnSubForm").data("subject");

    document.location.href = "mailto:" + toEmail + "?subject="
        + encodeURIComponent(subject)
        + "&body="+encodeURIComponent(firstNameLabel) + ":%20"
        + encodeURIComponent(firstName) + "%0D%0A"
        + encodeURIComponent(lastNameLabel) + ":%20"
        + encodeURIComponent(lastName) + "%0D%0A"
    

    document.getElementById("rnSubForm").reset();

  });



  // On relocation page, hide paragraphs in the lead section, use clicks to show
  if (window.matchMedia('(max-width: ' + mobileBreakpoint + 'px)').matches)
  {
    $(".rn-relocation-page .rn-lead .rn-flex-item").css("cursor","pointer");
    $(".rn-relocation-page .rn-lead .rn-flex-item p").css("display","none");
    $(".rn-relocation-page .rn-lead .rn-flex-item a").css("display","none");

    $(".rn-relocation-page .rn-lead .rn-flex-item").on("click", function(event){

      
      $(".rn-relocation-page .rn-lead .rn-flex-item p").css("display","none");
      $(".rn-relocation-page .rn-lead .rn-flex-item a").css("display","none");

      $(this).find("p").css("display","block");
      $(this).find("a").css("display","block");
    });

  }

  initRelocationTestimonialsSlider();

}




function homePageLoad() {

  siteGlobal();

  // Load home page on both cms site editor and live site
  if ($('.cms-site-home-page').length > 0 || $('.site-home-page').length > 0) {

    siteHomeScroll();

    siteHomeCallout();

    siteHomeBlog2();

  }else{

    siteSubPage();
  }
}

