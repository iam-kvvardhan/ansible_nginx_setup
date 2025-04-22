Your notes are clear and concise. Here's a more polished version with added structure and formatting to make it look better in your GitHub repo, using **markdown** syntax:

---

## **Ansible Setup for Passwordless SSH Authentication**

### **Pre-requisite: Passwordless Authentication**

Before setting up Ansible, make sure you have configured passwordless SSH authentication between your **Ansible server** and **target server**. If not, follow the steps below.

### **1. Create Two Servers (Ansible Server & Target Server)**

You will need two servers:

- **Ansible Server**: The machine from which you will run Ansible commands.
- **Target Server**: The machine that will be managed by Ansible.

**Install Ansible on Both Servers:**

On both servers, update the package list and install Ansible:

```bash
sudo apt update
sudo apt install ansible
```

---

### **2. Set Up Passwordless SSH Authentication**

#### **Step 1: Generate SSH Keys on Ansible Server**

1. On the **Ansible server**, run the following command to generate SSH keys:

   ```bash
   ssh-keygen
   ```

2. Press **Enter** to accept the default directory (`~/.ssh/id_rsa`) to save the SSH key.

3. After the key is generated, copy the **public key** to your clipboard:

   ```bash
   cat ~/.ssh/id_rsa.pub
   ```

   Copy the output from this command.

---

#### **Step 2: Set Up SSH Keys on Target Server**

1. On the **Target server**, run the following command to generate SSH keys (if not already done):

   ```bash
   ssh-keygen
   ```

2. Press **Enter** to accept the default directory to save the SSH key.

3. After generating the key, go to the **Target server**’s `.ssh` directory:

   ```bash
   cd ~/.ssh
   ```

4. Open the `authorized_keys` file and paste the **public key** from the Ansible server:

   ```bash
   echo "<Ansible server public key>" >> authorized_keys
   ```

5. Save the file and exit.

---

### **3. Verify Passwordless SSH Authentication**

Now, from the **Ansible server**, test the SSH connection to the **Target server**:

```bash
ssh target_user@<target_server_ip>
```

You should be able to log in without being prompted for a password.

---

### **Conclusion**

You have successfully configured **passwordless SSH authentication** between the **Ansible server** and the **Target server**. This setup is essential for running Ansible commands without requiring a password every time.

---
