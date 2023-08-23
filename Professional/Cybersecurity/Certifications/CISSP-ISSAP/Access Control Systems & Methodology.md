#professional #cybersecurity #certs #CISSP #CISSP-ISSAP #AccessControl 

Access control is the process of granting or denying access to resources based on a set of rules or policies. Access control systems and methodologies are important aspects of information security and are covered in the CISSP-ISSAP (Information Systems Security Architecture Professional) Body of Knowledge. This note will cover the different types of access control systems and methodologies.

## Access Control Systems

Access control systems can be categorized into four types:

1.  Discretionary Access Control (DAC)
2.  Mandatory Access Control (MAC)
3.  Role-Based Access Control (RBAC)
4.  Attribute-Based Access Control (ABAC)

### Discretionary Access Control #DAC

Discretionary Access Control (DAC) is a type of access control system that is used to restrict access to resources based on the identity of users and their permissions. DAC allows the owner of a resource to set access controls for that resource, which means that the owner has discretion over who can access the resource. This note will cover the different aspects of Discretionary Access Control as it relates to the CISSP-ISSAP (Information Systems Security Architecture Professional) Body of Knowledge.

#### How Discretionary Access Control Works

In Discretionary Access Control, each resource has an owner who is responsible for setting access controls for that resource. The owner can set access controls by specifying the users and groups that are allowed to access the resource, as well as the permissions that are granted to those users and groups. The access controls can be modified by the owner at any time, and the owner can also grant ownership of the resource to another user.

When a user attempts to access a resource, the access control system checks the user's identity and compares it to the access controls for the resource. If the user is authorized to access the resource, the access control system grants the user access based on the permissions that are associated with their user account. If the user is not authorized to access the resource, the access control system denies the user access.

#### Advantages of Discretionary Access Control

There are several advantages to using Discretionary Access Control:

1.  Flexibility: Discretionary Access Control provides the resource owner with the flexibility to grant or deny access to the resource as they see fit.
    
2.  Simplicity: Discretionary Access Control is relatively easy to implement and understand, which makes it a popular choice for small to medium-sized organizations.
    
3.  Granularity: Discretionary Access Control allows for fine-grained control over access to resources, which means that the owner can specify exactly which users and groups have access to the resource, and what level of access they have.
    

#### Limitations of Discretionary Access Control

There are also some limitations to using Discretionary Access Control:

1.  Lack of central control: Discretionary Access Control does not provide a centralized control mechanism, which means that the resource owner must set access controls for each resource individually.
    
2.  Difficulty in enforcing a consistent security policy: Discretionary Access Control can lead to inconsistencies in security policy enforcement, as each resource owner can set their own access controls.
    
3.  Lack of scalability: Discretionary Access Control can be difficult to manage in large organizations with a large number of resources and users.

### Mandatory Access Control #MAC

Mandatory Access Control (MAC) is a type of access control system that is used to restrict access to resources based on security labels that are assigned to each user, object, or resource. In this note, we will cover the different aspects of Mandatory Access Control as it relates to the CISSP-ISSAP (Information Systems Security Architecture Professional) Body of Knowledge.

#### How Mandatory Access Control Works

In Mandatory Access Control, each user, object, or resource is assigned a security label that defines its level of sensitivity or classification. Access to the resource is then restricted based on the security label of the user and the security label of the resource. If the security label of the user is lower than the security label of the resource, the user is denied access to the resource.

Mandatory Access Control systems are often used in government or military environments, where it is necessary to ensure that sensitive information is only accessed by authorized personnel.

#### Advantages of Mandatory Access Control

There are several advantages to using Mandatory Access Control:

1.  Greater control: Mandatory Access Control provides greater control over access to resources, as access is based on security labels that are assigned to each user and resource.
    
2.  Centralized control: Mandatory Access Control provides centralized control over access to resources, which makes it easier to enforce a consistent security policy.
    
3.  High-level security: Mandatory Access Control provides a high level of security, as access to resources is based on the security labels of the user and the resource.
    

#### Limitations of Mandatory Access Control

There are also some limitations to using Mandatory Access Control:

1.  Complexity: Mandatory Access Control is often more complex to implement and manage than other access control systems, due to the need for security labels and the associated policies.
    
2.  Inflexibility: Mandatory Access Control is often less flexible than other access control systems, as it relies on a fixed set of security labels and policies.
    
3.  Performance overhead: Mandatory Access Control can be resource-intensive, as it requires additional processing to check the security labels of each user and resource.

### Role-Based Access Control #RBAC

Role Based Access Control (RBAC) is a type of access control system that is used to restrict access to resources based on the roles that are assigned to each user. In this note, we will cover the different aspects of Role Based Access Control as it relates to the CISSP-ISSAP (Information Systems Security Architecture Professional) Body of Knowledge.

#### How Role Based Access Control Works

In Role Based Access Control, users are assigned roles based on their job functions, and access to resources is granted based on the roles assigned to the user. For example, a user with the role of "Manager" may have access to resources that are not available to a user with the role of "Clerk".

RBAC uses a set of rules to determine whether a user is authorized to access a particular resource based on their assigned role. These rules are typically defined in a policy that outlines the roles, the resources that are available to each role, and the actions that each role is allowed to perform.

#### Advantages of Role Based Access Control

There are several advantages to using Role Based Access Control:

1.  Simplicity: Role Based Access Control is often easier to implement and manage than other access control systems, as it is based on the user's role rather than individual permissions.
    
2.  Flexibility: Role Based Access Control is more flexible than other access control systems, as it can be easily adapted to changing business needs by adding or removing roles.
    
3.  Scalability: Role Based Access Control is highly scalable, as it can be used to manage access for large numbers of users across multiple systems.
    

#### Limitations of Role Based Access Control

There are also some limitations to using Role Based Access Control:

1.  Lack of granularity: Role Based Access Control may not provide the same level of granularity as other access control systems, as access is based on the user's role rather than individual permissions.
    
2.  Limited to predefined roles: Role Based Access Control is limited to the predefined roles that have been defined in the policy.
    
3.  Complexity in defining roles: Defining roles in a Role Based Access Control system can be complex, as it requires a deep understanding of the organization's business processes and the roles that are needed to support them.

### Attribute-Based Access Control #ABAC

Attribute Based Access Control (ABAC) is a type of access control system that is based on attributes or characteristics of the user, the resource, and the environment in which the access is requested. In this note, we will cover the different aspects of Attribute Based Access Control as it relates to the CISSP-ISSAP (Information Systems Security Architecture Professional) Body of Knowledge.

#### How Attribute Based Access Control Works

In Attribute Based Access Control, access to a resource is granted or denied based on the attributes associated with the user, the resource, and the environment in which the access is requested. These attributes may include a user's job title, location, time of day, and security clearance level, among others.

ABAC uses a set of policies to determine whether a user is authorized to access a particular resource based on the attributes associated with the user and the resource. These policies can be defined using a policy language that is capable of expressing complex conditions.

#### Advantages of Attribute Based Access Control

There are several advantages to using Attribute Based Access Control:

1.  Granularity: Attribute Based Access Control provides a high level of granularity in access control, as it can take into account a wide range of attributes associated with the user, the resource, and the environment in which the access is requested.
    
2.  Flexibility: Attribute Based Access Control is highly flexible, as policies can be easily adapted to changing business needs by modifying the attributes used in the policies.
    
3.  Scalability: Attribute Based Access Control is highly scalable, as it can be used to manage access for large numbers of users and resources across multiple systems.
    

#### Limitations of Attribute Based Access Control

There are also some limitations to using Attribute Based Access Control:

1.  Complexity: Attribute Based Access Control can be complex to implement and manage, as it requires the use of a policy language to define policies.
    
2.  Policy management: Managing policies in an Attribute Based Access Control system can be challenging, as policies can become complex and difficult to understand over time.
    
3.  Performance impact: The evaluation of policies in an Attribute Based Access Control system can impact performance, particularly when policies are complex or when there are a large number of attributes to consider.

## Access Control Methodology

Access control methodologies are the processes and procedures used to implement access control systems. The three access control methodologies are:

1.  Identification and Authentication #iam #Icam #idam
2.  #Authorization
3.  #Accountability

### Identification and Authentication

Identification and Authentication are key components of Access Control Systems and Methodology, as they enable the system to determine who is requesting access to a resource, and whether that access should be granted based on the user's identity and level of authentication. In this note, we will cover the different aspects of Identification and Authentication as it relates to the CISSP-ISSAP (Information Systems Security Architecture Professional) Body of Knowledge.

#### Identification

#Identification is the process of establishing the identity of a user who is requesting access to a resource. This involves the user providing some form of identifier, such as a username or email address. Identification does not, by itself, establish that the user is who they claim to be, but it does enable the system to track the user's activities and permissions.

#### Authentication

Authentication is the process of verifying that the user is who they claim to be. This involves the user providing some form of credential, such as a password or smart card, which is then compared to a stored value to verify the user's identity. Authentication provides a higher level of assurance that the user is authorized to access the resource.

##### Types of Authentication

There are several types of authentication that can be used in an Access Control System, including:

1.  Something you know - such as a password or PIN
2.  Something you have - such as a smart card or token
3.  Something you are - such as a fingerprint or other biometric characteristic

##### Multifactor Authentication #MFA

Multifactor #Authentication is the use of two or more types of authentication, such as a password and a smart card, to increase the level of assurance that the user is who they claim to be. This can help to prevent unauthorized access to resources even if one factor is compromised.

### Authorization

#Authorization is the process of granting or denying access to a resource. In this process, access control policies are enforced, and access is granted based on the user's role, attributes, or security clearance level. See the @AccessControlMethods

Authorization is a critical component of Access Control Systems and Methodology, as it determines what actions a user is allowed to perform on a resource once their identity has been established and authenticated. In this note, we will cover the different aspects of Authorization as it relates to the CISSP-ISSAP (Information Systems Security Architecture Professional) Body of Knowledge.

### Accountability

#Accountability is a critical component of Access Control Systems and Methodology, as it ensures that all actions taken on a system can be traced back to the individual who performed them. In this note, we will cover the different aspects of Accountability as it relates to the CISSP-ISSAP (Information Systems Security Architecture Professional) Body of Knowledge.

#### Audit Trails

#Audit Trails are one of the primary methods used to ensure Accountability in an Access Control System. An Audit Trail is a record of all activity on a system, including who performed the activity, what action was taken, and when the action was taken. Audit Trails can be used to monitor activity on a system in real-time or to investigate incidents that have already occurred.

#### Non-Repudiation

#Non-Repudiation is a concept that ensures that a user cannot deny that they performed a specific action. Non-Repudiation is typically achieved through the use of digital signatures or other methods of authentication that can be used to verify that a specific user performed a specific action.

#### Logging

#Logging is the process of recording activity on a system. Logging can be used to create an Audit Trail, but it can also be used for other purposes, such as performance monitoring or troubleshooting. When implementing logging, it is important to ensure that the logs are tamper-proof and that they cannot be modified by unauthorized users.

#### Forensic Analysis

#Forensic Analysis is the process of investigating incidents after they have occurred. Forensic Analysis is often used in conjunction with Audit Trails and Logging to investigate incidents and determine the cause and extent of a security breach. Forensic Analysis can also be used to gather evidence for use in legal proceedings.

## Access Control Administration and Management Concepts

Access control administration and management are important aspects of access control systems and methodologies. The goal of access control administration and management is to ensure that access control systems are implemented and maintained effectively to provide secure access to resources. This note will cover the different concepts related to access control administration and management as it relates to the CISSP-ISSAP (Information Systems Security Architecture Professional) Body of Knowledge.

### Access Control Administration

Access control administration involves the following activities:

1.  Policy and procedure development
2.  User administration
3.  Access control monitoring and reporting
4.  Audit and compliance management

#### Policy and Procedure Development

Policy and procedure development is the process of creating and documenting the policies and procedures for the access control system. The policies and procedures should be based on the organization's security requirements and should provide clear guidelines for access control management. The policies and procedures should be reviewed regularly and updated as needed.

#### User Administration

User administration is the process of managing user accounts and access rights. This process involves creating, modifying, and deleting user accounts and managing their access rights to resources. User administration should be based on the principle of least privilege, where users are granted only the minimum access required to perform their job functions.

#### Access Control Monitoring and Reporting

Access control monitoring and reporting is the process of monitoring access to resources and generating reports on access activities. This process helps to identify any unauthorized access attempts and provides visibility into access patterns. Access control monitoring and reporting should be performed regularly and should be based on the organization's security requirements.

#### Audit and Compliance Management

Audit and compliance management is the process of ensuring that the access control system is in compliance with regulatory and industry standards. This process involves regular audits and assessments to ensure that the system is implemented and maintained in a secure and compliant manner.

### Access Control Management

Access control management involves the following activities:

1.  Access control system selection and implementation
2.  Access control system testing and evaluation
3.  Access control system maintenance and updates

#### Access Control System Selection and Implementation

Access control system selection and implementation is the process of selecting the appropriate access control system and implementing it in the organization. The selection of the access control system should be based on the organization's security requirements, and the implementation should be based on industry standards and best practices.

#### Access Control System Testing and Evaluation

Access control system testing and evaluation is the process of testing the access control system to ensure that it is working as intended. This process involves performing vulnerability assessments, penetration testing, and other security testing to identify any vulnerabilities in the system.

#### Access Control System Maintenance and Updates

Access control system maintenance and updates are the processes of ensuring that the access control system is updated and maintained to provide ongoing security. This process involves regular updates to the access control system software, hardware, and firmware, as well as regular security patches and updates.

## Conclusion

Access control systems and methodologies are important aspects of information security. They are used to control access to resources and ensure that only authorized users have access. The different types of access control systems and methodologies are used in different environments, and the selection of the appropriate system and methodology is dependent on the organization's specific needs and requirements.