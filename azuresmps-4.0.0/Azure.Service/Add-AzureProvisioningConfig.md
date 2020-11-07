---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 0B3EF123-8424-4CCA-95E8-01301B70CBDC
online version: ''
schema: 2.0.0
ms.openlocfilehash: f84db81f51a4f8d0da605917f99e14c1721cd89d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967828"
---
# <span data-ttu-id="ea5af-101">Add-AzureProvisioningConfig</span><span class="sxs-lookup"><span data-stu-id="ea5af-101">Add-AzureProvisioningConfig</span></span>

## <span data-ttu-id="ea5af-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ea5af-102">SYNOPSIS</span></span>
<span data-ttu-id="ea5af-103">新增 Azure 虛擬機器的置備設定。</span><span class="sxs-lookup"><span data-stu-id="ea5af-103">Adds provisioning configuration for an Azure virtual machine.</span></span>

## <span data-ttu-id="ea5af-104">句法</span><span class="sxs-lookup"><span data-stu-id="ea5af-104">SYNTAX</span></span>

### <span data-ttu-id="ea5af-105">Windows (預設) </span><span class="sxs-lookup"><span data-stu-id="ea5af-105">Windows (Default)</span></span>
```
Add-AzureProvisioningConfig -VM <IPersistentVM> [-DisableGuestAgent] [-CustomDataFile <String>] [-Windows]
 [-AdminUsername <String>] [-Password <String>] [-ResetPasswordOnFirstLogon] [-DisableAutomaticUpdates]
 [-NoRDPEndpoint] [-TimeZone <String>] [-Certificates <CertificateSettingList>] [-EnableWinRMHttp]
 [-DisableWinRMHttps] [-WinRMCertificate <X509Certificate2>] [-X509Certificates <X509Certificate2[]>]
 [-NoExportPrivateKey] [-NoWinRMEndpoint] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="ea5af-106">Linux</span><span class="sxs-lookup"><span data-stu-id="ea5af-106">Linux</span></span>
```
Add-AzureProvisioningConfig -VM <IPersistentVM> [-DisableGuestAgent] [-Linux] [-LinuxUser <String>]
 [-DisableSSH] [-NoSSHEndpoint] [-NoSSHPassword] [-SSHPublicKeys <SSHPublicKeyList>]
 [-SSHKeyPairs <SSHKeyPairList>] [-CustomDataFile <String>] [-Password <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="ea5af-107">WindowsDomain</span><span class="sxs-lookup"><span data-stu-id="ea5af-107">WindowsDomain</span></span>
```
Add-AzureProvisioningConfig -VM <IPersistentVM> [-DisableGuestAgent] [-CustomDataFile <String>]
 -AdminUsername <String> [-WindowsDomain] [-Password <String>] [-ResetPasswordOnFirstLogon]
 [-DisableAutomaticUpdates] [-NoRDPEndpoint] [-TimeZone <String>] [-Certificates <CertificateSettingList>]
 -JoinDomain <String> -Domain <String> -DomainUserName <String> -DomainPassword <String>
 [-MachineObjectOU <String>] [-EnableWinRMHttp] [-DisableWinRMHttps] [-WinRMCertificate <X509Certificate2>]
 [-X509Certificates <X509Certificate2[]>] [-NoExportPrivateKey] [-NoWinRMEndpoint] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="ea5af-108">說明</span><span class="sxs-lookup"><span data-stu-id="ea5af-108">DESCRIPTION</span></span>
<span data-ttu-id="ea5af-109">**AzureProvisioningConfig** Cmdlet 會將預配配置資訊新增至 Azure 虛擬機器設定。</span><span class="sxs-lookup"><span data-stu-id="ea5af-109">The **Add-AzureProvisioningConfig** cmdlet adds provisioning configuration information to an Azure virtual machine configuration.</span></span>
<span data-ttu-id="ea5af-110">您可以使用 [配置] 物件來建立虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="ea5af-110">You can use the configuration object to create a virtual machine.</span></span>

<span data-ttu-id="ea5af-111">這個 Cmdlet 支援不同的置備設定，包括獨立 Windows 伺服器、加入 Active Directory 網域的 Windows 伺服器，以及 Linux 版伺服器。</span><span class="sxs-lookup"><span data-stu-id="ea5af-111">This cmdlet supports different provisioning configurations, including standalone Windows servers, Windows servers joined to an Active Directory domain, and Linux-based servers.</span></span>

<span data-ttu-id="ea5af-112">若要建立 Active Directory 網域加入的伺服器，請指定 Active Directory 網域的完整功能變數名稱，以及具有將虛擬機器加入至網域許可權的使用者的網域認證。</span><span class="sxs-lookup"><span data-stu-id="ea5af-112">To create an Active Directory domain joined server, specify the fully qualified domain name of the Active Directory domain and the domain credentials of a user who has permission to join the virtual machine to the domain.</span></span>

## <span data-ttu-id="ea5af-113">示例</span><span class="sxs-lookup"><span data-stu-id="ea5af-113">EXAMPLES</span></span>

### <span data-ttu-id="ea5af-114">範例1：建立獨立的虛擬機器</span><span class="sxs-lookup"><span data-stu-id="ea5af-114">Example 1: Create a standalone virtual machine</span></span>
```
PS C:\> New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" | New-AzureVM -ServiceName "ContosoService"
```

<span data-ttu-id="ea5af-115">這個命令會使用 **AzureVMConfig** Cmdlet 來建立虛擬機器設定物件。</span><span class="sxs-lookup"><span data-stu-id="ea5af-115">This command creates a virtual machine configuration object by using the **New-AzureVMConfig** cmdlet.</span></span>
<span data-ttu-id="ea5af-116">命令會使用管線運算子，將該物件傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ea5af-116">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ea5af-117">目前的 Cmdlet 會為執行 Windows 作業系統的虛擬機器新增置備配置。</span><span class="sxs-lookup"><span data-stu-id="ea5af-117">The current cmdlet adds provisioning configuration for a virtual machine that runs the Windows operating system.</span></span>
<span data-ttu-id="ea5af-118">此設定包含管理員的使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="ea5af-118">The configuration includes the administrator user name and password.</span></span>
<span data-ttu-id="ea5af-119">該命令會將設定傳遞到 **新的 add-azurevm** Cmdlet，這會建立虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="ea5af-119">The command passes the configuration to the **New-AzureVM** cmdlet, which creates the virtual machine.</span></span>

### <span data-ttu-id="ea5af-120">範例2：建立加入網域的虛擬機器</span><span class="sxs-lookup"><span data-stu-id="ea5af-120">Example 2: Create a domain joined virtual machine</span></span>
```
PS C:\> New-AzureVMConfig -Name "DomainVM" -InstanceSize Small -ImageName "Image09" | Add-AzureProvisioningConfig -WindowsDomain -Password "password" -AdminUsername "AdminMain" -ResetPasswordOnFirstLogon -JoinDomain "contoso.com" -Domain "contoso" -DomainUserName "DomainAdminUser" -DomainPassword "DomainPassword" -MachineObjectOU 'OU=AzureVMs,DC=contoso,DC=com' | New-AzureVM -ServiceName "ContosoService"
```

<span data-ttu-id="ea5af-121">這個命令會建立虛擬機器設定物件，然後將它傳遞到目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ea5af-121">This command creates a virtual machine configuration object, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="ea5af-122">目前的 Cmdlet 會新增虛擬機器的置備設定，以與 contoso 網域加入。</span><span class="sxs-lookup"><span data-stu-id="ea5af-122">The current cmdlet adds provisioning configuration for a virtual machine to be joined with the contoso domain.</span></span>
<span data-ttu-id="ea5af-123">此命令包含將虛擬機器加入至網域所需的使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="ea5af-123">The command includes user name and password necessary to join the virtual machine to the domain.</span></span>
<span data-ttu-id="ea5af-124">此設定要求使用者在第一次登入時變更使用者密碼。</span><span class="sxs-lookup"><span data-stu-id="ea5af-124">The configuration requires the user to change the user password at the first logon.</span></span>
<span data-ttu-id="ea5af-125">命令會根據置備物件建立虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="ea5af-125">The command creates the virtual machine based on the provisioning object.</span></span>

### <span data-ttu-id="ea5af-126">範例3：建立以 Linux 為基礎的虛擬機器</span><span class="sxs-lookup"><span data-stu-id="ea5af-126">Example 3: Create a Linux-based virtual machine</span></span>
```
PS C:\> New-AzureVMConfig -Name "LinuxVM" -InstanceSize Small -ImageName "LinuxImage03" | Add-AzureProvisioningConfig -Linux -LinuxUser "LinuxRoot" -Password "password" | New-AzureVM -ServiceName "ContosoService"
```

<span data-ttu-id="ea5af-127">這個命令會建立虛擬機器設定物件，然後將它傳遞到目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ea5af-127">This command creates a virtual machine configuration object, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="ea5af-128">目前的 Cmdlet 會為執行 Linux 作業系統的虛擬機器新增預配配置。</span><span class="sxs-lookup"><span data-stu-id="ea5af-128">The current cmdlet adds provisioning configuration for a virtual machine that runs the Linux operating system.</span></span>
<span data-ttu-id="ea5af-129">此設定包括超級使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="ea5af-129">The configuration includes the root user name and password.</span></span>
<span data-ttu-id="ea5af-130">命令會根據置備物件建立虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="ea5af-130">The command creates the virtual machine based on the provisioning object.</span></span>

### <span data-ttu-id="ea5af-131">範例4：建立包含 WinRM 憑證的虛擬機器</span><span class="sxs-lookup"><span data-stu-id="ea5af-131">Example 4: Create a virtual machine that includes certificates for WinRM</span></span>
```
PS C:\> $certs = Get-ChildItem Cert:\CurrentUser\My
New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image11" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -WinRMCertificate $certs[0] -X509Certificates $certs[1], $certs[2] | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

<span data-ttu-id="ea5af-132">第一個命令會從憑證存放區取得憑證，然後將它們儲存在 $certs 的陣列變數中。</span><span class="sxs-lookup"><span data-stu-id="ea5af-132">The first command gets certificates from a certificate store, and then stores them in the $certs array variable.</span></span>

<span data-ttu-id="ea5af-133">第二個命令會建立虛擬機器設定物件，然後將它傳遞到目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ea5af-133">The second command creates a virtual machine configuration object, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="ea5af-134">目前的 Cmdlet 會新增包括 WinRM 憑證的預配配置。</span><span class="sxs-lookup"><span data-stu-id="ea5af-134">The current cmdlet adds provisioning configuration that includes certificates for WinRM.</span></span>
<span data-ttu-id="ea5af-135">命令會根據置備物件建立虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="ea5af-135">The command creates the virtual machine based on the provisioning object.</span></span>

### <span data-ttu-id="ea5af-136">範例5：建立已在 HTTP 上啟用 WinRM 的虛擬機器</span><span class="sxs-lookup"><span data-stu-id="ea5af-136">Example 5: Create a virtual machine that has WinRM enabled over HTTP</span></span>
```
PS C:\> New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image14" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -EnableWinRMHttp | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

<span data-ttu-id="ea5af-137">這個命令會建立虛擬機器設定物件，然後將它傳遞到目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ea5af-137">This command creates a virtual machine configuration object, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="ea5af-138">目前的 Cmdlet 會新增已在 HTTP 上啟用 WinRM 的置備配置。</span><span class="sxs-lookup"><span data-stu-id="ea5af-138">The current cmdlet adds provisioning configuration that has WinRM enabled over HTTP.</span></span>
<span data-ttu-id="ea5af-139">命令會根據置備物件建立虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="ea5af-139">The command creates the virtual machine based on the provisioning object.</span></span>

### <span data-ttu-id="ea5af-140">範例6：建立已在 HTTPS 上停用 WinRM 的虛擬機器</span><span class="sxs-lookup"><span data-stu-id="ea5af-140">Example 6: Create a virtual machine that has WinRM disabled over HTTPS</span></span>
```
PS C:\> New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -DisableWinRMHttps | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

<span data-ttu-id="ea5af-141">這個命令會建立虛擬機器設定物件，然後將它傳遞到目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ea5af-141">This command creates a virtual machine configuration object, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="ea5af-142">目前的 Cmdlet 會新增在 HTTPS 上停用 WinRM 的置備設定。</span><span class="sxs-lookup"><span data-stu-id="ea5af-142">The current cmdlet adds provisioning configuration that disables WinRM over HTTPS.</span></span>
<span data-ttu-id="ea5af-143">命令會根據置備物件建立虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="ea5af-143">The command creates the virtual machine based on the provisioning object.</span></span>

### <span data-ttu-id="ea5af-144">範例7：建立沒有金鑰匯出的虛擬機器</span><span class="sxs-lookup"><span data-stu-id="ea5af-144">Example 7: Create a virtual machine with no key export</span></span>
```
PS C:\> $certs = Get-ChildItem Cert:\CurrentUser\My
New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -X509Certificates $certs[0], $certs[1] -NoExportPrivateKey | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

<span data-ttu-id="ea5af-145">第一個命令會從憑證存放區取得憑證，然後將它們儲存在 $certs 的陣列變數中。</span><span class="sxs-lookup"><span data-stu-id="ea5af-145">The first command gets certificates from a certificate store, and then stores them in the $certs array variable.</span></span>

<span data-ttu-id="ea5af-146">第二個命令會建立虛擬機器設定物件，然後將它傳遞到目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ea5af-146">The second command creates a virtual machine configuration object, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="ea5af-147">目前的 Cmdlet 會新增包含憑證的虛擬機器的提供設定，但不會匯出私人金鑰。</span><span class="sxs-lookup"><span data-stu-id="ea5af-147">The current cmdlet adds provisioning configuration for a virtual machine that includes certificates and does not export private keys.</span></span>
<span data-ttu-id="ea5af-148">命令會根據置備物件建立虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="ea5af-148">The command creates the virtual machine based on the provisioning object.</span></span>

## <span data-ttu-id="ea5af-149">參數</span><span class="sxs-lookup"><span data-stu-id="ea5af-149">PARAMETERS</span></span>

### <span data-ttu-id="ea5af-150">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="ea5af-150">-AdminUsername</span></span>
<span data-ttu-id="ea5af-151">指定此設定在虛擬機器上建立之系統管理員帳戶的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="ea5af-151">Specifies the user name of the Administrator account that this configuration creates on the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea5af-152">-憑證</span><span class="sxs-lookup"><span data-stu-id="ea5af-152">-Certificates</span></span>
<span data-ttu-id="ea5af-153">指定此設定在虛擬機器上安裝的一組憑證。</span><span class="sxs-lookup"><span data-stu-id="ea5af-153">Specifies a set of certificates that this configuration installs on the virtual machine.</span></span>

```yaml
Type: CertificateSettingList
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea5af-154">-CustomDataFile</span><span class="sxs-lookup"><span data-stu-id="ea5af-154">-CustomDataFile</span></span>
<span data-ttu-id="ea5af-155">指定虛擬機器的資料檔案。</span><span class="sxs-lookup"><span data-stu-id="ea5af-155">Specifies a data file for the virtual machine.</span></span>
<span data-ttu-id="ea5af-156">這個 Cmdlet 會將檔案的內容編碼為 Base64。</span><span class="sxs-lookup"><span data-stu-id="ea5af-156">This cmdlet encodes the contents of the file as Base64.</span></span>
<span data-ttu-id="ea5af-157">檔案長度必須小於 64 kb。</span><span class="sxs-lookup"><span data-stu-id="ea5af-157">The file must be less than 64 kilobytes long.</span></span>

<span data-ttu-id="ea5af-158">如果客體作業系統是 Windows 作業系統，此設定會將這個資料儲存為一個名為%SYSTEMDRIVE%\AzureData\CustomData.bin. 的二進位檔案</span><span class="sxs-lookup"><span data-stu-id="ea5af-158">If the guest operating system is the Windows operating system, this configuration saves this data as a binary file named %SYSTEMDRIVE%\AzureData\CustomData.bin.</span></span>

<span data-ttu-id="ea5af-159">如果客體作業系統是 Linux，此設定就會使用 ovf-env.xml 檔案傳遞資料。</span><span class="sxs-lookup"><span data-stu-id="ea5af-159">If the guest operating system is Linux, this configuration passes the data by using the ovf-env.xml file.</span></span>
<span data-ttu-id="ea5af-160">[配置] 會將該檔案複製到/var/lib/waagent 目錄。</span><span class="sxs-lookup"><span data-stu-id="ea5af-160">Configuration copies that file to the /var/lib/waagent directory.</span></span>
<span data-ttu-id="ea5af-161">此代理程式也會在/var/lib/waagent/CustomData. 中儲存 Base64 編碼資料</span><span class="sxs-lookup"><span data-stu-id="ea5af-161">The agent also stores the Base64 encoded data in /var/lib/waagent/CustomData.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea5af-162">-DisableAutomaticUpdates</span><span class="sxs-lookup"><span data-stu-id="ea5af-162">-DisableAutomaticUpdates</span></span>
<span data-ttu-id="ea5af-163">表示此設定會停用自動更新。</span><span class="sxs-lookup"><span data-stu-id="ea5af-163">Indicates that this configuration disables automatic updates.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea5af-164">-DisableGuestAgent</span><span class="sxs-lookup"><span data-stu-id="ea5af-164">-DisableGuestAgent</span></span>
<span data-ttu-id="ea5af-165">表示此設定會將基礎結構停成服務 (IaaS) 來賓代理程式。</span><span class="sxs-lookup"><span data-stu-id="ea5af-165">Indicates that this configuration disables the infrastructure as a service (IaaS) guest agent.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea5af-166">-DisableSSH</span><span class="sxs-lookup"><span data-stu-id="ea5af-166">-DisableSSH</span></span>
<span data-ttu-id="ea5af-167">表示此設定會停用 SSH。</span><span class="sxs-lookup"><span data-stu-id="ea5af-167">Indicates that this configuration disables SSH.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea5af-168">-DisableWinRMHttps</span><span class="sxs-lookup"><span data-stu-id="ea5af-168">-DisableWinRMHttps</span></span>
<span data-ttu-id="ea5af-169">指示此設定會停用 HTTPS 上的 Windows 遠端系統管理 (WinRM) 。</span><span class="sxs-lookup"><span data-stu-id="ea5af-169">Indicates that this configuration disables Windows Remote Management (WinRM) on HTTPS.</span></span>
<span data-ttu-id="ea5af-170">根據預設，WinRM 是透過 HTTPS 啟用的。</span><span class="sxs-lookup"><span data-stu-id="ea5af-170">By default, WinRM is enabled over HTTPS.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea5af-171">-網域</span><span class="sxs-lookup"><span data-stu-id="ea5af-171">-Domain</span></span>
<span data-ttu-id="ea5af-172">指定擁有將電腦新增至網域許可權的帳戶之網域的名稱。</span><span class="sxs-lookup"><span data-stu-id="ea5af-172">Specifies the name of the domain of the account that has permission to add the computer to a domain.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea5af-173">-DomainPassword</span><span class="sxs-lookup"><span data-stu-id="ea5af-173">-DomainPassword</span></span>
<span data-ttu-id="ea5af-174">指定擁有將電腦新增至網域許可權之使用者帳戶的密碼。</span><span class="sxs-lookup"><span data-stu-id="ea5af-174">Specifies the password of the user account that has permission to add the computer to a domain.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea5af-175">-DomainUserName</span><span class="sxs-lookup"><span data-stu-id="ea5af-175">-DomainUserName</span></span>
<span data-ttu-id="ea5af-176">指定擁有將電腦新增至網域許可權的使用者帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="ea5af-176">Specifies the name of the user account that has permission to add the computer to a domain.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea5af-177">-EnableWinRMHttp</span><span class="sxs-lookup"><span data-stu-id="ea5af-177">-EnableWinRMHttp</span></span>
<span data-ttu-id="ea5af-178">指示此設定啟用 WinRM over HTTP。</span><span class="sxs-lookup"><span data-stu-id="ea5af-178">Indicates that this configuration enables WinRM over HTTP.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea5af-179">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ea5af-179">-InformationAction</span></span>
<span data-ttu-id="ea5af-180">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="ea5af-180">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ea5af-181">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="ea5af-181">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ea5af-182">持續</span><span class="sxs-lookup"><span data-stu-id="ea5af-182">Continue</span></span>
- <span data-ttu-id="ea5af-183">理會</span><span class="sxs-lookup"><span data-stu-id="ea5af-183">Ignore</span></span>
- <span data-ttu-id="ea5af-184">看</span><span class="sxs-lookup"><span data-stu-id="ea5af-184">Inquire</span></span>
- <span data-ttu-id="ea5af-185">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ea5af-185">SilentlyContinue</span></span>
- <span data-ttu-id="ea5af-186">停止</span><span class="sxs-lookup"><span data-stu-id="ea5af-186">Stop</span></span>
- <span data-ttu-id="ea5af-187">封存</span><span class="sxs-lookup"><span data-stu-id="ea5af-187">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea5af-188">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ea5af-188">-InformationVariable</span></span>
<span data-ttu-id="ea5af-189">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="ea5af-189">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea5af-190">-JoinDomain</span><span class="sxs-lookup"><span data-stu-id="ea5af-190">-JoinDomain</span></span>
<span data-ttu-id="ea5af-191">指定要加入之網域 (FQDN) 的完整功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="ea5af-191">Specifies the fully qualified domain name (FQDN) of the domain to join.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea5af-192">-Linux</span><span class="sxs-lookup"><span data-stu-id="ea5af-192">-Linux</span></span>
<span data-ttu-id="ea5af-193">表示此設定會建立 Linux 配置。</span><span class="sxs-lookup"><span data-stu-id="ea5af-193">Indicates that this configuration creates a Linux configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea5af-194">-LinuxUser</span><span class="sxs-lookup"><span data-stu-id="ea5af-194">-LinuxUser</span></span>
<span data-ttu-id="ea5af-195">指定此設定在虛擬機器上建立之 Linux 系統管理員帳戶的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="ea5af-195">Specifies the user name of the Linux administrative account that this configuration creates on the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea5af-196">-MachineObjectOU</span><span class="sxs-lookup"><span data-stu-id="ea5af-196">-MachineObjectOU</span></span>
<span data-ttu-id="ea5af-197">指定在設定建立電腦帳戶的組織單位 (OU) 的完整名稱。</span><span class="sxs-lookup"><span data-stu-id="ea5af-197">Specifies the fully qualified name of the organizational unit (OU) in which the configuration creates the computer account.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea5af-198">-NoExportPrivateKey</span><span class="sxs-lookup"><span data-stu-id="ea5af-198">-NoExportPrivateKey</span></span>
<span data-ttu-id="ea5af-199">指示此設定不會上傳私用金鑰。</span><span class="sxs-lookup"><span data-stu-id="ea5af-199">Indicates that this configuration does not upload the private key.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea5af-200">-NoRDPEndpoint</span><span class="sxs-lookup"><span data-stu-id="ea5af-200">-NoRDPEndpoint</span></span>
<span data-ttu-id="ea5af-201">表示此設定會建立沒有遠端桌面端點的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="ea5af-201">Indicates that this configuration creates a virtual machine without a remote desktop endpoint.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea5af-202">-NoSSHEndpoint</span><span class="sxs-lookup"><span data-stu-id="ea5af-202">-NoSSHEndpoint</span></span>
<span data-ttu-id="ea5af-203">表示此設定會建立沒有 SSH 端點的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="ea5af-203">Indicates that this configuration creates a virtual machine without an SSH endpoint.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea5af-204">-NoSSHPassword</span><span class="sxs-lookup"><span data-stu-id="ea5af-204">-NoSSHPassword</span></span>
<span data-ttu-id="ea5af-205">表示此設定會建立沒有 SSH 密碼的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="ea5af-205">Indicates that this configuration creates a virtual machine without an SSH password.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea5af-206">-NoWinRMEndpoint</span><span class="sxs-lookup"><span data-stu-id="ea5af-206">-NoWinRMEndpoint</span></span>
<span data-ttu-id="ea5af-207">指示此設定不會為虛擬機器新增 WinRM 端點。</span><span class="sxs-lookup"><span data-stu-id="ea5af-207">Indicates that this configuration does not add a WinRM endpoint for the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea5af-208">-Password</span><span class="sxs-lookup"><span data-stu-id="ea5af-208">-Password</span></span>
<span data-ttu-id="ea5af-209">指定管理員帳戶的密碼。</span><span class="sxs-lookup"><span data-stu-id="ea5af-209">Specifies the password of the administrator account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea5af-210">-設定檔</span><span class="sxs-lookup"><span data-stu-id="ea5af-210">-Profile</span></span>
<span data-ttu-id="ea5af-211">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="ea5af-211">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ea5af-212">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="ea5af-212">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea5af-213">-ResetPasswordOnFirstLogon</span><span class="sxs-lookup"><span data-stu-id="ea5af-213">-ResetPasswordOnFirstLogon</span></span>
<span data-ttu-id="ea5af-214">表示虛擬機器要求使用者在第一次登入時變更密碼。</span><span class="sxs-lookup"><span data-stu-id="ea5af-214">Indicates that the virtual machine requires the user to change the password at the first logon.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea5af-215">-SSHKeyPairs</span><span class="sxs-lookup"><span data-stu-id="ea5af-215">-SSHKeyPairs</span></span>
<span data-ttu-id="ea5af-216">指定 SSH 金鑰組。</span><span class="sxs-lookup"><span data-stu-id="ea5af-216">Specifies SSH key pairs.</span></span>

```yaml
Type: SSHKeyPairList
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea5af-217">-SSHPublicKeys</span><span class="sxs-lookup"><span data-stu-id="ea5af-217">-SSHPublicKeys</span></span>
<span data-ttu-id="ea5af-218">指定 SSH 公開金鑰。</span><span class="sxs-lookup"><span data-stu-id="ea5af-218">Specifies SSH public keys.</span></span>

```yaml
Type: SSHPublicKeyList
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea5af-219">-時區</span><span class="sxs-lookup"><span data-stu-id="ea5af-219">-TimeZone</span></span>
<span data-ttu-id="ea5af-220">指定虛擬機器的時區，例如，太平洋標準時間或加拿大中部標準時間。</span><span class="sxs-lookup"><span data-stu-id="ea5af-220">Specifies the time zone for the virtual machine, for example, Pacific Standard Time or Canada Central Standard Time.</span></span>

```yaml
Type: String
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea5af-221">-VM</span><span class="sxs-lookup"><span data-stu-id="ea5af-221">-VM</span></span>
<span data-ttu-id="ea5af-222">指定虛擬電腦物件。</span><span class="sxs-lookup"><span data-stu-id="ea5af-222">Specifies a virtual machine object.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ea5af-223">-Windows</span><span class="sxs-lookup"><span data-stu-id="ea5af-223">-Windows</span></span>
<span data-ttu-id="ea5af-224">指示此設定會建立可執行 Windows 作業系統的獨立虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="ea5af-224">Indicates that this configuration creates a standalone virtual machine that runs the Windows operating system.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea5af-225">-WindowsDomain</span><span class="sxs-lookup"><span data-stu-id="ea5af-225">-WindowsDomain</span></span>
<span data-ttu-id="ea5af-226">指示此設定會建立已加入 Active Directory 網域的 Windows server。</span><span class="sxs-lookup"><span data-stu-id="ea5af-226">Indicates that this configuration creates Windows server that is joined to an Active Directory domain.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea5af-227">-WinRMCertificate</span><span class="sxs-lookup"><span data-stu-id="ea5af-227">-WinRMCertificate</span></span>
<span data-ttu-id="ea5af-228">指定此設定會與 WinRM 端點相關聯的憑證。</span><span class="sxs-lookup"><span data-stu-id="ea5af-228">Specifies a certificate that this configuration associates to a WinRM endpoint.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea5af-229">-X509Certificates</span><span class="sxs-lookup"><span data-stu-id="ea5af-229">-X509Certificates</span></span>
<span data-ttu-id="ea5af-230">指定部署至託管服務的 X509 憑證陣列。</span><span class="sxs-lookup"><span data-stu-id="ea5af-230">Specifies an array of X509 certificates that are deployed to a hosted service.</span></span>

```yaml
Type: X509Certificate2[]
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea5af-231">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea5af-231">CommonParameters</span></span>
<span data-ttu-id="ea5af-232">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ea5af-232">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea5af-233">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ea5af-233">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea5af-234">輸入</span><span class="sxs-lookup"><span data-stu-id="ea5af-234">INPUTS</span></span>

## <span data-ttu-id="ea5af-235">輸出</span><span class="sxs-lookup"><span data-stu-id="ea5af-235">OUTPUTS</span></span>

## <span data-ttu-id="ea5af-236">筆記</span><span class="sxs-lookup"><span data-stu-id="ea5af-236">NOTES</span></span>

## <span data-ttu-id="ea5af-237">相關連結</span><span class="sxs-lookup"><span data-stu-id="ea5af-237">RELATED LINKS</span></span>

[<span data-ttu-id="ea5af-238">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="ea5af-238">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="ea5af-239">新-AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="ea5af-239">New-AzureVMConfig</span></span>](./New-AzureVMConfig.md)


