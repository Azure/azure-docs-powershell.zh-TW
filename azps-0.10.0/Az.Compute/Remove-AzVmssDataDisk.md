---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVmssDataDisk.md
ms.openlocfilehash: 30836628d6be41e06eaf8982fcc59646fb5b5e89
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93796001"
---
# <span data-ttu-id="7dbaa-101">Remove-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="7dbaa-101">Remove-AzVmssDataDisk</span></span>

## <span data-ttu-id="7dbaa-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7dbaa-102">SYNOPSIS</span></span>
<span data-ttu-id="7dbaa-103">從 VMSS 中移除資料磁片。</span><span class="sxs-lookup"><span data-stu-id="7dbaa-103">Removes a data disk from the VMSS.</span></span>

## <span data-ttu-id="7dbaa-104">句法</span><span class="sxs-lookup"><span data-stu-id="7dbaa-104">SYNTAX</span></span>

### <span data-ttu-id="7dbaa-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7dbaa-105">NameParameterSet</span></span>
```
Remove-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7dbaa-106">LunParameterSet</span><span class="sxs-lookup"><span data-stu-id="7dbaa-106">LunParameterSet</span></span>
```
Remove-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7dbaa-107">說明</span><span class="sxs-lookup"><span data-stu-id="7dbaa-107">DESCRIPTION</span></span>
<span data-ttu-id="7dbaa-108">**AzVmssDataDisk** Cmdlet 會從虛擬電腦規模集 (VMSS) 實例中移除資料磁片。</span><span class="sxs-lookup"><span data-stu-id="7dbaa-108">The **Remove-AzVmssDataDisk** cmdlet removes a data disk from the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="7dbaa-109">示例</span><span class="sxs-lookup"><span data-stu-id="7dbaa-109">EXAMPLES</span></span>

### <span data-ttu-id="7dbaa-110">範例1</span><span class="sxs-lookup"><span data-stu-id="7dbaa-110">Example 1</span></span>
```
PS C:\> Remove-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1'
```

<span data-ttu-id="7dbaa-111">這個命令會從 VMSS 物件中移除名為「DataDisk1」的資料磁片。</span><span class="sxs-lookup"><span data-stu-id="7dbaa-111">This command removes the data disk named 'DataDisk1' from the VMSS object.</span></span>

### <span data-ttu-id="7dbaa-112">範例2</span><span class="sxs-lookup"><span data-stu-id="7dbaa-112">Example 2</span></span>
```
PS C:\> Remove-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Lun 0
```

<span data-ttu-id="7dbaa-113">這個命令會從 VMSS 物件中移除 LUN 0 的資料磁片。</span><span class="sxs-lookup"><span data-stu-id="7dbaa-113">This command removes the data disk of LUN 0 from the VMSS object.</span></span>

## <span data-ttu-id="7dbaa-114">參數</span><span class="sxs-lookup"><span data-stu-id="7dbaa-114">PARAMETERS</span></span>

### <span data-ttu-id="7dbaa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7dbaa-115">-DefaultProfile</span></span>
<span data-ttu-id="7dbaa-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7dbaa-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7dbaa-117">-Lun</span><span class="sxs-lookup"><span data-stu-id="7dbaa-117">-Lun</span></span>
<span data-ttu-id="7dbaa-118">指定磁片的邏輯單元號碼。</span><span class="sxs-lookup"><span data-stu-id="7dbaa-118">Specifies the logical unit number of the disk.</span></span>

```yaml
Type: Int32
Parameter Sets: LunParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7dbaa-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="7dbaa-119">-Name</span></span>
<span data-ttu-id="7dbaa-120">指定磁片的名稱。</span><span class="sxs-lookup"><span data-stu-id="7dbaa-120">Specifies the name of the disk.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7dbaa-121">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="7dbaa-121">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="7dbaa-122">指定 VMSS 物件。</span><span class="sxs-lookup"><span data-stu-id="7dbaa-122">Specify the VMSS object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7dbaa-123">-確認</span><span class="sxs-lookup"><span data-stu-id="7dbaa-123">-Confirm</span></span>
<span data-ttu-id="7dbaa-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7dbaa-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7dbaa-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7dbaa-125">-WhatIf</span></span>
<span data-ttu-id="7dbaa-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7dbaa-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7dbaa-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7dbaa-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7dbaa-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7dbaa-128">CommonParameters</span></span>
<span data-ttu-id="7dbaa-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7dbaa-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7dbaa-130">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7dbaa-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7dbaa-131">輸入</span><span class="sxs-lookup"><span data-stu-id="7dbaa-131">INPUTS</span></span>

### <span data-ttu-id="7dbaa-132">VirtualMachineScaleSet 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="7dbaa-132">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>
<span data-ttu-id="7dbaa-133">System.object 系統為 Nullable "1 [（System.object，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]）</span><span class="sxs-lookup"><span data-stu-id="7dbaa-133">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="7dbaa-134">輸出</span><span class="sxs-lookup"><span data-stu-id="7dbaa-134">OUTPUTS</span></span>

### <span data-ttu-id="7dbaa-135">VirtualMachineScaleSet 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="7dbaa-135">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="7dbaa-136">筆記</span><span class="sxs-lookup"><span data-stu-id="7dbaa-136">NOTES</span></span>

## <span data-ttu-id="7dbaa-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="7dbaa-137">RELATED LINKS</span></span>

