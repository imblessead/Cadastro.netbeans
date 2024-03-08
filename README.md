# Cadastro.netbeans
Back-end

package com.projectone.projectfaculdade.folder.domain;

import java.util.Objects;


public class User {
   private String name;
   private String id;
   private String email;

    public User(String name, String id, String email) {
        this.name = name;
        this.id = id;
        this.email = email;
    }
   
  public User(){
      
      
  }
  
  

    @Override
    public String toString() {
        StringBuilder sb = new  StringBuilder();
        sb.append("User { ");
        sb.append("id=" ).append(getId());
        sb.append(", name= "). append(getName());
        sb.append(", email ="). append(getEmail());
        sb.append('}');
        return sb.toString();
      
    }

    @Override
    public int hashCode() {
        int hash = 5;
        hash = 29 * hash + Objects.hashCode(this.getId());
        return hash;
    }

    @Override
    public boolean equals(Object obj) {
        if (this == obj) {
            return true;
        }
        if (obj == null) {
            return false;
        }
        if (getClass() != obj.getClass()) {
            return false;
        }
        final User other = (User) obj;
        return Objects.equals(this.getId(), other.getId());
    }

    /**
     * @return the name
     */
    public String getName() {
        return name;
    }

    /**
     * @param name the name to set
     */
    public void setName(String name) {
        this.name = name;
    }

    /**
     * @return the id
     */
    public String getId() {
        return id;
    }

    /**
     * @param id the id to set
     */
    public void setId(String id) {
        this.id = id;
    }

    /**
     * @return the email
     */
    public String getEmail() {
        return email;
    }

    /**
     * @param email the email to set
     */
    public void setEmail(String email) {
        this.email = email;
    }
       
}
    
