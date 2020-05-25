# UD-UnSplash
React wrapper for UD and unsplash.com based on https://www.npmjs.com/package/react-unsplash-wrapper

# Unlimited Awesome Quality Pictures
Yes you read that right, that is basically what this component is. It is a react wrapper to **www.unsplash.com** allowing you to
easily obtain images from this website and place them on your dashboard.

# Demonstration

```
Import-Module -Name UniversalDashboard.Community -RequiredVersion 2.8.1
Import-Module -Name UniversalDashboard.UDUnSplash
Get-UDDashboard | Stop-UDDashboard

Start-UDDashboard -Port 10005 -Dashboard (
    New-UDDashboard -Title "Powershell UniversalDashboard" -Content {
        New-UDRow -Columns {
            New-UDColumn -Size 4 -Content {
                New-UDCard -Id "Dynamic" -Title "Thank you NHS" -Content {
                    New-UDUnSplash -Keyword "uk, covid-19, nhs" -Width 300 -Height 300 -Id "UNSPLASH1"
                    "Keyword = uk, covid-19, nhs"
                }
            }
            New-UDColumn -Size 4 -Content {
                New-UDCard -Title "Cornwall" -Content {
                    New-UDUnSplash -Keyword "cornwall" -Width 300 -Height 300 -Id "UNSPLASH2"
                    "Keyword = cornwall"
                }
            }
            New-UDColumn -Size 4 -Content {
                New-UDCard -Title "Collection ID" -Content {
                    New-UDUnSplash -CollectionId 3178572 -Width 300 -Height 300 -Id "UNSPLASH3"
                    "Some nice photos from a collection id"
                }
            }
            New-UDColumn -Size 4 -Content {
                New-UDCard -Title "Username result" -Content {
                    New-UDUnSplash -Username "anniespratt" -Width 300 -Height 300 -Id "UNSPLASH4"
                    "Some nice photos from a username"
                }
            }
            New-UDColumn -Size 4 -Content {
                New-UDCard -Title "By Photo Id" -Content {
                    New-UDUnSplash -PhotoId "ImoVrhUBeFs" -Width 300 -Height 300 -Id "UNSPLASH5"
                    "London city UK"
                }
            }
        }
    }
)

```

## Parameters
**-Height**
Accepts an integer for the value to specify the height of the image you want to display from unsplash.com

**-Width**
Accepts an integer for the value to specify the height of the image you want to display from unsplash.com

**-Keyword** 
This parameter accepts a string for the input, you can use multiple words, but separate them by a comma and enclose the 
complete string in double quotes as shown in the demonstration 

**-CollectionId**
Accepts an integer of a collection id of pictures from unsplash.com example in demonstration

**-Username**
Accepts a string for the input, which must be a valid username from unsplash.com please see demonstration

**-PhotoId**
Accepts a string as the input, whilst browsing unsplash.com if you see a particular image you like, take the photoid from the 
URL which uniquley identifies the image and use it.  Example in the demonstration.
