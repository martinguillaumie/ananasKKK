local ToNote in
fun {ToNote Note}
   case Note of Nom#Octave then
      if Nom==a then
	 echantillon(hauteur:(12*(Octave-4)+1) durée:1 intrument:none)
      elseif Nom==b then
	 echantillon(hauteur:(12*(Octave-4)+3) durée:1 intrument:none)
      elseif Nom==c then
	 echantillon(hauteur:(12*(Octave-4)+4) durée:1 intrument:none)
      elseif Nom==d then
	 echantillon(hauteur:(12*(Octave-4)+6) durée:1 intrument:none)	 
      elseif Nom==e then
	 echantillon(hauteur:(12*(Octave-4)+8) durée:1 intrument:none)
      elseif Nom==f then
	 echantillon(hauteur:(12*(Octave-4)+9) durée:1 intrument:none)
      else echantillon(hauteur:(12*(Octave-4)+11) durée:1 intrument:none)
      end
      
   [] Atom then
      case {AtomToString Atom} of [N] then
	 if Atom==a then echantillon(hauteur:0 durée:1 intrument:none)
	 elseif Atom==b then echantillon(hauteur:2 durée:1 intrument:none)
	 elseif Atom==c then echantillon(hauteur:3 durée:1 intrument:none)
	 elseif Atom==d then echantillon(hauteur:5 durée:1 intrument:none)
	 elseif Atom==e then echantillon(hauteur:7 durée:1 intrument:none)
	 elseif Atom==f then echantillon(hauteur:8 durée:1 intrument:none)
	 else echantillon(hauteur:10 durée:1 intrument:none)
	 end
	 
      [] [N O] then
	 if {StringToAtom [N]}==a then
	    echantillon(hauteur:(12*({StringToInt [O]}-4)) durée:1 intrument:none)
	 elseif {StringToAtom [N]}==b then
	    echantillon(hauteur:(12*({StringToInt [O]}-4)+2) durée:1 intrument:none)
	 elseif {StringToAtom [N]}==c then
	    echantillon(hauteur:(12*({StringToInt [O]}-4)+3) durée:1 intrument:none)
	 elseif {StringToAtom [N]}==d then
	    echantillon(hauteur:(12*({StringToInt [O]}-4)+5) durée:1 intrument:none)
	 elseif {StringToAtom [N]}==e then
	    echantillon(hauteur:(12*({StringToInt [O]}-4)+7) durée:1 intrument:none)
	 elseif {StringToAtom [N]}==f then
	    echantillon(hauteur:(12*({StringToInt [O]}-4)+8) durée:1 intrument:none)
	 else echantillon(hauteur:(12*({StringToInt [O]}-4)+2) durée:1 intrument:none)
	 end
      end
   end
end
      
