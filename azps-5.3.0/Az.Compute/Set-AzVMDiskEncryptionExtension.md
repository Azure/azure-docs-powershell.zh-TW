---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6BCB36BC-F5E6-4EDD-983C-8BDE7A9B004D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiskEncryptionExtension.md
ms.openlocfilehash: 1c69d79e148eae92307855ecfe308f5208a2f455
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98449690"
---
# <span data-ttu-id="12da4-101">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="12da4-101">Set-AzVMDiskEncryptionExtension</span></span>

## <span data-ttu-id="12da4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="12da4-102">SYNOPSIS</span></span>
<span data-ttu-id="12da4-103">在 Azure 中的執行 IaaS 虛擬機器上啟用加密。</span><span class="sxs-lookup"><span data-stu-id="12da4-103">Enables encryption on a running IaaS virtual machine in Azure.</span></span>

## <span data-ttu-id="12da4-104">句法</span><span class="sxs-lookup"><span data-stu-id="12da4-104">SYNTAX</span></span>

### <span data-ttu-id="12da4-105">SinglePassParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="12da4-105">SinglePassParameterSet (Default)</span></span>
```
Set-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String>
 [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>]
 [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>] [[-VolumeType] <String>]
 [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>] [[-Passphrase] <String>]
 [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12da4-106">AADClientSecretParameterSet</span><span class="sxs-lookup"><span data-stu-id="12da4-106">AADClientSecretParameterSet</span></span>
```
Set-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientSecret] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12da4-107">AADClientCertParameterSet</span><span class="sxs-lookup"><span data-stu-id="12da4-107">AADClientCertParameterSet</span></span>
```
Set-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientCertThumbprint] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12da4-108">說明</span><span class="sxs-lookup"><span data-stu-id="12da4-108">DESCRIPTION</span></span>
<span data-ttu-id="12da4-109">**AzVMDiskEncryptionExtension** Cmdlet 可在執行中的基礎結構上加密，成為 Azure 中的服務 (IaaS) 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="12da4-109">The **Set-AzVMDiskEncryptionExtension** cmdlet enables encryption on a running infrastructure as a service (IaaS) virtual machine in Azure.</span></span>  <span data-ttu-id="12da4-110">它會在虛擬機器上安裝磁片加密延伸，以啟用加密。</span><span class="sxs-lookup"><span data-stu-id="12da4-110">It enables encryption by installing the disk encryption extension on the virtual machine.</span></span> 

<span data-ttu-id="12da4-111">這個 Cmdlet 需要使用者確認，因為啟用加密的其中一個步驟需要重新開機虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="12da4-111">This cmdlet requires confirmation from the users as one of the steps to enable encryption requires a restart of the virtual machine.</span></span>

<span data-ttu-id="12da4-112">建議您在執行此 Cmdlet 前，先將工作儲存在虛擬機器上。</span><span class="sxs-lookup"><span data-stu-id="12da4-112">It is advised that you save your work on the virtual machine before you run this cmdlet.</span></span>

<span data-ttu-id="12da4-113">Linux：加密 Linux 虛擬電腦時需要 **VolumeType** 參數，且必須設定為 Linux 發佈支援的「Os」、「資料」或「全部」 ) 值 (。</span><span class="sxs-lookup"><span data-stu-id="12da4-113">Linux: The **VolumeType** parameter is required when encrypting Linux virtual machines, and must be set to a value ("Os", "Data", or "All") supported by the Linux distribution.</span></span> 

<span data-ttu-id="12da4-114">Windows：您可以省略 **VolumeType** 參數，在這種情況下，該作業的預設值為 All;如果 Windows 虛擬機器的 VolumeType 參數存在，則必須將它設為 All 或 OS。</span><span class="sxs-lookup"><span data-stu-id="12da4-114">Windows: The **VolumeType** parameter may be omitted, in which case the operation defaults to All; if the VolumeType parameter is present for a Windows virtual machine, it must be set to either All or OS.</span></span>

## <span data-ttu-id="12da4-115">示例</span><span class="sxs-lookup"><span data-stu-id="12da4-115">EXAMPLES</span></span>

### <span data-ttu-id="12da4-116">範例1：啟用加密</span><span class="sxs-lookup"><span data-stu-id="12da4-116">Example 1: Enable encryption</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$VolumeType = "All"
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -VolumeType $VolumeType
```

<span data-ttu-id="12da4-117">這個範例會在 VM 上啟用加密，而不指定廣告認證。</span><span class="sxs-lookup"><span data-stu-id="12da4-117">This example enables encryption on a VM without specifying AD credentials.</span></span>

### <span data-ttu-id="12da4-118">範例2：使用流水線輸入啟用加密</span><span class="sxs-lookup"><span data-stu-id="12da4-118">Example 2: Enable encryption with pipelined input</span></span>
```
$params = New-Object PSObject -Property @{
    ResourceGroupName = "[resource-group-name]"
    VMName = "[vm-name]"
    DiskEncryptionKeyVaultId = "/subscriptions/[subscription-id-guid]/resourceGroups/[resource-group-name]/providers/Microsoft.KeyVault/vaults/[keyvault-name]"
    DiskEncryptionKeyVaultUrl = "https://[keyvault-name].vault.azure.net"
    KeyEncryptionKeyVaultId = "/subscriptions/[subscription-id-guid]/resourceGroups/[resource-group-name]/providers/Microsoft.KeyVault/vaults/[keyvault-name]"
    KeyEncryptionKeyUrl = "https://[keyvault-name].vault.azure.net/keys/[kekname]/[kek-unique-id]"
    VolumeType = "All"
}

$params | Set-AzVmDiskEncryptionExtension
```

<span data-ttu-id="12da4-119">這個範例會使用流水線輸入傳送參數，以在 VM 上啟用加密，而不需指定廣告認證。</span><span class="sxs-lookup"><span data-stu-id="12da4-119">This example sends parameters using pipelined input to enable encryption on a VM, without specifying AD credentials.</span></span>

### <span data-ttu-id="12da4-120">範例3：使用 Azure AD 用戶端識別碼和用戶端密碼啟用加密</span><span class="sxs-lookup"><span data-stu-id="12da4-120">Example 3: Enable encryption using Azure AD Client ID and Client Secret</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
$AADClientID = "<clientID of your Azure AD app>"
$AADClientSecret = "<clientSecret of your Azure AD app>"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$VolumeType = "All"
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientSecret $AADClientSecret -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -VolumeType $VolumeType
```

<span data-ttu-id="12da4-121">這個範例使用 Azure AD 用戶端識別碼和用戶端密碼在 VM 上啟用加密。</span><span class="sxs-lookup"><span data-stu-id="12da4-121">This example uses Azure AD client ID and client secret to enable encryption on a VM.</span></span>

### <span data-ttu-id="12da4-122">範例4：使用 Azure AD 用戶端識別碼和用戶端認證指紋啟用加密</span><span class="sxs-lookup"><span data-stu-id="12da4-122">Example 4: Enable encryption using Azure AD client ID and client certification thumbprint</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
#The KeyVault must have enabledForDiskEncryption property set on it
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$VolumeType = "All"

# create Azure AD application and associate the certificate
$CertPath = "C:\certificates\examplecert.pfx"
$CertPassword = "Password"
$Cert = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2($CertPath, $CertPassword)
$CertValue = [System.Convert]::ToBase64String($cert.GetRawCertData())
$AzureAdApplication = New-AzADApplication -DisplayName "<Your Application Display Name>" -HomePage "<https://YourApplicationHomePage>" -IdentifierUris "<https://YouApplicationUri>" -CertValue $CertValue 
$ServicePrincipal = New-AzADServicePrincipal -ApplicationId $AzureAdApplication.ApplicationId

$AADClientID = $AzureAdApplication.ApplicationId
$aadClientCertThumbprint= $cert.Thumbprint

#Upload pfx to KeyVault 
$KeyVaultSecretName = "MyAADCert"
$FileContentBytes = get-content $CertPath -Encoding Byte
$FileContentEncoded = [System.Convert]::ToBase64String($fileContentBytes)
$JSONObject = @"
    { 
        "data" : "$filecontentencoded", 
        "dataType" : "pfx", 
        "password" : "$CertPassword" 
    } 
"@
$JSONObjectBytes = [System.Text.Encoding]::UTF8.GetBytes($jsonObject)
$JSONEncoded = [System.Convert]::ToBase64String($jsonObjectBytes)

$Secret = ConvertTo-SecureString -String $JSONEncoded -AsPlainText -Force
Set-AzKeyVaultSecret -VaultName $VaultName -Name $KeyVaultSecretName -SecretValue $Secret
Set-AzKeyVaultAccessPolicy -VaultName $VaultName -ResourceGroupName $RGName -EnabledForDeployment

#deploy cert to VM
$CertUrl = (Get-AzKeyVaultSecret -VaultName $VaultName -Name $KeyVaultSecretName).Id
$SourceVaultId = (Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName).ResourceId
$VM = Get-AzVM -ResourceGroupName $RGName -Name $VMName 
$VM = Add-AzVMSecret -VM $VM -SourceVaultId $SourceVaultId -CertificateStore "My" -CertificateUrl $CertUrl
Update-AzVM -VM $VM -ResourceGroupName $RGName 

#Enable encryption on the virtual machine using Azure AD client ID and client cert thumbprint
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientCertThumbprint $AADClientCertThumbprint -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -VolumeType $VolumeType
```

<span data-ttu-id="12da4-123">這個範例使用 Azure AD 用戶端識別碼和用戶端認證指紋在 VM 上啟用加密。</span><span class="sxs-lookup"><span data-stu-id="12da4-123">This example uses Azure AD client ID and client certification thumbprints to enable encryption on a VM.</span></span>

### <span data-ttu-id="12da4-124">範例5：使用金鑰加密金鑰啟用使用 Azure AD 用戶端識別碼、用戶端密碼及自動換行磁片加密金鑰的加密功能</span><span class="sxs-lookup"><span data-stu-id="12da4-124">Example 5: Enable encryption using Azure AD client ID, client secret, and wrap disk encryption key by using key encryption key</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"

$AADClientID = "<clientID of your Azure AD app>"
$AADClientSecret = "<clientSecret of your Azure AD app>"

$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$VolumeType = "All"

$KEKName = "MyKeyEncryptionKey"
$KEK = Add-AzKeyVaultKey -VaultName $VaultName -Name $KEKName -Destination "Software"
$KeyEncryptionKeyUrl = $KEK.Key.kid

Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientSecret $AADClientSecret -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl -KeyEncryptionKeyVaultId $KeyVaultResourceId -VolumeType $VolumeType
```

<span data-ttu-id="12da4-125">這個範例使用 Azure AD 用戶端識別碼和用戶端密碼在 VM 上啟用加密，並使用金鑰加密金鑰來包裝磁片加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="12da4-125">This example uses Azure AD client ID and client secret to enable encryption on a VM, and wraps the disk encryption key using a key encryption key.</span></span>

### <span data-ttu-id="12da4-126">範例6：使用 Azure AD 用戶端識別碼、用戶端憑證指紋，以及使用金鑰加密金鑰來包裝磁片 encryption.encryptionkey 來啟用加密</span><span class="sxs-lookup"><span data-stu-id="12da4-126">Example 6: Enable encryption using Azure AD client ID, client cert thumbprint, and wrap disk encryptionkey by using key encryption key</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
#The KeyVault must have enabledForDiskEncryption property set on it
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$KEKName = "MyKeyEncryptionKey"
$KEK = Add-AzKeyVaultKey -VaultName $VaultName -Name $KEKName -Destination "Software"
$KeyEncryptionKeyUrl = $KEK.Key.kid
$VolumeType = "All"

# create Azure AD application and associate the certificate
$CertPath = "C:\certificates\examplecert.pfx"
$CertPassword = "Password"
$Cert = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2($CertPath, $CertPassword)
$CertValue = [System.Convert]::ToBase64String($cert.GetRawCertData())
$AzureAdApplication = New-AzADApplication -DisplayName "<Your Application Display Name>" -HomePage "<https://YourApplicationHomePage>" -IdentifierUris "<https://YouApplicationUri>" -CertValue $CertValue
$ServicePrincipal = New-AzADServicePrincipal -ApplicationId $AzureAdApplication.ApplicationId

$AADClientID = $AzureAdApplication.ApplicationId
$AADClientCertThumbprint= $Cert.Thumbprint

#Upload pfx to KeyVault 
$KeyVaultSecretName = "MyAADCert"
$FileContentBytes = get-content $CertPath -Encoding Byte
$FileContentEncoded = [System.Convert]::ToBase64String($FileContentBytes)
$JSONObject = @"
    { 
        "data" : "$filecontentencoded", 
        "dataType" : "pfx", 
        "password" : "$CertPassword" 
    } 
"@
$JSONObjectBytes = [System.Text.Encoding]::UTF8.GetBytes($JSONObject)
$JsonEncoded = [System.Convert]::ToBase64String($JSONObjectBytes)
$Secret = ConvertTo-SecureString -String $JSONEncoded -AsPlainText -Force
Set-AzKeyVaultSecret -VaultName $VaultName-Name $KeyVaultSecretName -SecretValue $Secret
Set-AzKeyVaultAccessPolicy -VaultName $VaultName -ResourceGroupName $RGName -EnabledForDeployment

#deploy cert to VM
$CertUrl = (Get-AzKeyVaultSecret -VaultName $VaultName -Name $KeyVaultSecretName).Id
$SourceVaultId = (Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName).ResourceId
$VM = Get-AzVM -ResourceGroupName $RGName -Name $VMName 
$VM = Add-AzVMSecret -VM $VM -SourceVaultId $SourceVaultId -CertificateStore "My" -CertificateUrl $CertUrl 
Update-AzVM -VM $VM -ResourceGroupName $RGName 

#Enable encryption on the virtual machine using Azure AD client ID and client cert thumbprint
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGname -VMName $VMName -AadClientID $AADClientID -AadClientCertThumbprint $AADClientCertThumbprint -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl -KeyEncryptionKeyVaultId $KeyVaultResourceId -VolumeType $VolumeType
```

<span data-ttu-id="12da4-127">這個範例使用 Azure AD 用戶端識別碼和用戶端憑證指紋在 VM 上啟用加密，並使用金鑰加密金鑰來包裝磁片加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="12da4-127">This example uses Azure AD client ID and client cert thumbprint to enable encryption on a VM, and wraps the disk encryption key using a key encryption key.</span></span>

## <span data-ttu-id="12da4-128">參數</span><span class="sxs-lookup"><span data-stu-id="12da4-128">PARAMETERS</span></span>

### <span data-ttu-id="12da4-129">-AadClientCertThumbprint</span><span class="sxs-lookup"><span data-stu-id="12da4-129">-AadClientCertThumbprint</span></span>
<span data-ttu-id="12da4-130">指定 AzureActive 目錄的指紋， (的 Azure AD) 應用程式用戶端憑證，且具有將機密寫入 **KeyVault** 的許可權。</span><span class="sxs-lookup"><span data-stu-id="12da4-130">Specifies the thumbprint of the AzureActive Directory (Azure AD) application client certificate that has permissions to write secrets to **KeyVault**.</span></span>
<span data-ttu-id="12da4-131">就必要而言，Azure AD 用戶端憑證必須先部署到虛擬機器的 [本機電腦] `my` 憑證存放區。</span><span class="sxs-lookup"><span data-stu-id="12da4-131">As a prerequisite, the Azure AD client certificate must be previously deployed to the virtual machine's local computer `my` certificate store.</span></span>
<span data-ttu-id="12da4-132">Add-AzVMSecret Cmdlet 可以用來將憑證部署到 Azure 中的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="12da4-132">The Add-AzVMSecret cmdlet can be used to deploy a certificate to a virtual machine in Azure.</span></span>
<span data-ttu-id="12da4-133">如需詳細資訊，請參閱 **Add AzVMSecret** Cmdlet 說明。</span><span class="sxs-lookup"><span data-stu-id="12da4-133">For more details, see the **Add-AzVMSecret** cmdlet help.</span></span>
<span data-ttu-id="12da4-134">證書必須先部署到 [虛擬機器本機電腦] 的 [我的證書] 存放區。</span><span class="sxs-lookup"><span data-stu-id="12da4-134">The certificate must be previously deployed to the virtual machine local computer my certificate store.</span></span>

```yaml
Type: System.String
Parameter Sets: AADClientCertParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12da4-135">-AadClientID</span><span class="sxs-lookup"><span data-stu-id="12da4-135">-AadClientID</span></span>
<span data-ttu-id="12da4-136">指定擁有將機密寫入 **KeyVault** 之許可權的 Azure AD 應用程式的用戶端識別碼。</span><span class="sxs-lookup"><span data-stu-id="12da4-136">Specifies the client ID of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

```yaml
Type: System.String
Parameter Sets: AADClientSecretParameterSet, AADClientCertParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12da4-137">-AadClientSecret</span><span class="sxs-lookup"><span data-stu-id="12da4-137">-AadClientSecret</span></span>
<span data-ttu-id="12da4-138">指定擁有將機密寫入 **KeyVault** 之許可權的 Azure AD 應用程式的用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="12da4-138">Specifies the client secret of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

```yaml
Type: System.String
Parameter Sets: AADClientSecretParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12da4-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12da4-139">-DefaultProfile</span></span>
<span data-ttu-id="12da4-140">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="12da4-140">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12da4-141">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="12da4-141">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="12da4-142">表示此 Cmdlet 會停用延伸次要版本的自動升級。</span><span class="sxs-lookup"><span data-stu-id="12da4-142">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 14
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12da4-143">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="12da4-143">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="12da4-144">指定要上傳虛擬機器加密金鑰之 **KeyVault** 的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="12da4-144">Specifies the resource ID of the **KeyVault** to which the virtual machine encryption keys should be uploaded.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12da4-145">-DiskEncryptionKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="12da4-145">-DiskEncryptionKeyVaultUrl</span></span>
<span data-ttu-id="12da4-146">指定要將虛擬機器加密金鑰上傳到哪個 **KeyVault** URL。</span><span class="sxs-lookup"><span data-stu-id="12da4-146">Specifies the **KeyVault** URL to which the virtual machine encryption keys should be uploaded.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12da4-147">-EncryptFormatAll</span><span class="sxs-lookup"><span data-stu-id="12da4-147">-EncryptFormatAll</span></span>
<span data-ttu-id="12da4-148">Encrypt-Format 尚未加密的所有資料磁片磁碟機</span><span class="sxs-lookup"><span data-stu-id="12da4-148">Encrypt-Format all data drives that are not already encrypted</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12da4-149">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="12da4-149">-ExtensionPublisherName</span></span>
<span data-ttu-id="12da4-150">延伸發行者名稱。</span><span class="sxs-lookup"><span data-stu-id="12da4-150">The extension publisher name.</span></span> <span data-ttu-id="12da4-151">指定此參數，只會覆寫「Microsoft Azure. Security」的預設值。</span><span class="sxs-lookup"><span data-stu-id="12da4-151">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12da4-152">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="12da4-152">-ExtensionType</span></span>
<span data-ttu-id="12da4-153">延伸類型。</span><span class="sxs-lookup"><span data-stu-id="12da4-153">The extension type.</span></span> <span data-ttu-id="12da4-154">指定此參數可覆寫 Windows Vm 的 "AzureDiskEncryption" 的預設值，以及 Linux Vm 的 "AzureDiskEncryptionForLinux"。</span><span class="sxs-lookup"><span data-stu-id="12da4-154">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12da4-155">-Force</span><span class="sxs-lookup"><span data-stu-id="12da4-155">-Force</span></span>
<span data-ttu-id="12da4-156">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="12da4-156">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12da4-157">-KeyEncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="12da4-157">-KeyEncryptionAlgorithm</span></span>
<span data-ttu-id="12da4-158">指定用來包裝及解出虛擬機器金鑰加密金鑰的演算法。</span><span class="sxs-lookup"><span data-stu-id="12da4-158">Specifies the algorithm that is used to wrap and unwrap the key encryption key of the virtual machine.</span></span>
<span data-ttu-id="12da4-159">預設值為 RSA-OAEP。</span><span class="sxs-lookup"><span data-stu-id="12da4-159">The default value is RSA-OAEP.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA-OAEP, RSA1_5

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12da4-160">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="12da4-160">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="12da4-161">指定金鑰加密金鑰的 URL，該金鑰是用來包裝及解包虛擬機器加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="12da4-161">Specifies the URL of the key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="12da4-162">這必須是完整的版本控制 URL。</span><span class="sxs-lookup"><span data-stu-id="12da4-162">This must be the full versioned URL.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12da4-163">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="12da4-163">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="12da4-164">指定包含金鑰加密金鑰的 **KeyVault** 的資源識別碼，該金鑰是用來包裝及解包虛擬機器加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="12da4-164">Specifies the resource ID of the **KeyVault** that contains key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="12da4-165">這必須是完整版本的 URL。</span><span class="sxs-lookup"><span data-stu-id="12da4-165">This must be a full versioned URL.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12da4-166">-名稱</span><span class="sxs-lookup"><span data-stu-id="12da4-166">-Name</span></span>
<span data-ttu-id="12da4-167">指定代表延伸的 Azure 資源管理員資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="12da4-167">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span> <span data-ttu-id="12da4-168">如果省略 *Name* 參數，則在 Windows 虛擬機器上，系統會將已安裝的擴充功能命名為 AzureDiskEncryption，並在 Linux 虛擬機器上 AzureDiskEncryptionForLinux。</span><span class="sxs-lookup"><span data-stu-id="12da4-168">If the *Name* parameter is omitted, the installed extension will be named AzureDiskEncryption on Windows virtual machines and AzureDiskEncryptionForLinux on Linux virtual machines.</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12da4-169">-密碼</span><span class="sxs-lookup"><span data-stu-id="12da4-169">-Passphrase</span></span>
<span data-ttu-id="12da4-170">指定僅用於加密 Linux 虛擬機器的密碼。</span><span class="sxs-lookup"><span data-stu-id="12da4-170">Specifies the passphrase used for encrypting Linux virtual machines only.</span></span>
<span data-ttu-id="12da4-171">此參數不適用於執行 Windows 作業系統的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="12da4-171">This parameter is not used for virtual machines that run the Windows operating system.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 13
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12da4-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12da4-172">-ResourceGroupName</span></span>
<span data-ttu-id="12da4-173">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="12da4-173">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12da4-174">-SequenceVersion</span><span class="sxs-lookup"><span data-stu-id="12da4-174">-SequenceVersion</span></span>
<span data-ttu-id="12da4-175">指定虛擬機器加密作業的序列值。</span><span class="sxs-lookup"><span data-stu-id="12da4-175">Specifies the sequence number of the encryption operations for a virtual machine.</span></span>
<span data-ttu-id="12da4-176">每個在同一個虛擬機器上執行的加密作業都是唯一的。</span><span class="sxs-lookup"><span data-stu-id="12da4-176">This is unique per each encryption operation performed on the same virtual machine.</span></span>
<span data-ttu-id="12da4-177">Get-AzVMExtension Cmdlet 可用來檢索以前使用的序列值。</span><span class="sxs-lookup"><span data-stu-id="12da4-177">The Get-AzVMExtension cmdlet can be used to retrieve the previous sequence number that was used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12da4-178">-SkipVmBackup</span><span class="sxs-lookup"><span data-stu-id="12da4-178">-SkipVmBackup</span></span>
<span data-ttu-id="12da4-179">略過 Linux Vm 的備份建立</span><span class="sxs-lookup"><span data-stu-id="12da4-179">Skip backup creation for Linux VMs</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 15
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12da4-180">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="12da4-180">-TypeHandlerVersion</span></span>
<span data-ttu-id="12da4-181">指定加密延伸的版本。</span><span class="sxs-lookup"><span data-stu-id="12da4-181">Specifies the version of the encryption extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12da4-182">-VMName</span><span class="sxs-lookup"><span data-stu-id="12da4-182">-VMName</span></span>
<span data-ttu-id="12da4-183">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="12da4-183">Specifies the name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12da4-184">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="12da4-184">-VolumeType</span></span>
<span data-ttu-id="12da4-185">指定要執行加密作業的虛擬機器體積類型：作業系統、資料或全部。</span><span class="sxs-lookup"><span data-stu-id="12da4-185">Specifies the type of virtual machine volumes on which to perform encryption operation: OS, Data, or All.</span></span> 

<span data-ttu-id="12da4-186">Linux：加密 Linux 虛擬電腦時需要 **VolumeType** 參數，且必須設定為 Linux 發佈支援的「Os」、「資料」或「全部」 ) 值 (。</span><span class="sxs-lookup"><span data-stu-id="12da4-186">Linux: The **VolumeType** parameter is required when encrypting Linux virtual machines, and must be set to a value ("Os", "Data", or "All") supported by the Linux distribution.</span></span> 

<span data-ttu-id="12da4-187">Windows：您可以省略 **VolumeType** 參數，在這種情況下，該作業的預設值為 All;如果 Windows 虛擬機器的 VolumeType 參數存在，則必須將它設為 All 或 OS。</span><span class="sxs-lookup"><span data-stu-id="12da4-187">Windows: The **VolumeType** parameter may be omitted, in which case the operation defaults to All; if the VolumeType parameter is present for a Windows virtual machine, it must be set to either All or OS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: OS, Data, All

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12da4-188">-確認</span><span class="sxs-lookup"><span data-stu-id="12da4-188">-Confirm</span></span>
<span data-ttu-id="12da4-189">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="12da4-189">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12da4-190">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12da4-190">-WhatIf</span></span>
<span data-ttu-id="12da4-191">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="12da4-191">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12da4-192">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="12da4-192">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12da4-193">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12da4-193">CommonParameters</span></span>
<span data-ttu-id="12da4-194">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="12da4-194">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12da4-195">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="12da4-195">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12da4-196">輸入</span><span class="sxs-lookup"><span data-stu-id="12da4-196">INPUTS</span></span>

### <span data-ttu-id="12da4-197">System.object</span><span class="sxs-lookup"><span data-stu-id="12da4-197">System.String</span></span>

### <span data-ttu-id="12da4-198">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="12da4-198">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="12da4-199">輸出</span><span class="sxs-lookup"><span data-stu-id="12da4-199">OUTPUTS</span></span>

### <span data-ttu-id="12da4-200">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="12da4-200">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="12da4-201">筆記</span><span class="sxs-lookup"><span data-stu-id="12da4-201">NOTES</span></span>

## <span data-ttu-id="12da4-202">相關連結</span><span class="sxs-lookup"><span data-stu-id="12da4-202">RELATED LINKS</span></span>

[<span data-ttu-id="12da4-203">附加 AzVMSecret</span><span class="sxs-lookup"><span data-stu-id="12da4-203">Add-AzVMSecret</span></span>](./Add-AzVMSecret.md)

[<span data-ttu-id="12da4-204">AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="12da4-204">Get-AzVMDiskEncryptionStatus</span></span>](./Get-AzVMDiskEncryptionStatus.md)

[<span data-ttu-id="12da4-205">移除-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="12da4-205">Remove-AzVMDiskEncryptionExtension</span></span>](./Remove-AzVMDiskEncryptionExtension.md)


