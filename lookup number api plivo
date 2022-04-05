import plivo
import json
import threading

asu = input('input list: ')
f = open(asu).read().split()
for line in f:
    try:
        client = plivo.RestClient('auth_id','auth_token')
        response = client.lookup.get('+1'+line)
        print(response['carrier']['name'] + ' --> ' + response['phone_number'])
        test = response['carrier']['name'] + ' --> ' + response['phone_number']
        file1 = open("result.txt", "a")
        file1.write("\n")
        file1.writelines(test)
        file1.close()
        if 'str' in line:
            break
    except:
        print('invalid')

