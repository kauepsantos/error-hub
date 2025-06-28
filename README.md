local a=game:GetService("Players") local b=game:GetService("UserInputService") local c=a.LocalPlayer
local d=Instance.new("ScreenGui") d.Name="error_Hub_beta_GUI" d.Parent=c:WaitForChild("PlayerGui") d.ResetOnSpawn=false
local e=Instance.new("Frame") e.Size=UDim2.new(0,380,0,260) e.Position=UDim2.new(0.5,-190,0.5,-130) e.BackgroundColor3=Color3.fromRGB(27,28,38) e.Active=true e.Parent=d
local f=Instance.new("UICorner") f.CornerRadius=UDim.new(0,22) f.Parent=e
local g=Instance.new("Frame") g.Size=UDim2.new(1,0,0,40) g.Position=UDim2.new(0,0,0,0) g.BackgroundTransparency=1 g.Parent=e g.ZIndex=3
local h=Instance.new("TextLabel") h.Size=UDim2.new(1,0,1,0) h.BackgroundTransparency=1 h.Text="error_Hub-beta" h.Font=Enum.Font.GothamBold h.TextColor3=Color3.fromRGB(255,255,255) h.TextSize=22 h.Parent=g
local i=Instance.new("UIGradient") i.Color=ColorSequence.new{ColorSequenceKeypoint.new(0,Color3.fromRGB(120,180,255)),ColorSequenceKeypoint.new(0.3,Color3.fromRGB(180,140,255)),ColorSequenceKeypoint.new(0.6,Color3.fromRGB(255,140,220)),ColorSequenceKeypoint.new(1,Color3.fromRGB(110,255,190))} i.Rotation=0 i.Parent=h
local j=Instance.new("Frame") j.Size=UDim2.new(1,0,0,36) j.Position=UDim2.new(0,0,0,40) j.BackgroundColor3=Color3.fromRGB(34,37,54) j.Parent=e j.ZIndex=2
local k=Instance.new("UICorner") k.CornerRadius=UDim.new(0,18) k.Parent=j
local l=Instance.new("Frame") l.Size=UDim2.new(0,90,1,-76) l.Position=UDim2.new(0,0,0,76) l.BackgroundColor3=Color3.fromRGB(36,40,60) l.Parent=e
local m=Instance.new("UICorner") m.CornerRadius=UDim.new(0,14) m.Parent=l
local n=Instance.new("TextButton") n.Size=UDim2.new(1,-12,0,40) n.Position=UDim2.new(0,6,0,16) n.Text="Visuals" n.Font=Enum.Font.GothamBold n.TextSize=17 n.BackgroundColor3=Color3.fromRGB(67,150,255) n.TextColor3=Color3.fromRGB(255,255,255) n.Parent=l
local o=Instance.new("UICorner") o.CornerRadius=UDim.new(0,12) o.Parent=n
local p=Instance.new("TextButton") p.Size=UDim2.new(1,-12,0,40) p.Position=UDim2.new(0,6,0,70) p.Text="Scripts" p.Font=Enum.Font.GothamBold p.TextSize=17 p.BackgroundColor3=Color3.fromRGB(44,200,150) p.TextColor3=Color3.fromRGB(255,255,255) p.Parent=l
local q=Instance.new("UICorner") q.CornerRadius=UDim.new(0,12) q.Parent=p
local r=Instance.new("Frame") r.Size=UDim2.new(1,-100,1,-86) r.Position=UDim2.new(0,98,0,86) r.BackgroundTransparency=1 r.Parent=e
local s=Instance.new("Frame") s.Size=UDim2.new(1,0,1,0) s.BackgroundTransparency=1 s.Parent=r
local t=Instance.new("TextButton") t.Size=UDim2.new(0,200,0,54) t.Position=UDim2.new(0.5,-100,0.3,-27) t.Text="Dupe" t.Font=Enum.Font.GothamBlack t.TextSize=22 t.BackgroundColor3=Color3.fromRGB(68,255,175) t.TextColor3=Color3.fromRGB(24,28,35) t.Parent=s
local u=Instance.new("UICorner") u.CornerRadius=UDim.new(0,22) u.Parent=t
local v=Instance.new("Frame") v.Size=UDim2.new(1,0,1,0) v.BackgroundTransparency=1 v.Visible=false v.Parent=r
local w=Instance.new("TextLabel") w.Size=UDim2.new(1,0,0,50) w.Position=UDim2.new(0,0,0.2,0) w.Text="sem nada por enquanto" w.Font=Enum.Font.Gotham w.TextSize=20 w.BackgroundTransparency=1 w.TextColor3=Color3.fromRGB(170,170,170) w.Parent=v
n.MouseButton1Click:Connect(function()s.Visible=true v.Visible=false n.BackgroundColor3=Color3.fromRGB(67,150,255) p.BackgroundColor3=Color3.fromRGB(44,200,150)end)
p.MouseButton1Click:Connect(function()s.Visible=false v.Visible=true n.BackgroundColor3=Color3.fromRGB(44,200,150) p.BackgroundColor3=Color3.fromRGB(67,150,255)end)
local x=false local y local z
local function A(B) local C=B.Position-y e.Position=UDim2.new(e.Position.X.Scale,z.X.Offset+C.X,e.Position.Y.Scale,z.Y.Offset+C.Y) end
j.InputBegan:Connect(function(B)if B.UserInputType==Enum.UserInputType.MouseButton1 or B.UserInputType==Enum.UserInputType.Touch then x=true y=B.Position z=e.Position B.Changed:Connect(function()if B.UserInputState==Enum.UserInputState.End then x=false end end) end end)
j.InputChanged:Connect(function(B)if x and(B.UserInputType==Enum.UserInputType.MouseMovement or B.UserInputType==Enum.UserInputType.Touch)then A(B)end end)
b.InputChanged:Connect(function(B)if x and(B.UserInputType==Enum.UserInputType.MouseMovement or B.UserInputType==Enum.UserInputType.Touch)then A(B)end end)
t.MouseButton1Click:Connect(function()
local D=c.Character and c.Character:FindFirstChildOfClass("Tool")
if D then local E=D:Clone()E.Parent=c.Backpack t.Text="Item Duplicado!" wait(1) t.Text="Dupe"
else t.Text="Segure um item!" wait(1) t.Text="Dupe" end end)
