# RGBNamer
using System;

namespace RGBNamer
{
    class Program
    {
        static void Main(string[] args)
        {
            //the point of this program is to name colors after defining rgb values

            //user input accepted here
            Console.WriteLine("Please define R values between 0-255:  ");
            int R = Int32.Parse(Console.ReadLine());
            Console.WriteLine("Please define G values between 0-255:  ");
            int G = Int32.Parse(Console.ReadLine());
            Console.WriteLine("Please define B values between 0-255;  ");
            int B = Int32.Parse(Console.ReadLine());
            
            //Boolean variables used to provide text output
            bool White = (R + G + B == 765);
            bool Black = (R + G + B == 0);
            bool Red = (G + B == 0);
            bool Green = (R + B == 0);
            bool Blue = (G + R == 0);
            bool Redish = (R >= (G + B));
            bool Bluish = (B >= (G + R));
            bool Greenish = (G >= (R + B));
            string err = "Please ensure all values are between 0-255";
           
            //first three statements are if a user defies instructions.
            if (R >= 256)
            { Console.WriteLine(err); }
            else
            { if (G >= 256)
                { Console.WriteLine(err); }
                else
                { if (B >= 256)
                    { Console.WriteLine(err); }
                    
                    else //actual program runs from here

                    { if (White) //If the result of the input would be White
                        { Console.WriteLine("That Color is White"); }

                        else

                        {
                            if (Black) //if the result of the input would be Black
                            { Console.WriteLine("That Color is Black"); }

                            else

                            {
                                if (Red) //if the result of the input appears Red  
                                { Console.WriteLine("That Color is Red"); }

                                else

                                {
                                    if (Blue) //if the result of the input appears blue
                                    { Console.WriteLine("That Color is Blue"); }

                                    else


                                    {
                                        if (Green) //if the result of the input appears green
                                        { Console.WriteLine("That Color Green"); }

                                        else

                                        {
                                            if (Redish) //if the result of the input appears redish
                                            { Console.WriteLine("That's pretty Redish"); }

                                            else

                                            {
                                                if (Greenish) //if the result of the input appears greenish
                                                { Console.WriteLine("That's kinda Green"); }

                                                else

                                                {
                                                    if (Bluish) // if the result of the input appears bluish
                                                    { Console.WriteLine("Yeeeaah, that's probably kinda Blue"); }
                                                }


                                            }
                                        }


                                    }
                                }

                            }
                        }

                    }
                }
            }
        }
    } 
}
