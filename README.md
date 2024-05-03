import win32net

def list_users():
    user_info = win32net.NetUserEnum(None, 0)
    users = [user['name'] for user in user_info]
    return users

if __name__ == "__main__":
    users = list_users()
    print("Usuários do Sistema Operacional Windows:")
    for user in users:
        print(user)
