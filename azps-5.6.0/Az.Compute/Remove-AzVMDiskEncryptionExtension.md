---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9DDB3672-4C98-4449-9F29-DD9501ED4D3E
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiskEncryptionExtension.md
ms.openlocfilehash: 8bdfa0afeb5b558faa91d82df9ccdc64a0b4433c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910278"
---
# <span data-ttu-id="0a3e0-101">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="0a3e0-101">Remove-AzVMDiskEncryptionExtension</span></span>

## <span data-ttu-id="0a3e0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0a3e0-102">SYNOPSIS</span></span>
<span data-ttu-id="0a3e0-103">從虛擬機器移除磁片加密擴充功能。</span><span class="sxs-lookup"><span data-stu-id="0a3e0-103">Removes the disk encryption extension from a virtual machine.</span></span>

## <span data-ttu-id="0a3e0-104">語法</span><span class="sxs-lookup"><span data-stu-id="0a3e0-104">SYNTAX</span></span>

```
Remove-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Force]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a3e0-105">描述</span><span class="sxs-lookup"><span data-stu-id="0a3e0-105">DESCRIPTION</span></span>
<span data-ttu-id="0a3e0-106">**Remove-Az VIRTUALCryptEncryptionExtension** Cmdlet 會從虛擬機器移除磁片加密擴充功能及相關擴充功能組。</span><span class="sxs-lookup"><span data-stu-id="0a3e0-106">The **Remove-AzVMDiskEncryptionExtension** cmdlet removes the disk encryption extension and the associated extension configuration from a virtual machine.</span></span> <span data-ttu-id="0a3e0-107">如果未指定副檔名，此 Cmdlet 會針對執行 Windows 作業系統的虛擬機器或 Linux 版 AzureCryptEncryptionForWindows 虛擬機器，以預設名稱 AzureCryptEncryption 移除擴充功能。</span><span class="sxs-lookup"><span data-stu-id="0a3e0-107">If no extension name is specified, this cmdlet removes the extension with default name AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux based virtual machines.</span></span> 

<span data-ttu-id="0a3e0-108">如果尚未先停用虛擬機器上的加密，此 Cmdlet 將會失敗。</span><span class="sxs-lookup"><span data-stu-id="0a3e0-108">This cmdlet will fail if encryption on the virtual machine has not been first disabled.</span></span>  <span data-ttu-id="0a3e0-109">若要在虛擬機器上停用加密，請使用[Disable-AzCRYPTCryptEncryption。](./Disable-AzVMDiskEncryption.md)</span><span class="sxs-lookup"><span data-stu-id="0a3e0-109">To disable encryption on a virtual machine, use [Disable-AzVMDiskEncryption](./Disable-AzVMDiskEncryption.md).</span></span> 

## <span data-ttu-id="0a3e0-110">例子</span><span class="sxs-lookup"><span data-stu-id="0a3e0-110">EXAMPLES</span></span>

### <span data-ttu-id="0a3e0-111">範例 1：從虛擬機器移除磁片加密擴充功能。</span><span class="sxs-lookup"><span data-stu-id="0a3e0-111">Example 1: Remove the disk encryption extension from a virtual machine.</span></span>
```
PS C:\> Remove-AzVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM"
```

<span data-ttu-id="0a3e0-112">此命令會移除執行 Windows 作業系統的虛擬機器的擴充功能，該虛擬機器的預設名稱為 AzureAzEncryption，或名為 MyTest LINUX 的 Linux 虛擬機器 AzureCryptEncryptionForWindows。</span><span class="sxs-lookup"><span data-stu-id="0a3e0-112">This command removes the extension with default name AzureDiskEncryption for a virtual machine that runs the Windows operating system or AzureDiskEncryptionForLinux for Linux based virtual machine named MyTestVM.</span></span>

### <span data-ttu-id="0a3e0-113">範例 2：從虛擬機器移除特定的磁片加密擴充功能。</span><span class="sxs-lookup"><span data-stu-id="0a3e0-113">Example 2: Remove a specific disk encryption extension from a virtual machine.</span></span>
```
PS C:\> Remove-AzVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM" -Name "MyDiskEncryptionExtension"
```

<span data-ttu-id="0a3e0-114">此命令會移除名為 MyCryptEncryptionExtension 的加密副檔名，從名為 MyTest MACHINE 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="0a3e0-114">This command removes the encryption extension named MyDiskEncryptionExtension from the virtual machine named MyTestVM.</span></span>

## <span data-ttu-id="0a3e0-115">參數</span><span class="sxs-lookup"><span data-stu-id="0a3e0-115">PARAMETERS</span></span>

### <span data-ttu-id="0a3e0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a3e0-116">-DefaultProfile</span></span>
<span data-ttu-id="0a3e0-117">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0a3e0-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a3e0-118">-強制</span><span class="sxs-lookup"><span data-stu-id="0a3e0-118">-Force</span></span>
<span data-ttu-id="0a3e0-119">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="0a3e0-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0a3e0-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="0a3e0-120">-Name</span></span>
<span data-ttu-id="0a3e0-121">指定代表擴充功能之 Azure Resource Manager 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="0a3e0-121">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="0a3e0-122">此Set-AzVMDiskEncryptionExtension Cmdlet 會針對執行 Windows 作業系統的虛擬機器和適用于 Linux 虛擬機器的 AzureCryptEncryptionForWindows，將這個名稱設定為 AzureCryptEncryption。</span><span class="sxs-lookup"><span data-stu-id="0a3e0-122">The Set-AzVMDiskEncryptionExtension cmdlet sets this name to AzureDiskEncryption for virtual machines that run the Windows operating system and AzureDiskEncryptionForLinux for Linux virtual machines.</span></span>
<span data-ttu-id="0a3e0-123">只有在您變更 **Set-AzCRYPTCryptIonExtension** Cmdlet 中的預設名稱，或在 Resource Manager 範本中使用不同的資源名稱時，才指定此參數。</span><span class="sxs-lookup"><span data-stu-id="0a3e0-123">Specify this parameter only if you changed the default name in the **Set-AzVMDiskEncryptionExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a3e0-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="0a3e0-124">-NoWait</span></span>
<span data-ttu-id="0a3e0-125">啟動作業，並立即在作業完成之前返回。</span><span class="sxs-lookup"><span data-stu-id="0a3e0-125">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="0a3e0-126">若要判斷作業是否成功完成，請使用一些其他機制。</span><span class="sxs-lookup"><span data-stu-id="0a3e0-126">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="0a3e0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a3e0-127">-ResourceGroupName</span></span>
<span data-ttu-id="0a3e0-128">指定虛擬機器的資源組名。</span><span class="sxs-lookup"><span data-stu-id="0a3e0-128">Specifies the name of the resource group for the virtual machine.</span></span>

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

### <span data-ttu-id="0a3e0-129">-VMName</span><span class="sxs-lookup"><span data-stu-id="0a3e0-129">-VMName</span></span>
<span data-ttu-id="0a3e0-130">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="0a3e0-130">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="0a3e0-131">-確認</span><span class="sxs-lookup"><span data-stu-id="0a3e0-131">-Confirm</span></span>
<span data-ttu-id="0a3e0-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="0a3e0-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a3e0-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a3e0-133">-WhatIf</span></span>
<span data-ttu-id="0a3e0-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0a3e0-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a3e0-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0a3e0-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a3e0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a3e0-136">CommonParameters</span></span>
<span data-ttu-id="0a3e0-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0a3e0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a3e0-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0a3e0-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a3e0-139">輸入</span><span class="sxs-lookup"><span data-stu-id="0a3e0-139">INPUTS</span></span>

### <span data-ttu-id="0a3e0-140">System.String</span><span class="sxs-lookup"><span data-stu-id="0a3e0-140">System.String</span></span>

## <span data-ttu-id="0a3e0-141">輸出</span><span class="sxs-lookup"><span data-stu-id="0a3e0-141">OUTPUTS</span></span>

### <span data-ttu-id="0a3e0-142">Microsoft.Azure.Commands.Compute.models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="0a3e0-142">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="0a3e0-143">筆記</span><span class="sxs-lookup"><span data-stu-id="0a3e0-143">NOTES</span></span>

## <span data-ttu-id="0a3e0-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="0a3e0-144">RELATED LINKS</span></span>

[<span data-ttu-id="0a3e0-145">Get-AzCRYPTCryptEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="0a3e0-145">Get-AzVMDiskEncryptionStatus</span></span>](./Get-AzVMDiskEncryptionStatus.md)

[<span data-ttu-id="0a3e0-146">Set-Az解說EncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="0a3e0-146">Set-AzVMDiskEncryptionExtension</span></span>](./Set-AzVMDiskEncryptionExtension.md)


