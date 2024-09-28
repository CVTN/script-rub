local OrionLib = loadstring(game:HttpGet(('https://raw.githubusercontent.com/shlexware/Orion/main/source')))()
 local Window = OrionLib:MakeWindow({Name = "HUB CVTN", HidePremium = false, SaveConfig = false, ConfigFolder = "OrionTest"})

 --[[
 Name = <string> - The name of the UI.
 HidePremium = <bool> - Whether or not the user details shows Premium status or not.
 SaveConfig = <bool> - Toggles the config saving in the UI.
 ConfigFolder = <string> - The name of the folder where the configs are saved.
 IntroEnabled = <bool> - Whether or not to show the intro animation.
 IntroText = <string> - Text to show in the intro animation.
 IntroIcon = <string> - URL to the image you want to use in the intro animation.
 Icon = <string> - URL to the image you want displayed on the window.
 CloseCallback = <function> - Function to execute when the window is closed.
 ]]
 local Tab = Window:MakeTab({
	Name = "pets",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
     })

  Tab:AddButton({
	Name = "PET 5",
	Callback = function()
      		print("button pressed")
  	

        local args = {
        [1] = "1"
         }

            game:GetService("ReplicatedStorage"):WaitForChild("Events"):WaitForChild("PlayerPressedKeyOnEgg"):FireServer(unpack(args))

                 end    
                  })
            Tab:AddButton({
	        Name = "PET 50",
	        Callback = function()
      		print("button pressed")
  	
              local args = {
               [1] = "1"
                }

                game:GetService("ReplicatedStorage"):WaitForChild("Events"):WaitForChild("PlayerPressedKeyOnEgg"):FireServer(unpack(args))

               end
                  })

              Tab:AddButton({
	            Name = "PET 2.5k",
	              Callback = function()
      		       print("button pressed")
  	
                 local args = {
             [1] = "2"
            }

                      game:GetService("ReplicatedStorage"):WaitForChild("Events"):WaitForChild("PlayerPressedKeyOnEgg"):FireServer(unpack(args))
                    end
                 })

                       Tab:AddButton({
	                     Name = "pet 30M",
	                       Callback = function()
      		print("button pressed")
  	 
	        local args = {
               [1] = "3"
             }

                   game:GetService("ReplicatedStorage"):WaitForChild("Events"):WaitForChild("PlayerPressedKeyOnEgg"):FireServer(unpack(args))
 
	       end  
              })

               local Tab = Window:MakeTab({
	    Name = "raid",
       	Icon = "rbxassetid://4483345998",
	       PremiumOnly = false
                 })


            Tab:AddButton({
	       Name = "DUEGO",
              Callback = function()
      		print("button pressed")

    local args = {
    [1] = "StartDungeon"
    }

          game:GetService("ReplicatedStorage"):WaitForChild("Events"):WaitForChild("DungeonEvent"):FireServer(unpack(args))
     local args = {
    [1] = "Info"
 }

         game:GetService("ReplicatedStorage"):WaitForChild("Events"):WaitForChild("QuestEvent"):InvokeServer(unpack(args))


     end

      })



         local Tab = Window:MakeTab({
	Name = "TP",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
        })


      Tab:AddButton({
	Name = "1 ARENA",
	Callback = function()
      		print("button pressed")
  	
     local args = {
    [1] = 1,
    [2] = 11
    }

      game:GetService("ReplicatedStorage"):WaitForChild("Packages"):WaitForChild("Knit"):WaitForChild("Services"):WaitForChild("RaceService"):WaitForChild("RF"):WaitForChild("ReachedCheckpoint"):InvokeServer(unpack(args))

     end    
       })


      Tab:AddButton({
	Name = "2 ARENA",
	Callback = function()
      		print("button pressed")
  	
	local args = {
    [1] = "Teleport",
    [2] = Vector3.new(-2352.2197265625, 97.0920181274414, 2372.9619140625)
 }

           game:GetService("ReplicatedStorage"):WaitForChild("Events"):WaitForChild("ResetPlayerTank"):FireServer(unpack(args))
  
	  
	  
	  
	  
	  
	  end    
      })
    Tab:AddButton({
	   Name = "3 ARENA",
	   Callback = function()
      		print("YESA")
	

        local args = {
    [1] = "Teleport",
    [2] = Vector3.new(-3351.2060546875, 97.69249725341797, 2376.299072265625)
    }

     game:GetService("ReplicatedStorage"):WaitForChild("Events"):WaitForChild("ResetPlayerTank"):FireServer(unpack(args))



   end    
      })

     Tab:AddButton({
	Name = "4 ARENA",
	Callback = function()
      		print("button pressed")
        local args = {
     [1] = "Teleport",
    [2] = Vector3.new(-4351.447265625, 98.26249694824219, 2378.768798828125)
        }

          game:GetService("ReplicatedStorage"):WaitForChild("Events"):WaitForChild("ResetPlayerTank"):FireServer(unpack(args))


        end
        })



   local Tab = Window:MakeTab({
	Name = "auto Click",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
 })




 local click = true


 Tab:AddToggle({
	     Name = "click",
	     Default = click,
	      Callback = function(Value)
		      click = Value
	game:GetService("ReplicatedStorage"):WaitForChild("StopFireCannon"):FireServer()
        
   game:GetService("ReplicatedStorage"):WaitForChild("FireCannon"):FireServer()

    game:GetService("ReplicatedStorage"):WaitForChild("Events"):WaitForChild("ReloadEvent"):FireServer()

 end    
  })

  while click do
    wait ()
    print("ativo")

     game:GetService("ReplicatedStorage"):WaitForChild("Events"):WaitForChild("DamageIncreaseOnClickEvent"):FireServer()


    game:GetService("ReplicatedStorage"):WaitForChild("FireCannon"):FireServer()

   game:GetService("ReplicatedStorage"):WaitForChild("Events"):WaitForChild("ReloadEvent"):FireServer()

  end
  OrionLib:Init()



