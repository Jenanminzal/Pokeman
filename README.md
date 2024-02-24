# Pokeman

import random
class pokeman:
    def __init__(self,N,Level,Stringth,Speed,Type,Life):
      self.name=N
      self.L=Level
      self.Stringth=Stringth
      self.Speed=Speed
      self.T=Type
      self.Life=Life

#select which pekomon is first

def ISFirst(pokeman_list):
    max =0
    first_pokemon =None
    for i in range(5):
        x=random.randint(1,20)+ pokeman.Speed
        while x>max:
            max=x
            first_pokemon=i
    return first_pokemon
selects_pokeman= random.randint()
#generate list of pokemans to select one of them.

# attack proccess:
#1-demag
#2-remove the demg from life of pekomn
#3-pokeman with life=0 dead

#the def of demage
def damage(p1,p2):
    calc =0
    typemodifier= modifierCalculator(p1,p2)
    calc += typemodifier*(random.randint(1,20) + p1.stringt)
    return calc

#how to calc modifier
def modifierCalculator(attP, defP):
    match attP.Type:
        case "fire":
            match defP.Type:
                case "fire ","water","wind":
                    return 1
            return 2
        case "water":
            match defP.Type:
                case "fire","water","earth":
                    return 1
            return 2
        case "earth":
            match defP.Type:
                case "fire","earth","wind":
                    return 1
            return 2
        case "wind":
            match defP.Type:
                case "water","wind":
                    return 1
            return 2
    return

def Isalive(p1,p2):
    while p1["life"]>0 &p2 ["life"]>0:
        p1.["life"]-=damage(p1,p2)
        p2.["life"] -=damage(p1,p2)

def assign_roles(p1,p2):
    return [p1, p2] if p1["speed"] > p2["speed"] else [p2, p1]










