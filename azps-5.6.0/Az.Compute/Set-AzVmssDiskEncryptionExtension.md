---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmssdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssDiskEncryptionExtension.md
ms.openlocfilehash: 7f163a80efe4e10f0107298351c59a72bfaaceb0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914874"
---
# <span data-ttu-id="c3ecb-101">Set-AzVmssDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="c3ecb-101">Set-AzVmssDiskEncryptionExtension</span></span>

## <span data-ttu-id="c3ecb-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c3ecb-102">SYNOPSIS</span></span>
<span data-ttu-id="c3ecb-103">啟用 VM 縮放集的磁片加密。</span><span class="sxs-lookup"><span data-stu-id="c3ecb-103">Enables disk encryption on a VM scale set.</span></span>

## <span data-ttu-id="c3ecb-104">語法</span><span class="sxs-lookup"><span data-stu-id="c3ecb-104">SYNTAX</span></span>

```
Set-AzVmssDiskEncryptionExtension [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String> [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionKeyVaultId <String>] [-KeyEncryptionAlgorithm <String>] [-VolumeType <String>] [-ForceUpdate]
 [-TypeHandlerVersion <String>] [-ExtensionName <String>] [-Passphrase <String>] [-Force]
 [-DisableAutoUpgradeMinorVersion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c3ecb-105">描述</span><span class="sxs-lookup"><span data-stu-id="c3ecb-105">DESCRIPTION</span></span>
<span data-ttu-id="c3ecb-106">**Set-Az VmsCryptencryptionExtension** Cmdlet 可在 VM 縮放集上啟用加密。</span><span class="sxs-lookup"><span data-stu-id="c3ecb-106">The **Set-AzVmssDiskEncryptionExtension** cmdlet enables encryption on a VM scale set.</span></span> <span data-ttu-id="c3ecb-107">此 Cmdlet 可在 VM 縮放集上安裝磁片加密擴充功能，以啟用加密。</span><span class="sxs-lookup"><span data-stu-id="c3ecb-107">This cmdlet enables encryption by installing the disk encryption extension on the VM scale set.</span></span>

<span data-ttu-id="c3ecb-108">對於 Linux 虛擬機器 *，VolumeType* 參數必須存在，而且必須設定為「資料」</span><span class="sxs-lookup"><span data-stu-id="c3ecb-108">For Linux virtual machines, the *VolumeType* parameter must be present and must be set to "Data"</span></span>

## <span data-ttu-id="c3ecb-109">例子</span><span class="sxs-lookup"><span data-stu-id="c3ecb-109">EXAMPLES</span></span>

### <span data-ttu-id="c3ecb-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="c3ecb-110">Example 1</span></span>
```
$RGName = "MyResourceGroup"
$VmssName = "MyTestVmss"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId

PS C:\> Set-AzVmssDiskEncryptionExtension -ResourceGroupName $RGName -VMScaleSetName $VmssName -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="c3ecb-111">此命令可在 VM 縮放集內所有 Windows 虛擬機器的所有磁片上啟用加密。</span><span class="sxs-lookup"><span data-stu-id="c3ecb-111">This command enables encryption on all disks of all Windows VMs in a VM scale set.</span></span>

### <span data-ttu-id="c3ecb-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="c3ecb-112">Example 2</span></span>
```
$RGName = "MyResourceGroup"
$VmssName = "MyTestVmss"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$VolumeType = "Data"

PS C:\> Set-AzVmssDiskEncryptionExtension -ResourceGroupName $RGName -VMScaleSetName $VmssName -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
 -VolumeType $volumeType
```

<span data-ttu-id="c3ecb-113">此命令可在 VM 縮放集內所有 Linux 虛擬機器的資料磁片上啟用加密。</span><span class="sxs-lookup"><span data-stu-id="c3ecb-113">This command enables encryption on the data disks of all Linux VMs in a VM scale set.</span></span>

## <span data-ttu-id="c3ecb-114">參數</span><span class="sxs-lookup"><span data-stu-id="c3ecb-114">PARAMETERS</span></span>

### <span data-ttu-id="c3ecb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3ecb-115">-DefaultProfile</span></span>
<span data-ttu-id="c3ecb-116">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c3ecb-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3ecb-117">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="c3ecb-117">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="c3ecb-118">停用次要版本的自動升級</span><span class="sxs-lookup"><span data-stu-id="c3ecb-118">Disable auto-upgrade of minor version</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3ecb-119">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="c3ecb-119">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="c3ecb-120">KeyVault 的 ResourceID，其中會放置產生加密金鑰的位置</span><span class="sxs-lookup"><span data-stu-id="c3ecb-120">ResourceID of the KeyVault where generated encryption key will be placed to</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3ecb-121">-DiskEncryptionKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="c3ecb-121">-DiskEncryptionKeyVaultUrl</span></span>
<span data-ttu-id="c3ecb-122">將放置產生加密金鑰的 KeyVault URL</span><span class="sxs-lookup"><span data-stu-id="c3ecb-122">URL of the KeyVault where generated encryption key will be placed to</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3ecb-123">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="c3ecb-123">-ExtensionName</span></span>
<span data-ttu-id="c3ecb-124">副檔名。</span><span class="sxs-lookup"><span data-stu-id="c3ecb-124">The extension name.</span></span>
<span data-ttu-id="c3ecb-125">如果未指定此參數，則使用的預設值為適用于 Windows 虛擬機器的 AzureCryptEncryption 和適用于 Linux VMs 的 AzureCryptEncryptionForWindows</span><span class="sxs-lookup"><span data-stu-id="c3ecb-125">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs</span></span>

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

### <span data-ttu-id="c3ecb-126">-強制</span><span class="sxs-lookup"><span data-stu-id="c3ecb-126">-Force</span></span>
<span data-ttu-id="c3ecb-127">在虛擬機器縮放比例集上強制啟用加密。</span><span class="sxs-lookup"><span data-stu-id="c3ecb-127">To force enabling encryption on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="c3ecb-128">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="c3ecb-128">-ForceUpdate</span></span>
<span data-ttu-id="c3ecb-129">產生強制更新的標記。</span><span class="sxs-lookup"><span data-stu-id="c3ecb-129">Generate a tag for force update.</span></span>  <span data-ttu-id="c3ecb-130">您應該提供這個選項，以在同一個 VM 上重複執行加密作業。</span><span class="sxs-lookup"><span data-stu-id="c3ecb-130">This should be given to perform repeated encryption operations on the same VM.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3ecb-131">-KeyEncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="c3ecb-131">-KeyEncryptionAlgorithm</span></span>
<span data-ttu-id="c3ecb-132">用來加密大量加密金鑰的 KeyEncryption 演算法</span><span class="sxs-lookup"><span data-stu-id="c3ecb-132">KeyEncryption Algorithm used to encrypt the volume encryption key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA-OAEP, RSA1_5

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3ecb-133">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="c3ecb-133">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="c3ecb-134">用來加密磁片加密金鑰的 KeyEncryptionKey 版本化 KeyVault URL</span><span class="sxs-lookup"><span data-stu-id="c3ecb-134">Versioned KeyVault URL of the KeyEncryptionKey used to encrypt the disk encryption key</span></span>

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

### <span data-ttu-id="c3ecb-135">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="c3ecb-135">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="c3ecb-136">KeyVault 的 ResourceID，其中包含用來加密磁片加密金鑰的 KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="c3ecb-136">ResourceID of the KeyVault containing the KeyEncryptionKey used to encrypt the disk encryption key</span></span>

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

### <span data-ttu-id="c3ecb-137">-Passphrase</span><span class="sxs-lookup"><span data-stu-id="c3ecb-137">-Passphrase</span></span>
<span data-ttu-id="c3ecb-138">參數中指定的密碼。</span><span class="sxs-lookup"><span data-stu-id="c3ecb-138">The passphrase specified in parameters.</span></span>
<span data-ttu-id="c3ecb-139">此參數僅適用于 Linux VM。</span><span class="sxs-lookup"><span data-stu-id="c3ecb-139">This parameter only works for Linux VM.</span></span>

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

### <span data-ttu-id="c3ecb-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3ecb-140">-ResourceGroupName</span></span>
<span data-ttu-id="c3ecb-141">VM 縮放集所屬的資源組名</span><span class="sxs-lookup"><span data-stu-id="c3ecb-141">The resource group name to which the VM Scale Set belongs to</span></span>

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

### <span data-ttu-id="c3ecb-142">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="c3ecb-142">-TypeHandlerVersion</span></span>
<span data-ttu-id="c3ecb-143">類型處理常式版本。</span><span class="sxs-lookup"><span data-stu-id="c3ecb-143">The type handler version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3ecb-144">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="c3ecb-144">-VMScaleSetName</span></span>
<span data-ttu-id="c3ecb-145">虛擬機器縮放集的名稱</span><span class="sxs-lookup"><span data-stu-id="c3ecb-145">Name of the virtual machine scale set</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3ecb-146">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="c3ecb-146">-VolumeType</span></span>
<span data-ttu-id="c3ecb-147">指定要執行加密作業的虛擬機器卷積類型：作業系統、資料或全部。</span><span class="sxs-lookup"><span data-stu-id="c3ecb-147">Specifies the type of virtual machine volumes on which to perform encryption operation: OS, Data, or All.</span></span> 

<span data-ttu-id="c3ecb-148">**Linux：VolumeType** 參數必須存在，而且必須設定為數據。</span><span class="sxs-lookup"><span data-stu-id="c3ecb-148">Linux: The **VolumeType** parameter must be present and must be set to Data.</span></span> 

<span data-ttu-id="c3ecb-149">Windows： **如果 VolumeType** 參數存在，則必須設定為 All 或 OS。</span><span class="sxs-lookup"><span data-stu-id="c3ecb-149">Windows: The **VolumeType** parameter, if present, must be set to either All or OS.</span></span> <span data-ttu-id="c3ecb-150">如果 **省略 VolumeType** 參數，預設值為 "All"。</span><span class="sxs-lookup"><span data-stu-id="c3ecb-150">If the **VolumeType** parameter is omitted it defaults to "All".</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: OS, Data, All

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3ecb-151">-確認</span><span class="sxs-lookup"><span data-stu-id="c3ecb-151">-Confirm</span></span>
<span data-ttu-id="c3ecb-152">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c3ecb-152">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3ecb-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3ecb-153">-WhatIf</span></span>
<span data-ttu-id="c3ecb-154">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c3ecb-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3ecb-155">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c3ecb-155">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3ecb-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3ecb-156">CommonParameters</span></span>
<span data-ttu-id="c3ecb-157">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c3ecb-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3ecb-158">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c3ecb-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3ecb-159">輸入</span><span class="sxs-lookup"><span data-stu-id="c3ecb-159">INPUTS</span></span>

### <span data-ttu-id="c3ecb-160">System.String</span><span class="sxs-lookup"><span data-stu-id="c3ecb-160">System.String</span></span>

### <span data-ttu-id="c3ecb-161">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c3ecb-161">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c3ecb-162">輸出</span><span class="sxs-lookup"><span data-stu-id="c3ecb-162">OUTPUTS</span></span>

### <span data-ttu-id="c3ecb-163">Microsoft.Azure.Commands.Compute.models.PSVirtualMachineScaleSetExtension</span><span class="sxs-lookup"><span data-stu-id="c3ecb-163">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineScaleSetExtension</span></span>

## <span data-ttu-id="c3ecb-164">筆記</span><span class="sxs-lookup"><span data-stu-id="c3ecb-164">NOTES</span></span>

## <span data-ttu-id="c3ecb-165">相關連結</span><span class="sxs-lookup"><span data-stu-id="c3ecb-165">RELATED LINKS</span></span>
