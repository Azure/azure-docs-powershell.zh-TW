---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 70AA9747-232E-40F2-845C-35A779F51CD2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssVM.md
ms.openlocfilehash: d035844046e238694cfec72feda9eab61b7714d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449922"
---
# <span data-ttu-id="b8ae2-101">Set-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="b8ae2-101">Set-AzureRmVmssVM</span></span>

## <span data-ttu-id="b8ae2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b8ae2-102">SYNOPSIS</span></span>
<span data-ttu-id="b8ae2-103">修改 VMSS 實例的狀態。</span><span class="sxs-lookup"><span data-stu-id="b8ae2-103">Modifies the state of a VMSS instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8ae2-104">句法</span><span class="sxs-lookup"><span data-stu-id="b8ae2-104">SYNTAX</span></span>

### <span data-ttu-id="b8ae2-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="b8ae2-105">DefaultParameter (Default)</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-Reimage]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8ae2-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="b8ae2-106">FriendMethod</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-ReimageAll]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8ae2-107">說明</span><span class="sxs-lookup"><span data-stu-id="b8ae2-107">DESCRIPTION</span></span>
<span data-ttu-id="b8ae2-108">**AzureRmVmssVM** Cmdlet 會修改虛擬機器縮放集 (VMSS) 實例的狀態。</span><span class="sxs-lookup"><span data-stu-id="b8ae2-108">The **Set-AzureRmVmssVM** cmdlet modifies the state of a Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="b8ae2-109">示例</span><span class="sxs-lookup"><span data-stu-id="b8ae2-109">EXAMPLES</span></span>

## <span data-ttu-id="b8ae2-110">參數</span><span class="sxs-lookup"><span data-stu-id="b8ae2-110">PARAMETERS</span></span>

### <span data-ttu-id="b8ae2-111">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="b8ae2-111">-InstanceId</span></span>
<span data-ttu-id="b8ae2-112">指定此 Cmdlet 修改狀態的 VMSS 實例識別碼。</span><span class="sxs-lookup"><span data-stu-id="b8ae2-112">Specifies the ID of the VMSS instance for which this cmdlet modifies state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8ae2-113">-重新映射</span><span class="sxs-lookup"><span data-stu-id="b8ae2-113">-Reimage</span></span>
<span data-ttu-id="b8ae2-114">表示此 Cmdlet reimages VMSS 實例。</span><span class="sxs-lookup"><span data-stu-id="b8ae2-114">Indicates that this cmdlet reimages the VMSS instance.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8ae2-115">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="b8ae2-115">-ReimageAll</span></span>
<span data-ttu-id="b8ae2-116">表示 Cmdlet reimages VMSS 實例中的所有磁片。</span><span class="sxs-lookup"><span data-stu-id="b8ae2-116">Indicates that the cmdlet reimages all the disks in the VMSS instance.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8ae2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8ae2-117">-ResourceGroupName</span></span>
<span data-ttu-id="b8ae2-118">指定包含 VMSS 實例之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b8ae2-118">Specifies the name of the resource group that contains the VMSS instance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8ae2-119">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="b8ae2-119">-VMScaleSetName</span></span>
<span data-ttu-id="b8ae2-120">指定此 Cmdlet 所修改之 VMSS 實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="b8ae2-120">Specifies the name of the VMSS instance that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8ae2-121">-確認</span><span class="sxs-lookup"><span data-stu-id="b8ae2-121">-Confirm</span></span>
<span data-ttu-id="b8ae2-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b8ae2-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8ae2-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8ae2-123">-WhatIf</span></span>
<span data-ttu-id="b8ae2-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b8ae2-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b8ae2-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b8ae2-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8ae2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8ae2-126">CommonParameters</span></span>
<span data-ttu-id="b8ae2-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b8ae2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8ae2-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b8ae2-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8ae2-129">輸入</span><span class="sxs-lookup"><span data-stu-id="b8ae2-129">INPUTS</span></span>

### <span data-ttu-id="b8ae2-130">所有</span><span class="sxs-lookup"><span data-stu-id="b8ae2-130">None</span></span>
<span data-ttu-id="b8ae2-131">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="b8ae2-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b8ae2-132">輸出</span><span class="sxs-lookup"><span data-stu-id="b8ae2-132">OUTPUTS</span></span>

## <span data-ttu-id="b8ae2-133">筆記</span><span class="sxs-lookup"><span data-stu-id="b8ae2-133">NOTES</span></span>

## <span data-ttu-id="b8ae2-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="b8ae2-134">RELATED LINKS</span></span>

[<span data-ttu-id="b8ae2-135">AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="b8ae2-135">Get-AzureRmVmssVM</span></span>](./Get-AzureRmVmssVM.md)
