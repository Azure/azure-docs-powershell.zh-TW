---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 9DDB3672-4C98-4449-9F29-DD9501ED4D3E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDiskEncryptionExtension.md
ms.openlocfilehash: 3fc1424fe2cde9b2137ca6925a8788fa5c8a8139
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623516"
---
# <span data-ttu-id="873ca-101">Remove-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="873ca-101">Remove-AzureRmVMDiskEncryptionExtension</span></span>

## <span data-ttu-id="873ca-102">摘要</span><span class="sxs-lookup"><span data-stu-id="873ca-102">SYNOPSIS</span></span>
<span data-ttu-id="873ca-103">從虛擬機器移除磁片加密延伸。</span><span class="sxs-lookup"><span data-stu-id="873ca-103">Removes the disk encryption extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="873ca-104">句法</span><span class="sxs-lookup"><span data-stu-id="873ca-104">SYNTAX</span></span>

```
Remove-AzureRmVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="873ca-105">說明</span><span class="sxs-lookup"><span data-stu-id="873ca-105">DESCRIPTION</span></span>
<span data-ttu-id="873ca-106">**AzureRmVMDiskEncryptionExtension** Cmdlet 會從虛擬機器中移除磁片加密延伸。</span><span class="sxs-lookup"><span data-stu-id="873ca-106">The **Remove-AzureRmVMDiskEncryptionExtension** cmdlet removes the disk encryption extension from a virtual machine.</span></span>
<span data-ttu-id="873ca-107">如果沒有指定副檔名，這個 Cmdlet 會移除針對執行 Windows 作業系統的虛擬機器或 AzureDiskEncryptionForLinux （針對 Linux 虛擬電腦）的 [預設名稱 AzureDiskEncryption] 的副檔名。</span><span class="sxs-lookup"><span data-stu-id="873ca-107">If no extension name is specified, this cmdlet removes the extension with default name AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux based virtual machines.</span></span>
<span data-ttu-id="873ca-108">這個 Cmdlet 不會停用虛擬機器上的加密。</span><span class="sxs-lookup"><span data-stu-id="873ca-108">This cmdlet does not disable encryption on the virtual machine.</span></span>
<span data-ttu-id="873ca-109">它會從虛擬機器中移除延伸和相關聯的延伸設定。</span><span class="sxs-lookup"><span data-stu-id="873ca-109">It removes the extension and the associated extension configuration from the virtual machine.</span></span>

## <span data-ttu-id="873ca-110">示例</span><span class="sxs-lookup"><span data-stu-id="873ca-110">EXAMPLES</span></span>

### <span data-ttu-id="873ca-111">範例1：從虛擬機器移除磁片加密延伸。</span><span class="sxs-lookup"><span data-stu-id="873ca-111">Example 1: Remove the disk encryption extension from a virtual machine.</span></span>
```
PS C:\> Remove-AzureRmVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM"
```

<span data-ttu-id="873ca-112">這個命令會針對執行 Windows 作業系統的虛擬機器或以 Linux 為基礎的虛擬機器（名為 MyTestVM）的 AzureDiskEncryptionForLinux，移除具有預設名稱 AzureDiskEncryption 的副檔名。</span><span class="sxs-lookup"><span data-stu-id="873ca-112">This command removes the extension with default name AzureDiskEncryption for a virtual machine that runs the Windows operating system or AzureDiskEncryptionForLinux for Linux based virtual machine named MyTestVM.</span></span>

### <span data-ttu-id="873ca-113">範例2：從虛擬機器移除特定磁片加密延伸。</span><span class="sxs-lookup"><span data-stu-id="873ca-113">Example 2: Remove a specific disk encryption extension from a virtual machine.</span></span>
```
PS C:\> Remove-AzureRmVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM" -Name "MyDiskEncryptionExtension"
```

<span data-ttu-id="873ca-114">這個命令會從名為 MyTestVM 的虛擬機器中移除名為 MyDiskEncryptionExtension 的加密延伸。</span><span class="sxs-lookup"><span data-stu-id="873ca-114">This command removes the encryption extension named MyDiskEncryptionExtension from the virtual machine named MyTestVM.</span></span>

## <span data-ttu-id="873ca-115">參數</span><span class="sxs-lookup"><span data-stu-id="873ca-115">PARAMETERS</span></span>

### <span data-ttu-id="873ca-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="873ca-116">-DefaultProfile</span></span>
<span data-ttu-id="873ca-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="873ca-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="873ca-118">-Force</span><span class="sxs-lookup"><span data-stu-id="873ca-118">-Force</span></span>
<span data-ttu-id="873ca-119">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="873ca-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="873ca-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="873ca-120">-Name</span></span>
<span data-ttu-id="873ca-121">指定代表延伸的 Azure 資源管理員資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="873ca-121">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="873ca-122">Set-AzureRmVMDiskEncryptionExtension Cmdlet 會針對執行 Windows 作業系統和 AzureDiskEncryptionForLinux Linux 虛擬機器的虛擬機器將此名稱設定為 AzureDiskEncryption。</span><span class="sxs-lookup"><span data-stu-id="873ca-122">The Set-AzureRmVMDiskEncryptionExtension cmdlet sets this name to AzureDiskEncryption for virtual machines that run the Windows operating system and AzureDiskEncryptionForLinux for Linux virtual machines.</span></span>
<span data-ttu-id="873ca-123">如果您在 **AzureRmVMDiskEncryptionExtension** Cmdlet 中變更了預設名稱，或在資源管理器範本中使用不同的資源名稱，請指定此參數。</span><span class="sxs-lookup"><span data-stu-id="873ca-123">Specify this parameter only if you changed the default name in the **Set-AzureRmVMDiskEncryptionExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

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

### <span data-ttu-id="873ca-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="873ca-124">-ResourceGroupName</span></span>
<span data-ttu-id="873ca-125">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="873ca-125">Specifies the name of the resource group for the virtual machine.</span></span>

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

### <span data-ttu-id="873ca-126">-VMName</span><span class="sxs-lookup"><span data-stu-id="873ca-126">-VMName</span></span>
<span data-ttu-id="873ca-127">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="873ca-127">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="873ca-128">-確認</span><span class="sxs-lookup"><span data-stu-id="873ca-128">-Confirm</span></span>
<span data-ttu-id="873ca-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="873ca-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="873ca-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="873ca-130">-WhatIf</span></span>
<span data-ttu-id="873ca-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="873ca-131">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="873ca-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="873ca-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="873ca-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="873ca-133">CommonParameters</span></span>
<span data-ttu-id="873ca-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="873ca-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="873ca-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="873ca-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="873ca-136">輸入</span><span class="sxs-lookup"><span data-stu-id="873ca-136">INPUTS</span></span>

## <span data-ttu-id="873ca-137">輸出</span><span class="sxs-lookup"><span data-stu-id="873ca-137">OUTPUTS</span></span>

## <span data-ttu-id="873ca-138">筆記</span><span class="sxs-lookup"><span data-stu-id="873ca-138">NOTES</span></span>

## <span data-ttu-id="873ca-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="873ca-139">RELATED LINKS</span></span>

[<span data-ttu-id="873ca-140">AzureRmVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="873ca-140">Get-AzureRmVMDiskEncryptionStatus</span></span>](./Get-AzureRmVMDiskEncryptionStatus.md)

[<span data-ttu-id="873ca-141">Set-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="873ca-141">Set-AzureRmVMDiskEncryptionExtension</span></span>](./Set-AzureRmVMDiskEncryptionExtension.md)


