---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssDataDisk.md
ms.openlocfilehash: b32734bbca2ec0fd554a073b2e0b5acf077874ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445056"
---
# <span data-ttu-id="9d1ed-101">Remove-AzureRmVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="9d1ed-101">Remove-AzureRmVmssDataDisk</span></span>

## <span data-ttu-id="9d1ed-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9d1ed-102">SYNOPSIS</span></span>
<span data-ttu-id="9d1ed-103">從 VMSS 中移除資料磁片。</span><span class="sxs-lookup"><span data-stu-id="9d1ed-103">Removes a data disk from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d1ed-104">句法</span><span class="sxs-lookup"><span data-stu-id="9d1ed-104">SYNTAX</span></span>

### <span data-ttu-id="9d1ed-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d1ed-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d1ed-106">LunParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d1ed-106">LunParameterSet</span></span>
```
Remove-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d1ed-107">說明</span><span class="sxs-lookup"><span data-stu-id="9d1ed-107">DESCRIPTION</span></span>
<span data-ttu-id="9d1ed-108">**AzureRmVmssDataDisk** Cmdlet 會從虛擬電腦規模集 (VMSS) 實例中移除資料磁片。</span><span class="sxs-lookup"><span data-stu-id="9d1ed-108">The **Remove-AzureRmVmssDataDisk** cmdlet removes a data disk from the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="9d1ed-109">示例</span><span class="sxs-lookup"><span data-stu-id="9d1ed-109">EXAMPLES</span></span>

### <span data-ttu-id="9d1ed-110">範例1</span><span class="sxs-lookup"><span data-stu-id="9d1ed-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1'
```

<span data-ttu-id="9d1ed-111">這個命令會從 VMSS 物件中移除名為「DataDisk1」的資料磁片。</span><span class="sxs-lookup"><span data-stu-id="9d1ed-111">This command removes the data disk named 'DataDisk1' from the VMSS object.</span></span>

### <span data-ttu-id="9d1ed-112">範例2</span><span class="sxs-lookup"><span data-stu-id="9d1ed-112">Example 2</span></span>
```
PS C:\> Remove-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Lun 0
```

<span data-ttu-id="9d1ed-113">這個命令會從 VMSS 物件中移除 LUN 0 的資料磁片。</span><span class="sxs-lookup"><span data-stu-id="9d1ed-113">This command removes the data disk of LUN 0 from the VMSS object.</span></span>

## <span data-ttu-id="9d1ed-114">參數</span><span class="sxs-lookup"><span data-stu-id="9d1ed-114">PARAMETERS</span></span>

### <span data-ttu-id="9d1ed-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d1ed-115">-DefaultProfile</span></span>
<span data-ttu-id="9d1ed-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9d1ed-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d1ed-117">-Lun</span><span class="sxs-lookup"><span data-stu-id="9d1ed-117">-Lun</span></span>
<span data-ttu-id="9d1ed-118">指定磁片的邏輯單元號碼。</span><span class="sxs-lookup"><span data-stu-id="9d1ed-118">Specifies the logical unit number of the disk.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: LunParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d1ed-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="9d1ed-119">-Name</span></span>
<span data-ttu-id="9d1ed-120">指定磁片的名稱。</span><span class="sxs-lookup"><span data-stu-id="9d1ed-120">Specifies the name of the disk.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d1ed-121">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="9d1ed-121">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="9d1ed-122">指定 VMSS 物件。</span><span class="sxs-lookup"><span data-stu-id="9d1ed-122">Specify the VMSS object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9d1ed-123">-確認</span><span class="sxs-lookup"><span data-stu-id="9d1ed-123">-Confirm</span></span>
<span data-ttu-id="9d1ed-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9d1ed-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d1ed-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d1ed-125">-WhatIf</span></span>
<span data-ttu-id="9d1ed-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9d1ed-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d1ed-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9d1ed-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d1ed-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d1ed-128">CommonParameters</span></span>
<span data-ttu-id="9d1ed-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9d1ed-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d1ed-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9d1ed-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d1ed-131">輸入</span><span class="sxs-lookup"><span data-stu-id="9d1ed-131">INPUTS</span></span>

### <span data-ttu-id="9d1ed-132">VirtualMachineScaleSet 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="9d1ed-132">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>
<span data-ttu-id="9d1ed-133">System.object 系統為 Nullable "1 [（System.object，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]）</span><span class="sxs-lookup"><span data-stu-id="9d1ed-133">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="9d1ed-134">輸出</span><span class="sxs-lookup"><span data-stu-id="9d1ed-134">OUTPUTS</span></span>

### <span data-ttu-id="9d1ed-135">VirtualMachineScaleSet 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="9d1ed-135">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="9d1ed-136">筆記</span><span class="sxs-lookup"><span data-stu-id="9d1ed-136">NOTES</span></span>

## <span data-ttu-id="9d1ed-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="9d1ed-137">RELATED LINKS</span></span>

