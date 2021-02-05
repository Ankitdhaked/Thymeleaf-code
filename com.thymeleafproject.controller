package com.thymeleafproject.controller;

import java.time.LocalDateTime;
import java.util.Date;
import java.util.List;

import org.springframework.stereotype.Controller;
import org.springframework.ui.Model;
import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.RequestMapping;
import org.springframework.web.bind.annotation.RequestMethod;

@Controller
public class MyController 
{

	@RequestMapping(value = "/about",method = RequestMethod.GET)
	public String about(Model model)
	{
		System.out.println("Inside about handler..");
		
		//putting data in model
		
		model.addAttribute("name","Ankit kumar");
		
		model.addAttribute("currentDate",new Date().toLocaleString());
		
		return "about";
	}
	
	
	//handling iteration
	@GetMapping("/loop")
	public String iterateHandler(Model m)
	{
		//send
		List<String> names = List.of("Ankit","cleagruber","anku","mohan");
		m.addAttribute("names",names);
		return "iterate";
	}
	
	//handler for conditional statement
	@GetMapping("/condition")
	public String conditionHandler(Model m)
	{
		System.out.println("conditional handler statement");
		m.addAttribute("isActive",true);  //true and false
		m.addAttribute("gender","M");
		
		List<Integer> li = List.of(321,123,23,21,42);
		m.addAttribute("mylist",li);
		return "condition";
	}
	
	//handler for including fragments
	@GetMapping("/service")
	public String servicesHandler(Model m)
	{
		m.addAttribute("title","i like you");
		m.addAttribute("subtitle",LocalDateTime.now().toString());
		//processing logic
		return "service";
	}
	
	//for new about
	@GetMapping("/aboutnew")
	public String newAbout()
	{
		
		return "aboutnew";
	}
	
	 //for contect
	@GetMapping("/contact")
	public String contact()
	{
			
		return "contact";
	}
}
