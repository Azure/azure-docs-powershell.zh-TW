---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9DDB3672-4C98-4449-9F29-DD9501ED4D3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiskEncryptionExtension.md
ms.openlocfilehash: 084775812a887e0cc6fe497a0e0cef46ec464956
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613234"
---
# <span data-ttu-id="ad972-101">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="ad972-101">Remove-AzVMDiskEncryptionExtension</span></span>

## <span data-ttu-id="ad972-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ad972-102">SYNOPSIS</span></span>
<span data-ttu-id="ad972-103">從虛擬機器移除磁片加密延伸。</span><span class="sxs-lookup"><span data-stu-id="ad972-103">Removes the disk encryption extension from a virtual machine.</span></span>

## <span data-ttu-id="ad972-104">句法</span><span class="sxs-lookup"><span data-stu-id="ad972-104">SYNTAX</span></span>

```
Remove-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Force]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad972-105">說明</span><span class="sxs-lookup"><span data-stu-id="ad972-105">DESCRIPTION</span></span>
<span data-ttu-id="ad972-106">**AzVMDiskEncryptionExtension** Cmdlet 會從虛擬機器中移除磁片加密延伸及相關聯的延伸設定。</span><span class="sxs-lookup"><span data-stu-id="ad972-106">The **Remove-AzVMDiskEncryptionExtension** cmdlet removes the disk encryption extension and the associated extension configuration from a virtual machine.</span></span> <span data-ttu-id="ad972-107">如果沒有指定副檔名，這個 Cmdlet 會移除針對執行 Windows 作業系統的虛擬機器或 AzureDiskEncryptionForLinux （針對 Linux 虛擬電腦）的 [預設名稱 AzureDiskEncryption] 的副檔名。</span><span class="sxs-lookup"><span data-stu-id="ad972-107">If no extension name is specified, this cmdlet removes the extension with default name AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux based virtual machines.</span></span> 

<span data-ttu-id="ad972-108">如果虛擬機器上的加密未事先停用，此 Cmdlet 將會失敗。</span><span class="sxs-lookup"><span data-stu-id="ad972-108">This cmdlet will fail if encryption on the virtual machine has not been first disabled.</span></span>  <span data-ttu-id="ad972-109">若要在虛擬機器上停用加密，請使用 [ [停用-AzVMDiskEncryption](./Disable-AzVMDiskEncryption.md)]。</span><span class="sxs-lookup"><span data-stu-id="ad972-109">To disable encryption on a virtual machine, use [Disable-AzVMDiskEncryption](./Disable-AzVMDiskEncryption.md).</span></span> 

## <span data-ttu-id="ad972-110">示例</span><span class="sxs-lookup"><span data-stu-id="ad972-110">EXAMPLES</span></span>

### <span data-ttu-id="ad972-111">範例1：從虛擬機器移除磁片加密延伸。</span><span class="sxs-lookup"><span data-stu-id="ad972-111">Example 1: Remove the disk encryption extension from a virtual machine.</span></span>
```
PS C:\> Remove-AzVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM"
```

<span data-ttu-id="ad972-112">這個命令會針對執行 Windows 作業系統的虛擬機器或以 Linux 為基礎的虛擬機器（名為 MyTestVM）的 AzureDiskEncryptionForLinux，移除具有預設名稱 AzureDiskEncryption 的副檔名。</span><span class="sxs-lookup"><span data-stu-id="ad972-112">This command removes the extension with default name AzureDiskEncryption for a virtual machine that runs the Windows operating system or AzureDiskEncryptionForLinux for Linux based virtual machine named MyTestVM.</span></span>

### <span data-ttu-id="ad972-113">範例2：從虛擬機器移除特定磁片加密延伸。</span><span class="sxs-lookup"><span data-stu-id="ad972-113">Example 2: Remove a specific disk encryption extension from a virtual machine.</span></span>
```
PS C:\> Remove-AzVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM" -Name "MyDiskEncryptionExtension"
```

<span data-ttu-id="ad972-114">這個命令會從名為 MyTestVM 的虛擬機器中移除名為 MyDiskEncryptionExtension 的加密延伸。</span><span class="sxs-lookup"><span data-stu-id="ad972-114">This command removes the encryption extension named MyDiskEncryptionExtension from the virtual machine named MyTestVM.</span></span>

## <span data-ttu-id="ad972-115">參數</span><span class="sxs-lookup"><span data-stu-id="ad972-115">PARAMETERS</span></span>

### <span data-ttu-id="ad972-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad972-116">-DefaultProfile</span></span>
<span data-ttu-id="ad972-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ad972-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad972-118">-Force</span><span class="sxs-lookup"><span data-stu-id="ad972-118">-Force</span></span>
<span data-ttu-id="ad972-119">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="ad972-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ad972-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="ad972-120">-Name</span></span>
<span data-ttu-id="ad972-121">指定代表延伸的 Azure 資源管理員資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="ad972-121">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="ad972-122">Set-AzVMDiskEncryptionExtension Cmdlet 會針對執行 Windows 作業系統和 AzureDiskEncryptionForLinux Linux 虛擬機器的虛擬機器將此名稱設定為 AzureDiskEncryption。</span><span class="sxs-lookup"><span data-stu-id="ad972-122">The Set-AzVMDiskEncryptionExtension cmdlet sets this name to AzureDiskEncryption for virtual machines that run the Windows operating system and AzureDiskEncryptionForLinux for Linux virtual machines.</span></span>
<span data-ttu-id="ad972-123">如果您在 **AzVMDiskEncryptionExtension** Cmdlet 中變更了預設名稱，或在資源管理器範本中使用不同的資源名稱，請指定此參數。</span><span class="sxs-lookup"><span data-stu-id="ad972-123">Specify this parameter only if you changed the default name in the **Set-AzVMDiskEncryptionExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

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

### <span data-ttu-id="ad972-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ad972-124">-NoWait</span></span>
<span data-ttu-id="ad972-125">在作業完成之前，立即開始作業並立即返回。</span><span class="sxs-lookup"><span data-stu-id="ad972-125">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="ad972-126">若要判斷該作業是否已順利完成，請使用一些其他的機制。</span><span class="sxs-lookup"><span data-stu-id="ad972-126">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="ad972-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad972-127">-ResourceGroupName</span></span>
<span data-ttu-id="ad972-128">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ad972-128">Specifies the name of the resource group for the virtual machine.</span></span>

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

### <span data-ttu-id="ad972-129">-VMName</span><span class="sxs-lookup"><span data-stu-id="ad972-129">-VMName</span></span>
<span data-ttu-id="ad972-130">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="ad972-130">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="ad972-131">-確認</span><span class="sxs-lookup"><span data-stu-id="ad972-131">-Confirm</span></span>
<span data-ttu-id="ad972-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ad972-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad972-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad972-133">-WhatIf</span></span>
<span data-ttu-id="ad972-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ad972-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad972-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ad972-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad972-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad972-136">CommonParameters</span></span>
<span data-ttu-id="ad972-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ad972-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad972-138">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ad972-138">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad972-139">輸入</span><span class="sxs-lookup"><span data-stu-id="ad972-139">INPUTS</span></span>

### <span data-ttu-id="ad972-140">System.object</span><span class="sxs-lookup"><span data-stu-id="ad972-140">System.String</span></span>

## <span data-ttu-id="ad972-141">輸出</span><span class="sxs-lookup"><span data-stu-id="ad972-141">OUTPUTS</span></span>

### <span data-ttu-id="ad972-142">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="ad972-142">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="ad972-143">筆記</span><span class="sxs-lookup"><span data-stu-id="ad972-143">NOTES</span></span>

## <span data-ttu-id="ad972-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="ad972-144">RELATED LINKS</span></span>

[<span data-ttu-id="ad972-145">AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="ad972-145">Get-AzVMDiskEncryptionStatus</span></span>](./Get-AzVMDiskEncryptionStatus.md)

[<span data-ttu-id="ad972-146">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="ad972-146">Set-AzVMDiskEncryptionExtension</span></span>](./Set-AzVMDiskEncryptionExtension.md)


