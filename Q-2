import os
import sys
FNAME="covid_records.txt"
def append_record(name,age,gender,vaccine,date):
    with open(FNAME,"a",encoding="utf-8") as f:
        f.write(f"{name}|{age}|{gender}|{vaccine}|{date}\n")
def read_records():
    if not os.path.exists(FNAME):
        return []
    with open(FNAME,"r",encoding="utf-8") as f:
        lines=[l.strip() for l in f if l.strip()]
    records=[l.split("|") for l in lines]
    return records
def display(records):
    cols=["Name","Age","Gender","Vaccine","Date"]
    widths=[20,5,8,15,12]
    header="".join(c.ljust(w) for c,w in zip(cols,widths))
    print(header)
    print("-"*sum(widths))
    for r in records:
        row=[(r[i] if i<len(r) else "").ljust(w) for i,w in enumerate(widths)]
        print("".join(row))
def main():
    try:
        while True:
            print("1 Add 2 View 3 Exit")
            c=input("Choice: ").strip()
            if c=="1":
                name=input("Name: ").strip()
                age=input("Age: ").strip()
                gender=input("Gender: ").strip()
                vaccine=input("Vaccine: ").strip()
                date=input("Date (YYYY-MM-DD): ").strip()
                append_record(name,age,gender,vaccine,date)
                print("Record appended.")
            elif c=="2":
                rec=read_records()
                display(rec)
            elif c=="3":
                break
            else:
                print("Invalid choice")
    except Exception as e:
        print("Error:",e)
        sys.exit(1)
if _name=="main_":
    main()
