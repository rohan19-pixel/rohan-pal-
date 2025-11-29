import json,os,re,sys
FNAME="library.json"
def load():
    if not os.path.exists(FNAME):
        return {},set()
    with open(FNAME,"r",encoding="utf-8") as f:
        data=json.load(f)
    books={b["id"]:b for b in data}
    ids=set(books.keys())
    return books,ids
def save(books):
    with open(FNAME,"w",encoding="utf-8") as f:
        json.dump(list(books.values()),f,indent=2)
def add_book(books,ids):
    bid=input("ID: ").strip()
    if bid in ids:
        print("Duplicate ID")
        return
    name=input("Name: ").strip()
    author=input("Author: ").strip()
    category=input("Category: ").strip()
    books[bid]={"id":bid,"name":name,"author":author,"category":category}
    ids.add(bid)
    save(books)
    print("Added")
def search_books(books):
    kw=input("Regex keyword: ").strip()
    try:
        prog=re.compile(kw, re.IGNORECASE)
    except Exception as e:
        print("Invalid regex")
        return
    found=[]
    for b in books.values():
        s=f"{b['id']} {b['name']} {b['author']} {b['category']}"
        if prog.search(s):
            found.append(b)
    if not found:
        print("No matches")
    else:
        for b in found:
            print(b)
def update_book(books,ids):
    bid=input("ID to update: ").strip()
    if bid not in ids:
        print("Not found")
        return
    name=input("New name (blank to keep): ").strip()
    author=input("New author (blank to keep): ").strip()
    category=input("New category (blank to keep): ").strip()
    if name:
        books[bid]["name"]=name
    if author:
        books[bid]["author"]=author
    if category:
        books[bid]["category"]=category
    save(books)
    print("Updated")
def delete_book(books,ids):
    bid=input("ID to delete: ").strip()
    if bid not in ids:
        print("Not found")
        return
    del books[bid]
    ids.remove(bid)
    save(books)
    print("Deleted")
def list_books(books):
    if not books:
        print("No books")
        return
    for b in books.values():
        print(b)
def explain():
    print("Lists store ordered results, dicts map ids to entries, sets prevent duplicates, files persist data.")
def main():
    try:
        books,ids=load()
        while True:
            print("1 Add 2 Search 3 Update 4 Delete 5 List 6 Explain 7 Exit")
            c=input("Choice: ").strip()
            if c=="1":
                add_book(books,ids)
            elif c=="2":
                search_books(books)
            elif c=="3":
                update_book(books,ids)
            elif c=="4":
                delete_book(books,ids)
            elif c=="5":
                list_books(books)
            elif c=="6":
                explain()
            elif c=="7":
                break
            else:
                print("Invalid")
    except Exception as e:
        print("Error:",e)
        sys.exit(1)
if _name=="main_":
    main()
