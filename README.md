# 2020-weleetka-robotics

Code saved for 2020 botball season
 cmpc(1); // go to transport coletor
    while(gmpc(0)<2300)
    {
        mav(0,600);
        mav(1,600);
    } 
    motor(0,0);
    motor(1,0);
    msleep(2000);
    set_servo_position(0,1611);
    msleep(1000);
     set_servo_position(1,148);
    msleep(1000); 
    cmpc(0); // go to transport coletor
    while(gmpc(0)<687)
    {
        mav(0,600);
        mav(1,600);
    }
    motor(0,0);
    motor(1,0);
    msleep(2000);
      set_servo_position(0,1288);
    msleep(1000);








  enable_servos();
    while(analog (0)<1000) // start go to black line 
            {
              motor(0,60);
                  motor(1,60);
          }
          
     printf("lift up at blalk line\n");
    int sholder=get_servo_position(0);
    int elbow=get_servo_position(1);
    while(sholder >= 1607)
    {
        motor(0,0);
        motor(1,0);
        msleep(100);
        sholder=sholder-100;
        set_servo_position(0,sholder);
        motor(0,0);
        motor(1,0);
    }
    
  while(elbow <=316 )
    {
        motor(0,0);
        motor(1,0);
        msleep(100);
        elbow=elbow+100;
        set_servo_position(1,elbow);
        motor(0,0);
        motor(1,0);
    }
