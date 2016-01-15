# bullseyeloop
import java.awt.Color;
import javax.swing.JFrame;
import java.awt.Graphics;
import java.util.Random;

import javax.swing.*;


public class BullseyeLoop extends JFrame
{
    public BullseyeLoop()
    {
        super ("Target Loop");
        setSize(800,800);
        setVisible(true);
    }
    public void paint(Graphics g)
    {
        JFrame frame = new JFrame();
        frame.setSize(1000,1000);
         
        int width = 600;
        int length = 600;
        Random  gen = new Random();   
                super.paint(g);
            //int diam1 =10;
      

            
for(int i=1;i<=10;i++)
                
            {
            
                
                int red = gen.nextInt(256);
                int green = gen.nextInt(256);
                int blue = gen.nextInt(256);

                g.setColor( new Color( red,green, blue));
                g.fillArc(65, 75, width, length, 0, 360);
               
                width -=60;
                length -= 60;
                
                //g.fillOval( 100,100,diam1,diam1);
               // diam1 +=10; 
                      
        }

            
            
    }
   public static void main(String args[])
   {
        BullseyeLoop application = new BullseyeLoop();
        application.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
    }
        
    
}
