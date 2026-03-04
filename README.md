
<!-- GitHub Portfolio Project: AD Lab in Azure -->

<div class="project">

  <h2>Active Directory Lab in Azure</h2>
  <p><strong>Summary:</strong> Setting up an Active Directory environment in Microsoft Azure using virtual machines and PowerShell for bulk user creation.</p>

  <!-- Section 1: AD Infrastructure -->
  <h3>1. Preparing AD Infrastructure in Azure</h3>
  <ul>
    <li>Create a <strong>Resource Group</strong> and a <strong>Virtual Network</strong> in Azure for the AD lab.</li>
    <li>Set up two VMs:
      <ul>
        <li><strong>Domain Controller:</strong> Windows Server 2022</li>
        <li><strong>Client:</strong> Windows 10</li>
      </ul>
    </li>
    <li>Assign a <strong>static private IP</strong> to the Domain Controller for reliable DNS.</li>
    <li>Disable Windows Firewall on the Domain Controller for lab simplicity.</li>
    <li>Configure the client’s DNS to point to the Domain Controller IP instead of Azure’s default DNS.</li>
    <li>Restart the client, test connectivity (ping DC from client), and confirm DNS configuration using <code>ipconfig /all</code>.</li>
  </ul>

  <!-- Screenshot placeholder -->
  <p><em>Insert screenshots of your Azure portal setup here</em></p>

  <!-- Section 2: PowerShell User Creation -->
  <h3>2. Creating Users with PowerShell</h3>
  <ul>
    <li>Enable remote access for all domain users on the client using system settings (or Group Policy for larger environments).</li>
    <li>Understand Group Policy Objects (GPOs) to manage settings across multiple computers.</li>
    <li>Open <strong>PowerShell ISE as Administrator</strong> on the Domain Controller (DC1).</li>
    <li>Run a PowerShell script to create up to 10,000 user accounts in the Employees OU.
      <ul>
        <li>All users get the default password: <code>Password1</code>.</li>
        <li>Users are added to the <strong>Domain Users</strong> group.</li>
      </ul>
    </li>
    <li>Test logins on the client machine to ensure new profiles are created on first login.</li>
  </ul>

  <!-- Screenshot placeholder -->
  <p><em>Insert screenshots of PowerShell script and login tests here</em></p>

</div>
