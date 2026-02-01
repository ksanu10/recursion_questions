## flattening nested list

data = [1, [2, 3], 4]


def flattening(data):
  flat_new = []
  for i in data:
    if type(i)== int:
      flat_new.append(i)
    else:
      flat_new.extend(flattening(i))
  return flat_new

flattening(data)
