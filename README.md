sleep, 3000
MouseGetPos, xx, yy
r:=100
interval = 5
counter =0

MouseClick, L,,,,, D
Loop % r/interval
{

	mousemove % xx+counter, sqrt(r**2 - (xx+counter-xx)**2) + (yy-r)
	counter += interval
}
MouseClick, L,,,,, U
return
