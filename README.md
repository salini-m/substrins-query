# substrins-query
to find the maximum length of sub strings in a given query
package com.hacker;

import java.util.Scanner;

public class W30SubstringQueries
{ 
	   public static void main(String[] args) {
		        Scanner in = new Scanner(System.in);
		        int n = in.nextInt();
		        int q = in.nextInt();
		        String[] s = new String[n];
		        for(int s_i=0; s_i < n; s_i++){
		            s[s_i] = in.next();
		        }
		        for(int a0 = 0; a0 <q; a0++){
		            int x = in.nextInt();
		            int y = in.nextInt();
		            String s1 = s[x];
		            String s2 = s[y];
		            int length = 0; 
		            boolean b = false;
		            String s4 =s1;
		      //      System.out.println( );
		            for(int i=s1.length();i>0;i--){ 
		            	for(int j=0,k=i;k<=s1.length() ;j++,k++){ 
		            	 	s4 = s1.substring(j, k);
		            	// 	System.out.println(s4);
		            		if(s2.contains(s4)){
		            			length = s4.length();
		            			b = true;
		            			break;
		            		}
		            	}
		            	if(b==true)
		            		break;
		            }
		            System.out.println(length);
		        }
		    } 
}
