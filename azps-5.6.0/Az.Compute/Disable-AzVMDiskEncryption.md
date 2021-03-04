---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 979E956B-4C74-426E-A617-E50C4EBC8A20
online version: https://docs.microsoft.com/powershell/module/az.compute/disable-azvmdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Disable-AzVMDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Disable-AzVMDiskEncryption.md
ms.openlocfilehash: bd96a26eda14770dcc7a5592e12e64e15eac02f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906281"
---
# <span data-ttu-id="c7942-101">Disable-AzVMDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="c7942-101">Disable-AzVMDiskEncryption</span></span>

## <span data-ttu-id="c7942-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c7942-102">SYNOPSIS</span></span>
<span data-ttu-id="c7942-103">停用在IaaS 虛擬機器上的加密。</span><span class="sxs-lookup"><span data-stu-id="c7942-103">Disables encryption on an IaaS virtual machine.</span></span>

## <span data-ttu-id="c7942-104">語法</span><span class="sxs-lookup"><span data-stu-id="c7942-104">SYNTAX</span></span>

```
Disable-AzVMDiskEncryption [-ResourceGroupName] <String> [-VMName] <String> [[-VolumeType] <String>]
 [[-Name] <String>] [[-TypeHandlerVersion] <String>] [-Force] [-DisableAutoUpgradeMinorVersion]
 [-ExtensionType <String>] [-ExtensionPublisherName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7942-105">描述</span><span class="sxs-lookup"><span data-stu-id="c7942-105">DESCRIPTION</span></span>
<span data-ttu-id="c7942-106">**Disable-AzCRYPTCryptEncryption** Cmdlet 會停用基礎結構上的加密為 (IaaS) 虛擬機器的服務。</span><span class="sxs-lookup"><span data-stu-id="c7942-106">The **Disable-AzVMDiskEncryption** cmdlet disables encryption on an infrastructure as a service (IaaS) virtual machine.</span></span>
<span data-ttu-id="c7942-107">此 Cmdlet 僅支援 Windows 虛擬機器，不支援 Linux 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="c7942-107">This cmdlet is only supported on Windows virtual machines and not Linux virtual machines.</span></span>
<span data-ttu-id="c7942-108">此 Cmdlet 在虛擬機器上安裝擴充功能以停用加密。</span><span class="sxs-lookup"><span data-stu-id="c7942-108">This cmdlet installs an extension on the virtual machine to disable encryption.</span></span>
<span data-ttu-id="c7942-109">如果 *未指定 Name* 參數，會建立一個副檔名，其預設名稱為「Windows VMs 的 AzureAzAzEncryption」。</span><span class="sxs-lookup"><span data-stu-id="c7942-109">If the *Name* parameter is not specified, an extension with the default name "AzureDiskEncryption for Windows VMs" is created.</span></span>
<span data-ttu-id="c7942-110">注意：此 Cmdlet 會重新開機虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="c7942-110">Caution: This cmdlet reboots the virtual machine.</span></span>

## <span data-ttu-id="c7942-111">例子</span><span class="sxs-lookup"><span data-stu-id="c7942-111">EXAMPLES</span></span>

### <span data-ttu-id="c7942-112">範例 1：停用 Windows 虛擬機器上所有卷的加密</span><span class="sxs-lookup"><span data-stu-id="c7942-112">Example 1: Disable encryption for all volumes on a Windows virtual machine</span></span>
```
PS C:\> Disable-AzVMDiskEncryption -ResourceGroupName "Group001" -VMName "VM002"
```

<span data-ttu-id="c7942-113">此命令會針對屬於 Group001 資源群組之 VM002 的虛擬機器停用類型全部的加密。</span><span class="sxs-lookup"><span data-stu-id="c7942-113">This command disables encryption for volumes of type all for the virtual machine named VM002 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="c7942-114">由於 *未指定 VolumeType* 參數，因此 Cmdlet 會將值設定為 All。</span><span class="sxs-lookup"><span data-stu-id="c7942-114">Since the *VolumeType* parameter is not specified, the cmdlet sets the value to All.</span></span>

### <span data-ttu-id="c7942-115">範例 2：停用 Windows 虛擬機器上資料量加密</span><span class="sxs-lookup"><span data-stu-id="c7942-115">Example 2: Disable encryption for data volumes on a Windows virtual machine</span></span>
```
PS C:\> $ResourceGroup = "Group002"
PS C:\> $VMName = "VM004"
PS C:\> $VolumeType = "Data"
PS C:\> Disable-AzVMDiskEncryption -ResourceGroupName $ResourceGroup -VMName $VMName -VolumeType $VolumeType
```

<span data-ttu-id="c7942-116">此命令會針對名稱為 VM004 的虛擬機器類型資料量停用加密，該虛擬機器屬於名為 Group002 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="c7942-116">This command disables encryption for volumes of type data for the virtual machine named VM004 that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="c7942-117">參數</span><span class="sxs-lookup"><span data-stu-id="c7942-117">PARAMETERS</span></span>

### <span data-ttu-id="c7942-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7942-118">-DefaultProfile</span></span>
<span data-ttu-id="c7942-119">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c7942-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7942-120">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="c7942-120">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="c7942-121">表示此 Cmdlet 會停用擴充功能次要版本的自動升級。</span><span class="sxs-lookup"><span data-stu-id="c7942-121">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

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

### <span data-ttu-id="c7942-122">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="c7942-122">-ExtensionPublisherName</span></span>
<span data-ttu-id="c7942-123">擴充功能發行者名稱。</span><span class="sxs-lookup"><span data-stu-id="c7942-123">The extension publisher name.</span></span> <span data-ttu-id="c7942-124">僅指定此參數以覆蓋 "Microsoft.Azure.Security" 的預設值。</span><span class="sxs-lookup"><span data-stu-id="c7942-124">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

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

### <span data-ttu-id="c7942-125">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="c7942-125">-ExtensionType</span></span>
<span data-ttu-id="c7942-126">副檔名類型。</span><span class="sxs-lookup"><span data-stu-id="c7942-126">The extension type.</span></span> <span data-ttu-id="c7942-127">指定此參數以覆蓋其預設值 "AzureAzEncryption" for Windows VMs 和 "AzureCryptEncryptionForWindows" for Linux 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="c7942-127">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

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

### <span data-ttu-id="c7942-128">-強制</span><span class="sxs-lookup"><span data-stu-id="c7942-128">-Force</span></span>
<span data-ttu-id="c7942-129">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="c7942-129">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c7942-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="c7942-130">-Name</span></span>
<span data-ttu-id="c7942-131">指定代表副檔名的 Azure Resource Manager (ARM) 名稱。</span><span class="sxs-lookup"><span data-stu-id="c7942-131">Specifies the name of the Azure Resource Manager (ARM) resource that represents the extension.</span></span>
<span data-ttu-id="c7942-132">如果未指定此參數，此 Cmdlet 預設為 「Windows VMs 的 AzureAzAzEncryption」。</span><span class="sxs-lookup"><span data-stu-id="c7942-132">If this parameter is not specified, this cmdlet defaults to "AzureDiskEncryption for Windows VMs".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7942-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7942-133">-ResourceGroupName</span></span>
<span data-ttu-id="c7942-134">指定虛擬機器的資源組名。</span><span class="sxs-lookup"><span data-stu-id="c7942-134">Specifies the resource group name of the virtual machine.</span></span>

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

### <span data-ttu-id="c7942-135">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="c7942-135">-TypeHandlerVersion</span></span>
<span data-ttu-id="c7942-136">指定加密擴充功能的版本。</span><span class="sxs-lookup"><span data-stu-id="c7942-136">Specifies the version of the encryption extension.</span></span>
<span data-ttu-id="c7942-137">如果您沒有為此參數指定值，會使用最新版本的擴充功能。</span><span class="sxs-lookup"><span data-stu-id="c7942-137">If you do not specify a value for this parameter, the latest version of the extension is used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7942-138">-VMName</span><span class="sxs-lookup"><span data-stu-id="c7942-138">-VMName</span></span>
<span data-ttu-id="c7942-139">指定此 Cmdlet 停用加密的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="c7942-139">Specifies the name of the virtual machine that this cmdlet disables encryption on.</span></span>

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

### <span data-ttu-id="c7942-140">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="c7942-140">-VolumeType</span></span>
<span data-ttu-id="c7942-141">指定執行加密作業的虛擬機器捲動類型。</span><span class="sxs-lookup"><span data-stu-id="c7942-141">Specifies the type of virtual machine volumes to perform the encryption operation.</span></span>
<span data-ttu-id="c7942-142">對於 Windows 虛擬機器，有效的值為：</span><span class="sxs-lookup"><span data-stu-id="c7942-142">For Windows virtual machines, valid values are:</span></span> 
- <span data-ttu-id="c7942-143">所有</span><span class="sxs-lookup"><span data-stu-id="c7942-143">All</span></span>
- <span data-ttu-id="c7942-144">作業系統</span><span class="sxs-lookup"><span data-stu-id="c7942-144">OS</span></span>
- <span data-ttu-id="c7942-145">資料。</span><span class="sxs-lookup"><span data-stu-id="c7942-145">Data.</span></span>
<span data-ttu-id="c7942-146">如果您沒有為此參數指定值，預設值為 All。</span><span class="sxs-lookup"><span data-stu-id="c7942-146">If you do not specify a value for this parameter, the default value is All.</span></span>
<span data-ttu-id="c7942-147">Linux 目前不支援停用加密功能。</span><span class="sxs-lookup"><span data-stu-id="c7942-147">Disable encryption is not currently supported for Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: OS, Data, All

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7942-148">-確認</span><span class="sxs-lookup"><span data-stu-id="c7942-148">-Confirm</span></span>
<span data-ttu-id="c7942-149">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c7942-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7942-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7942-150">-WhatIf</span></span>
<span data-ttu-id="c7942-151">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c7942-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7942-152">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c7942-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7942-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7942-153">CommonParameters</span></span>
<span data-ttu-id="c7942-154">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c7942-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7942-155">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c7942-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7942-156">輸入</span><span class="sxs-lookup"><span data-stu-id="c7942-156">INPUTS</span></span>

### <span data-ttu-id="c7942-157">System.String</span><span class="sxs-lookup"><span data-stu-id="c7942-157">System.String</span></span>

### <span data-ttu-id="c7942-158">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c7942-158">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c7942-159">輸出</span><span class="sxs-lookup"><span data-stu-id="c7942-159">OUTPUTS</span></span>

### <span data-ttu-id="c7942-160">Microsoft.Azure.Commands.Compute.models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="c7942-160">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="c7942-161">筆記</span><span class="sxs-lookup"><span data-stu-id="c7942-161">NOTES</span></span>

## <span data-ttu-id="c7942-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="c7942-162">RELATED LINKS</span></span>

[<span data-ttu-id="c7942-163">Get-AzCRYPTCryptEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="c7942-163">Get-AzVMDiskEncryptionStatus</span></span>](./Get-AzVMDiskEncryptionStatus.md)

[<span data-ttu-id="c7942-164">Remove-AzCRYPTCryptEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="c7942-164">Remove-AzVMDiskEncryptionExtension</span></span>](./Remove-AzVMDiskEncryptionExtension.md)

[<span data-ttu-id="c7942-165">Set-Az解說EncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="c7942-165">Set-AzVMDiskEncryptionExtension</span></span>](./Set-AzVMDiskEncryptionExtension.md)


