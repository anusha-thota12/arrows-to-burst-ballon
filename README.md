# arrows-to-burst-ballon
Find the minimum no.of arrows to burst ballons.Given a set of ballons each represented by a range start,end find the minimum no.of arrows required to burst all the ballons.An arrow can burst multiple ballons if the overlap. {{10,16},{2,8},{1,6},{7,12}}
import java.util.*;
class Main {
    public static void main(String[] args) {
        Scanner sc= new Scanner(System.in);
        int n=sc.nextInt();
        int[][] ballons={{1,6},{2,8},{7,12},{10,16}};
        int arrow=1;
        int current = ballons[0][1];
        for(int i=0;i<n;i++){
            if(ballons[i][0]>current){
                arrow++;
                current=ballons[i][1];
            }
        }
        System.out.println(arrow);
    }
}
