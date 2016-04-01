
# HibernateTutorial
//
package com;

import org.hibernate.*;
import org.hibernate.cfg.*;
public class Test {
	
	public static void main(String[] args) {
		

		Configuration cfg=new Configuration();
		cfg.configure("hibernate.cfg.xml");
		
		SessionFactory factory=cfg.buildSessionFactory();
		
	              Session session=	factory.openSession();
		  Transaction tx=session.beginTransaction();
		  
	              Product p=new Product();
	              
	              p.setProductId(2);
	              p.setPrice(425);
	              p.setProName("iphone2");
	             session.save(p);
	              
	         // Object obj= session.get(Product.class, p);
	         // Product p1= (Product)obj;
	          System.out.println("hiiiiiiiiiiiiiiii");
	         // System.out.println(p1.getPrice());
	          tx.commit();
	          session.close();
	          factory.close();
	            
	            
	}

}
