import {BCAbstractRobot, SPECS} from 'battlecode';

class MyRobot extends BCAbstractRobot {
    turn() {
    
    var choices = [[1, 0], [0, 1], [-1, 0], [0, -1], [0, 0], [0, 0]];
    var choicesCorner= [[0, 0], [0,0] [0, 0], [0, 0]];
    var choice = choices[0];

    
        if (this.me.unit === SPECS.VOYAGER) {
             var planetR = this.me.r;
             var planetC = this.me.c;
             var robotMap = this.getVisibleRobotMap();
             const tMap = this.map;
            
            do {
                
                    do{
                        if(((planetC >= this.n * (2/5)) && (planetC <= this.n * (3/5))) && (planetR >= this.n * (2/5)) && (planetR <= this.n * (3/5))){
                            if((this.me.id % 5) === 0){
                                choice = choices[0];
                            }
                            else if ((this.me.id % 4) == 0){
                                choice = choices[1];
                            }
                            else if ((this.me.id % 3) == 0){
                                choice = choices[2];
                            }
                            else if ((this.me.id % 2) == 0){
                                choice = choices[3];
                            }
                            else if ((this.map[this.me.r][this.me.c - 1] === false) && (this.map[this.me.r + 1][this.me.c] === false) && (this.map[this.me.r][this.me.c + 1] === false)){
                            	//move r-2 or r-1
                            	this.move(this.me.r - 1,this.me.c)
                            }

                            else if ((this.map[this.me.r][this.me.c - 1] === false) && (this.map[this.me.r - 1][this.me.c] === false) && (this.map[this.me.r][this.me.c + 1] === false)){
                            	//move r+2 or r+1
                            	this.move(this.me.r + 1,this.me.c)
                            }

                            else if ((this.map[this.me.r - 1][this.me.c] === false) && (this.map[this.me.r][this.me.c + 1] === false) && (this.map[this.me.r + 1][this.me.c] === false)){
	                            //move c-2  or c-1
                            	this.move(this.me.r,this.me.c - 1)
                            }

                            else if ((this.map[this.me.r - 1][this.me.c] === false) && (this.map[this.me.r + 1][this.me.c - 1] === false) && (this.map[this.me.r + 1][this.me.c] === false)){
                            	//move c+2 or c+1
	                            this.move(this.me.r,this.me.c + 1)
                            }

                        }
                        else if((planetC <= this.n / 4) && (planetR <= this.n / 4)){
                            choicesCorner = [[0, 1], [0, 1], [1, 0], [1, 0]];
                            choice = choicesCorner[Math.floor(Math.random()*choices.length)];
                        }
                        else if((planetC >= this.n * (3 / 4)) && (planetR <= this.n / 4)){
                            choicesCorner = [[0, -1], [0, -1], [1, 0], [1, 0]];
                            choice = choicesCorner[Math.floor(Math.random()*choices.length)];
                        }
                        else if((planetC <= this.n / 4) && (planetR >= this.n * (3 / 4))){
                            choicesCorner = [[0, 1], [0, 1], [-1, 0], [-1, 0]];
                            choice = choicesCorner[Math.floor(Math.random()*choices.length)];
                        }
                        else if((planetC >= this.n * (3 / 4)) && (planetR >= this.n * (3 / 4))){
                            choicesCorner = [[0, -1], [0, -1], [-1, 0], [-1, 0]];
                            choice = choicesCorner[Math.floor(Math.random()*choices.length)];
                        }
                        else if ((planetC <= (this.n / 2)) && (planetR <= (this.n / 2))){
                            choices = [[0, -1], [0, 1], [0, 1], [1, 0], [1, 0], [-1, 0]];
                            choice = choices[Math.floor(Math.random()*choices.length)];
                        }
                        else if((planetC >= (this.n / 2)) && (planetR <= (this.n / 2))){
                            choices = [[0, -1], [0, -1], [0, 1], [1, 0], [1, 0], [-1, 0]];
                            choice = choices[Math.floor(Math.random()*choices.length)];
                        }
