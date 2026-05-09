<p align="center">
<img src="https://i.imgur.com/DW1yKLs.jpeg" alt="Traffic Examination"/>
</p>

<h1>Entra ID Identity Lab</h1>
This tutorial outlines the configuration and validation of backup and recovery for a Windows Server virtual machine using Azure-native services.<br> This lab simulates real-world disaster recovery scenarios by backing up critical system data and successfully restoring resources. <br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop (RDC/Windows App)
- Azure Recovery Services Vault
- Notepad/Notes App (Needed for saving usernames, passwords, and other information)

<h2>Operating Systems Used </h2>

- Windows Server 2025

<h2>List of Prerequisites</h2>

- Basic/General Understanding of Microsoft Azure
- Azure Subscription/Azure Account(Portal) created
- Resource Group created within your Azure portal
- Windows Server Virtual Machine(Windows) created within your Azure portal with the resource group you've created previously

<h2>Configuration Steps</h2>
<ol>
  <li>
    <strong>Create a Windows Server Virtual Machine</strong>
    <ul>
      <li>Deployed a Windows Server 2019 VM in Azure</li>
      <li>Configured networking and NSG rules to allow temporary RDP access</li>
      <li>Verified successful login and system readiness</li>
    </ul>
  </li>

  <li>
    <strong>Create a Recovery Services Vault</strong>
    <ul>
      <li>Created a Recovery Services Vault in the same region as the VM</li>
      <li>Configured default backup policies</li>
    </ul>
  </li>

  <li>
    <strong>Enable Azure VM Backup</strong>
    <ul>
      <li>Associated the Windows Server VM with the Recovery Services Vault</li>
      <li>Enabled Azure Backup protection</li>
      <li>Verified that the initial backup completed successfully</li>
    </ul>
  </li>

  <li>
    <strong>Simulate a Failure Scenario</strong>
    <ul>
      <li>Deleted a test file or user object from the Windows Server VM</li>
      <li>This simulated accidental data loss or administrative error</li>
    </ul>
  </li>

  <li>
    <strong>Restore from Backup</strong>
    <ul>
      <li>Initiated a restore operation from the Recovery Services Vault</li>
      <li>Performed a file-level restore</li>
      <li>Verified the deleted resource was successfully recovered</li>
    </ul>
  </li>
</ol>

<h2>Results</h2>
<ul>
  <li>Azure VM backup completed successfully</li>
  <li>Restore operation recovered deleted data without errors</li>
  <li>System functionality and access were fully restored</li>
</ul>

<h2>Key Skills Demonstrated</h2>
<ul>
  <li>Azure virtual machine administration</li>
  <li>Cloud-based backup and disaster recovery</li>
  <li>Recovery Services Vault configuration</li>
  <li>Failure simulation and recovery validation</li>
  <li>System reliability and availability best practices</li>
</ul>



