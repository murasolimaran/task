<!DOCTYPE html>
<html lang="en" xmlns="http://www.w3.org/1999/xhtml">
<head>

    <meta charset="utf-8">
    <title>Sample</title>
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.16.0/umd/popper.min.js"></script>
    <script src="https://maxcdn.bootstrapcdn.com/bootstrap/4.5.2/js/bootstrap.min.js"></script>
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.3.1/jquery.min.js"></script>

    <style>
        a.nav-link { text-transform: uppercase; }
        .wrapper { background-image: url(https://img.techpowerup.org/200821/banner.jpg); background-color: #cccccc; height: 500px; background-position: center; background-repeat: no-repeat; background-size: cover; }
        *, ::after, ::before { box-sizing: border-box; }
        .transparent { background: transparent; }
        ul.navbar-nav a.nav-link { font-weight: 500; }
        .img-box { position: relative; }
        .row.Request-form p { color: red; }

            .img-box .details { border-radius: 0 0 5px 5px; bottom: 0; left: 0; position: absolute; right: 0; text-align: center; background-color: #3f78e3; color: #f3f3f3; padding: 2px 0px; }
            .img-box.style2 { background-color: #ffffff; border-radius: 5px; margin: 0; padding: 15px 25px 54px; position: relative; box-shadow: 1px 5px 45px -15px rgba(0, 0, 0, 0.5); }

        .owl-next, .owl-prev { font-size: 14px; margin: 5px; padding: 4px 7px; display: inline-block; cursor: pointer; border-radius: 3px; border: 1px solid; width: 30px; text-align: center; color: #3f78e3; }
        .icon-box .icon { border-radius: 50%; display: inline-block; height: 75px; line-height: 83px; text-align: center; width: 75px; box-shadow: 1px 1px 11px 2px rgba(55, 100, 235, 0.1); background-color: white; }
            .icon-box .icon span { font-size: 30px; }
        .bg-whitef { background-color: #f7f7f7; }
        button.btn.btn-white { background-color: white; }
        h3:hover { color: #3f78e3; }
        h5:hover { color: #3f78e3; }

        .fa:hover { color: #3f78e3; }
        a.ourlink { color: #3a3737; text-decoration: underline; }
        .Request-form .form-control { border-bottom: 1px solid gray; border-right: 0; border-left: 0; border-top: 0; border-radius: 0; }
        textarea.form-control { height: 45px; }
        ul.social_icons li { padding: 0; display: inline-block; text-align: center; border-radius: 50%; background-color: white; }
        ul.social_icons { padding: 0; }
            ul.social_icons li a { font-size: 16px; height: 35px; line-height: 35px; width: 35px; }
        .latest p { margin-bottom: 0px; }
        ul.importen-link { padding: 0px; }
            ul.importen-link li a { color: gray; font-weight: bold; }
            ul.importen-link li { list-style: none; }
            ul.importen-link li { list-style: none; padding-bottom: 4px; }


        @media screen and (min-width:768px) {
            ul.navbar-nav { margin: auto; }
            .we_are_experts { padding-right: 60px; }
            .img-box.style2 .details2 h5 { font-size: 25px; line-height: 30px; color: #3f78e3; }
            .text-block { position: absolute; bottom: 100px; left: 115px; }
            .bg-pd { padding: 50px 0; }
            .ml-90 { margin-left: 90px; }
            .support_box.text-center { border-radius: 10px; padding: 30px 20px; position: relative; -webkit-box-shadow: 1px 1px 11px 0px rgba(55, 100, 235, 0.05); box-shadow: 1px 1px 11px 0px rgba(55, 100, 235, 0.05); }
        }

        @media screen and (max-width:767px) {
            .img-box.style2 .details2 h5 { font-size: 21px; line-height: 30px; color: #3f78e3; }
            .text-block { position: absolute; bottom: 170px; left: 30px; }
            .wrapper.position-relative h1 { font-size: 28px; }
            .text-left h2 { font-size: 28px; text-align: center; }
            .icon-box .text-left { text-align: center !important; }
            .icon-box { text-align: center; }
                .icon-box h3 { font-size: 22px; padding: 5px; }
            .bg-pd { padding: 20px 0; }
                .bg-pd h3 { text-align: center; font-size: 20px; }
            .ml-90 { text-align: left; margin-left: 90px; }
            .support_box.text-center { border-radius: 10px; padding: 0px; position: relative; -webkit-box-shadow: 1px 1px 11px 0px rgba(55, 100, 235, 0.05); box-shadow: 1px 1px 11px 0px rgba(55, 100, 235, 0.05); }
            .container h4, h3 { font-size: 20px; }
            div#collapsibleNavbar { background-color: #fffffff0; z-index: 10; }
        }

        @media screen and (min-width:768px) and (max-width:1024px) {
        }
    </style>
    <script type="text/javascript">
        $(document).on('click', '#FormSubmit', function () {
        //$('#FormSubmit').click(function () {
            debugger;
            $('.Forvalidation').each(function () {
                var data = $(this).val();
                var name = $(this).attr('name')
                var pattern = /^\b[A-Z0-9._%-]+@[A-Z0-9.-]+\.[A-Z]{2,4}\b$/i
                if (name != 'email') {
                    if (data == "") {
                        $(this).css('border-color', 'red');
                        $(this).parent().find('p').removeAttr('style');
                    }
                    else {
                        $(this).css('border-color', '');
                        $(this).parent().find('p').attr('style', 'display:none');
                    }
                } else {
                    if (!pattern.test(data) && name == 'email') {
                        $(this).css('border-color', 'red');
                        if (data == "") {
                            $(this).parent().find('p').removeAttr('style');
                        } else {
                            $(this).parent().find('b').removeAttr('style');
                        }
                    }
                    else {
                        $(this).css('border-color', '');
                        $(this).parent().find('p').attr('style', 'display:none');
                        $(this).parent().find('b').attr('style', 'display:none');
                    }
                }

            })
            var data1 = $('#investementconsultency option:selected').val();
            if (data1 == "-1") {
                $('#investementconsultency').css('border-color', 'red');
                $('.errormsgforinvest').find('p').removeAttr('style');
            } else {
                $('#investementconsultency').css('border-color', '');
                $('.errormsgforinvest').find('p').attr('style', 'display:none');
            }
        });
        $(document).on('mouseleave', '.Forvalidation', function () {
            var data = $(this).val();
           
            if (data != '' && name != 'email') {
                $(this).css('border-color', '');
                $(this).parent().find('p').attr('style', 'display:none');
            }
           
        });
    </script>

</head>
<body>
    <div class="wrapper position-relative">

        <header class="header-nav transparent navbar-scrolltofixed menu-one">
            <nav class="navbar navbar-expand-md navbar-inverse navbar-fixed-top">
                <div class="container">
                    <a class="navbar-brand" href="#"><h4><b>BizRoot</b></h4></a>
                    <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#collapsibleNavbar">
                        <span class="fa fa-bars"></span>
                    </button>
                    <div class="collapse navbar-collapse" id="collapsibleNavbar">
                        <ul class="navbar-nav">
                            <li class="nav-item">
                                <a class="nav-link" href="#">Home</a>
                            </li>
                            <li class="nav-item">
                                <a class="nav-link" href="#">About us</a>
                            </li>
                            <li class="nav-item">
                                <a class="nav-link" href="#">page</a>
                            </li>
                            <li class="nav-item">
                                <a class="nav-link" href="#">service</a>
                            </li>
                            <li class="nav-item">
                                <a class="nav-link" href="#">blog</a>
                            </li>
                            <li class="nav-item">
                                <a class="nav-link" href="#">contact</a>
                            </li>
                        </ul>
                    </div>
                </div>
            </nav>
        </header>
        <div class="container ">
            <div class="text-block">
                <h1>Your business  <span class="text-primary">success</span><br /> is our  <span class="text-primary">business</span> </h1>
                <p>What a beautiful sunrise quia consequuntur magni dolores <br />beautiful sunrise quia consequuntur magni dolores</p>
                <button class="btn btn-primary"> Service</button>
                <button class="btn btn-outline-primary"> Contact</button>
            </div>
        </div>
    </div>
    <section>
        <div class="container">

            <div class="row mt-4">
                <div class="col-lg-4 col-md-4 col-sm-4 col-12 mb-2">
                    <div class="img-box">
                        <div class="thumb">
                            <img src="https://img.techpowerup.org/200821/sub-a.jpg" class="img-fluid rounded" alt="sub" />
                        </div>
                        <div class="details">
                            <h5>Finance & Restructuring </h5>
                        </div>
                    </div>
                </div>
                <div class="col-lg-4 col-md-4 col-sm-4 col-12 mb-2">
                    <div class="img-box">
                        <div class="thumb">
                            <img src="https://img.techpowerup.org/200821/sub2.jpg" class="img-fluid rounded" alt="sub" />
                        </div>
                        <div class="details">
                            <h5>Management</h5>
                        </div>
                    </div>

                </div>
                <div class="col-lg-4 col-md-4 col-sm-4 col-12 mb-2">
                    <div class="img-box style2">
                        <div class="details2">
                            <h5>We craft marketing and digital products thats grow business</h5>
                        </div>
                        <div class="owl-prev" style=""><i class="fa fa-angle-left "></i></div>
                        <div class="owl-next" style=""><i class="fa fa-angle-right"></i></div>
                    </div>

                </div>
            </div>

            <div class="row mt-5">
                <div class="col-lg-12 col-md-12 col-sm-12 col-12  mb-4">
                    <div class="text-left">
                        <h2>Service we provide</h2>
                    </div>
                </div>

                <div class="col-lg-4 col-md-4 col-sm-4 col-12 mb-2">
                    <div class="icon-box">
                        <div class="icon">
                            <span class='fa fa-area-chart'></span>
                        </div>
                        <div class="text-left">
                            <h3>Capital Market</h3>
                            <p>Impedit quo minus id quod maxime placeat facere possimus, omnis voluptas assumenda est.</p>
                        </div>
                    </div>

                </div>
                <div class="col-lg-4 col-md-4 col-sm-4 col-12 mb-2">
                    <div class="icon-box">
                        <div class="icon">
                            <span class='fa fa-bar-chart'></span>
                        </div>
                        <div class="text-left">
                            <h3>Technology Advisory</h3>
                            <p>Impedit quo minus id quod maxime placeat facere possimus, omnis voluptas assumenda est.</p>
                        </div>
                    </div>

                </div>
                <div class="col-lg-4 col-md-4 col-sm-4 col-12 mb-2">
                    <div class="icon-box">
                        <div class="icon">
                            <span class='fa fa-bitcoin'></span>
                        </div>
                        <div class="text-left">
                            <h3>Business Opportunities</h3>
                            <p>Impedit quo minus id quod maxime placeat facere possimus, omnis voluptas assumenda est.</p>
                        </div>
                    </div>

                </div>
                <div class="col-lg-4 col-md-4 col-sm-4 col-12 mb-2">
                    <div class="icon-box">
                        <div class="icon">
                            <span class='fa fa-pie-chart'></span>
                        </div>
                        <div class="text-left">
                            <h3>Investment Management</h3>
                            <p>Impedit quo minus id quod maxime placeat facere possimus, omnis voluptas assumenda est.</p>
                        </div>
                    </div>

                </div>
                <div class="col-lg-4 col-md-4 col-sm-4 col-12 mb-2">
                    <div class="icon-box">
                        <div class="icon">
                            <span class='fa fa-address-card'></span>
                        </div>
                        <div class="text-left">
                            <h3>Portfolio Managment</h3>
                            <p>Impedit quo minus id quod maxime placeat facere possimus, omnis voluptas assumenda est.</p>
                        </div>
                    </div>

                </div>
                <div class="col-lg-4 col-md-4 col-sm-4 col-12 mb-2">
                    <div class="icon-box">
                        <div class="icon">
                            <span class='fa fa-money'></span>
                        </div>
                        <div class="text-left">
                            <h3>Wealth Management</h3>
                            <p>Impedit quo minus id quod maxime placeat facere possimus, omnis voluptas assumenda est.</p>
                        </div>
                    </div>

                </div>



            </div>
        </div>
    </section>

    <section>
        <div class="bg-pd bg-whitef">
            <div class="container">
                <div class="row">
                    <div class="col-md-9 col-12">
                        <h3>Looking for an experienced business consultant</h3>
                    </div>
                    <div class="col-md-3 col-12 text-center ">
                        <button type="submit" class="btn btn-white">Get a quote</button>
                    </div>
                </div>
            </div>

        </div>
    </section>

    <section>
        <div class="container">
            <div class="row m-4">
                <div class="col-lg-12 col-sm-12">
                    <h3 class="text-center">Our cases</h3>
                </div>
            </div>

            <div class="row mb-4">
                <div class="col-lg-4 col-md-4 col-sm-4 col-12 mb-2">
                    <div class="img-box">
                        <div class="thumb">
                            <img src="https://img.techpowerup.org/200821/sub1.jpg" class="img-fluid rounded" alt="sub" />
                        </div>
                        <div class="text-center mt-2">
                            <h5>Finance & Restructuring </h5>
                            <p>Impedit  quod maxime placeat facere possimus, omnis voluptas assumenda est.</p>
                            <button type="button" class="btn btn-outline-primary">Read More</button>
                        </div>
                    </div>
                </div>
                <div class="col-lg-4 col-md-4 col-sm-4 col-12 mb-2">
                    <div class="img-box">
                        <div class="thumb">
                            <img src="https://img.techpowerup.org/200821/sub1.jpg" class="img-fluid rounded" alt="sub" />
                        </div>
                        <div class="text-center mt-2">
                            <h5>Succession Planning </h5>
                            <p>Impedit  quod maxime placeat facere possimus, omnis voluptas assumenda est.</p>
                            <button type="button" class="btn btn-outline-primary">Read More</button>
                        </div>
                    </div>
                </div>
                <div class="col-lg-4 col-md-4 col-sm-4 col-12 mb-2">
                    <div class="img-box">
                        <div class="thumb">
                            <img src="https://img.techpowerup.org/200821/sub1.jpg" class="img-fluid rounded" alt="sub" />
                        </div>
                        <div class="text-center mt-2">
                            <h5>Merger & Acquisition </h5>
                            <p>Impedit  quod maxime placeat facere possimus, omnis voluptas assumenda est.</p>
                            <button type="button" class="btn btn-outline-primary">Read More</button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section class="position-relative">
        <div class="container">
            <div class="row bg-whitef">
                <div class="col-lg-6 col-md-6 col-sm-6 col-12 p-0">
                    <img src="https://img.techpowerup.org/200821/busnessmen.jpg" class="img-fluid " alt="sub">
                </div>
                <div class="offset-md-1 col-lg-5 col-md-6 col-sm-6 col-12">
                    <div class="text-left pt-3">
                        <h3>Why Choose Us</h3>
                        <p>Impedit  quod maxime placeat facere possimus, omnis voluptas assumenda est.</p>

                    </div>

                    <div class="icon-box">
                        <div class="icon pull-left">
                            <span class="fa fa-area-chart"></span>
                        </div>
                        <div class="ml-90">
                            <h5 class="text-thm2">Diverse Expertise</h5>
                            <p>Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, adipisci velit, sed quia non.</p>
                        </div>
                    </div>
                    <div class="icon-box">
                        <div class="icon pull-left">
                            <span class="fa fa-bank"></span>
                        </div>
                        <div class="ml-90">
                            <h5 class="text-thm2">On Time Service</h5>
                            <p>Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, adipisci velit, sed quia non.</p>
                        </div>
                    </div>


                </div>
            </div>

        </div>
    </section>

    <section>
        <div class="container">
            <div class="row mt-5">
                <div class="col-lg-6 col-md-6 col-sm-6 col-12">
                    <div class="support_box text-center">
                        <h4>Friendly and dedicated support every steps on the way</h4>
                        <p>Real people are availabe 24hours a day, 7 days a week to help you with whatever you need.</p>
                        <h3 class="text-primary">140-221-547-224</h3>
                        <p>or</p>
                        <p>check out our <a class="ourlink" href="#">online support center.</a></p>
                    </div>
                </div>
                <div class="col-lg-6 col-md-6 col-sm-6 col-12">
                    <form  name="myForm"  method="post">
                        <div class="row Request-form ">
                            <div class="col-sm-12">
                                <h3 class="text-center text-primary">Request a free consultation </h3>
                            </div>
                            <div class="col-lg-6 col-sm-6">
                                <div class="form-group">
                                    <input type="text" name="fname " class="form-control Forvalidation" placeholder="First Name" required>
                                    <p style="display : none">Enter your First name</p>
                                </div>
                            </div>
                            <div class="col-lg-6 col-sm-6">
                                <div class="form-group">
                                    <input type="text" name="lname" class="form-control Forvalidation" placeholder="Last Name" required>
                                    <p style="display : none">Enter your Last name</p>
                                </div>
                            </div>
                            <div class="col-lg-6 col-sm-6">
                                <div class="form-group">
                                    <input type="email" name="email" class="form-control Forvalidation" placeholder="Email" required>
                                    <p style="display : none">Enter your Email Address</p>
                                    <b style="display : none">Invalid email </b>
                                </div>
                            </div>
                            <div class="col-lg-6 col-sm-6">
                                <div class="form-group">
                                    <input type="number" name="phoneno" class="form-control Forvalidation" placeholder="Phone" required>
                                    <p style="display : none">Enter your Phone number</p>
                                </div>
                            </div>
                            <div class="col-lg-12 col-sm-12">
                                <div class="form-group errormsgforinvest">
                                    <select class="form-control" id="investementconsultency" name="sellist1" required>
                                        <option value="-1">Select</option>
                                        <option value="1">1</option>
                                        <option value="2">2</option>
                                        <option value="3">3</option>
                                    </select>
                                    <p style="display : none">Select your investement Consultancy</p>
                                </div>
                            </div>
                            <div class="col-lg-12 col-sm-12">
                                <div class="form-group">
                                    <textarea class="form-control Forvalidation" rows="3" id="" required></textarea>
                                    <p style="display : none">Enter your message</p>
                                </div>
                                <button type="button" id="FormSubmit" class="btn btn-outline-primary">Submit</button>
                            </div>
                        </div>
                    </form>

                </div>
            </div>
        </div>
    </section>

    <section class="position-relative">
        <div class="container">
            <div class="row bg-whitef mt-5">

                <div class="offset-md-1 col-lg-5 col-md-6 col-sm-6 col-12">
                    <div class="text-left pt-3 we_are_experts">
                        <h3>We are an expert in this field</h3>
                        <p>Impedit  quod maxime placeat facere possimus, omnis voluptas assumenda est .</p>
                        <ul class="list-style-check ">
                            <li>Premium services and beyond your expectation</li>
                            <li>Get the best support among all venders</li>
                            <li>Fully customized plan</li>
                            <li>90-days growth sprints</li>
                        </ul>

                    </div>




                </div>
                <div class="col-lg-6 col-md-6 col-sm-6 col-12 p-0">
                    <img src="https://img.techpowerup.org/200821/busnessmen.jpg" class="img-fluid " alt="sub">
                </div>
            </div>

        </div>
    </section>

    <section>
        <div class="container">
            <div class="row m-4">
                <div class="col-lg-12 col-sm-12">
                    <h3 class="text-center">Our Blog</h3>
                </div>
            </div>

            <div class="row mb-4">
                <div class="col-lg-4 col-md-4 col-sm-4 col-12 mb-3">
                    <div class="card">
                        <div class="thumb">
                            <img src="https://img.techpowerup.org/200821/sub2.jpg" class="img-fluid " alt="sub" />
                        </div>
                        <div class="card-body text-center mt-2">
                            <h5>Discover new banking tricks & strategies</h5>
                            <p>Impedit  quod maxime placeat facere possimus, omnis voluptas assumenda est.</p>

                        </div>
                    </div>
                </div>
                <div class="col-lg-4 col-md-4 col-sm-4 col-12 mb-3">
                    <div class="card">
                        <div class="thumb">
                            <img src="https://img.techpowerup.org/200821/sub-a.jpg" class="img-fluid " alt="sub" />
                        </div>
                        <div class="card-body text-center mt-2">
                            <h5>Four Big Mistakes Your Small Business Is Making </h5>
                            <p>Impedit  quod maxime placeat facere possimus, omnis voluptas assumenda est.</p>

                        </div>
                    </div>
                </div><div class="col-lg-4 col-md-4 col-sm-4 col-12 mb-3">
                    <div class="card">
                        <div class="thumb">
                            <img src="https://img.techpowerup.org/200821/sub3.jpg" class="img-fluid " alt="sub" />
                        </div>
                        <div class="card-body text-center mt-2">
                            <h5>How to Find the Best Bank for Your Business </h5>
                            <p>Impedit  quod maxime placeat facere possimus, omnis voluptas assumenda est.</p>

                        </div>
                    </div>
                </div>

            </div>
        </div>
    </section>

    <footer>
        <div class="bg-pd bg-whitef">
            <div class="container">
                <div class="row">
                    <div class="col-lg-3 col-sm-6 col-12">
                        <div class="text-left">
                            <h5>About Us</h5>
                            <p>Sed ut perspiciatis unde omnis iste natus error. facere possimus, omnis voluptas assumenda est</p>
                            <ul class="social_icons ">
                                <li class="bgc-white"><a href="#" class="fa fa-facebook text-primary"></a></li>
                                <li class="bgc-white"><a href="#" class="fa fa-twitter text-primary"></a></li>
                                <li class="bgc-white"><a href="#" class="fa fa-linkedin text-primary"></a></li>
                                <li class="bgc-white"><a href="#" class="fa fa-vimeo-square text-primary"></a></li>
                            </ul>
                        </div>
                    </div>
                    <div class="col-lg-3 col-sm-6 col-12 latest">
                        <div class="text-left">
                            <h5>Latest News</h5>
                            <div class="mb-3">
                                <p>Etiam dignissim sit amet felis.</p>
                                <a href="#" class="post-date text-thm2">21 January, 2018</a>
                            </div>
                            <div class="mb-3">
                                <p>Etiam dignissim sit amet felis.</p>
                                <a href="#" class="post-date text-thm2">21 January, 2018</a>
                            </div>
                            <div class="mb-3">
                                <p>Etiam dignissim sit amet felis.</p>
                                <a href="#" class="post-date text-thm2">21 January, 2018</a>
                            </div>
                        </div>
                    </div>
                    <div class="col-lg-3 col-sm-6 col-12 latest">
                        <div class="text-left">
                            <h5>Important Link</h5>
                            <ul class="importen-link">
                                <li><a href="#"> About Us</a></li>
                                <li><a href="#">  Carrers</a></li>
                                <li><a href="#">  Our Team</a></li>
                                <li><a href="#">  Our Services</a></li>
                                <li><a href="#">   Privacy</a></li>
                            </ul>
                        </div>
                    </div>
                    <div class="col-lg-3 col-sm-6 col-12 latest">
                        <div class="text-left">
                            <h5>Important Link</h5>
                            <div class="mb-2">
                                <p>Business Consulting and Preparation.</p>
                                <a class="text-primary" href="#">https://twitter.com </a>
                            </div>
                            <div class="mb-2">
                                <p>Business Consulting and Preparation.</p>
                                <a class="text-primary" href="#">https://twitter.com </a>
                            </div>


                        </div>
                    </div>

                </div>
            </div>
        </div>
    </footer>

</body>
</html>
