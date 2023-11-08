def manipulation_of_strings(result_string, remaining_strings):
    while remaining_strings:
        found = False
        for i, current_string in enumerate(remaining_strings):
            
            if current_string in result_string and current_string != remaining_strings[-1]:
                continue
            else:
                
                if result_string.endswith(current_string[:2]):
                    result_string += current_string[2:]  
                    remaining_strings.pop(i)  
                    found = True
                    break
                
                elif current_string.endswith(result_string[:2]):
                    result_string = current_string + result_string[2:]  
                    remaining_strings.pop(i)  
                    found = True
                    break
                
                elif result_string == '':
                    result_string = current_string
                    remaining_strings.pop(i) 
                    found = True
                    break

        
        if not found:
            missing_items = [item for item in remaining_strings if item not in result_string]
            return result_string, missing_items

    return result_string, []

resultant_string = ''
remaining_string_list = ['U_CH', 'PYT', 'CHEN', 'NAI', 'SNU_', 'OHN','ENNA', 'ANY', 'ART']


result, missing = manipulation_of_strings(resultant_string, remaining_string_list)
print("Resultant String:", result)
print("Missing Items:", missing)
