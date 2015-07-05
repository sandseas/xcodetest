//# xcodetest
//mystic app test

//
//  ViewController.swift
//  apr3lo
//
//  Created by Sandra Cook on 4/3/15.
//  Copyright (c) 2015 Sandra Cook. All rights reserved.
//

import UIKit

class ViewController: UIViewController {

    var answerArray:[String] = ["Definitely!",
                        "Without a doubt!",
                        "Trust your instincts!",
                        "Maybe.",
                        "Doubtful.",
                        "Not likely."]
    
    //answerArray.count
    
    @IBOutlet weak var answerLabel: UILabel!
    
    @IBOutlet weak var askQuestionLabel: UIButton!
    
    @IBOutlet weak var backgroundImageView: UIImageView!
    
    
    
    override func viewDidLoad() {
        super.viewDidLoad()
        // Do any additional setup after loading the view, typically from a nib.

        
        
        self.askQuestionLabel.setTitle("Ask Question", forState: UIControlState.Normal)
        
        self.answerLabel.text = "?"
    
    }

    
    override func didReceiveMemoryWarning() {
        super.didReceiveMemoryWarning()
        // Dispose of any resources that can be recreated.
    }


   
    @IBAction func ButtonPressed(sender: UIButton) {
    
        //set number for random answer number
        var randomAnswerNumber:Int = Int(arc4random_uniform(6))
        
        //set answer string for random answer
        var randomAnwerString:String = self.answerArray[randomAnswerNumber]
        
        
        self.answerLabel.text = randomAnwerString
        
        self.askQuestionLabel.setTitle("Ask Again", forState: UIControlState.Normal)
    
    }

}

