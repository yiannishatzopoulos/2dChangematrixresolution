# 2dChangematrixresolution
Change (upscale / downscale) 2d matrix resolution -
a small java implementation utility to resample a 2d matrix into a higher or lower resolution.
How to use

 public static void main(String[] args) {
        // TODO code application logic here

        // my input matrix
        double[][] input_data = {
            {1, 2, 3, 4, 5, 6, 7, 8, 9, 10},
            {1, 2, 3, 4, 5, 6, 7, 8, 9, 10},
            {1, 2, 3, 4, 5, 6, 7, 8, 9, 10},
            {1, 2, 3, 4, 5, 6, 7, 8, 9, 10},
            {1, 2, 3, 4, 5, 6, 7, 8, 9, 10},
            {1, 2, 3, 4, 5, 6, 7, 8, 9, 10},
            {1, 2, 3, 4, 5, 6, 7, 8, 9, 10},
            {1, 2, 3, 4, 5, 6, 7, 8, 9, 10},
            {1, 2, 3, 4, 5, 6, 7, 8, 9, 10}
        };
        //------------------------------------------------------------------------
        // starting lat,lng top left
        double start_lng = 1;
        double start_lat = 1;
        double orig_step = 1;
        double new_step = 0.3; // for interpolation
        //------------------------------------------------------------------------
        InterpolationEngine Interpolationn = new InterpolationEngine();

        Interpolationn.print(input_data);

        double[][] nb = Interpolationn.Execute(
                start_lng,
                start_lat,
                orig_step,
                new_step,
                input_data);

        Interpolationn.print(nb);

        // now print interpolated matrix
    }
