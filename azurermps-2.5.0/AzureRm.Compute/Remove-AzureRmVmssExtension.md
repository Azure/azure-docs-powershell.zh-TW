---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 8C1C12AD-5130-42E7-99BB-B13900D7A712
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmssextension
schema: 2.0.0
ms.openlocfilehash: 224b0302da76fd1c748cd77a183aa9a302dd3c9b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93799981"
---
# <span data-ttu-id="1e53f-101">Remove-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="1e53f-101">Remove-AzureRmVmssExtension</span></span>

## <span data-ttu-id="1e53f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1e53f-102">SYNOPSIS</span></span>
<span data-ttu-id="1e53f-103">從 VMSS 中移除延伸。</span><span class="sxs-lookup"><span data-stu-id="1e53f-103">Removes an extension from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e53f-104">句法</span><span class="sxs-lookup"><span data-stu-id="1e53f-104">SYNTAX</span></span>

### <span data-ttu-id="1e53f-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1e53f-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e53f-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1e53f-106">IdParameterSet</span></span>
```
Remove-AzureRmVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e53f-107">說明</span><span class="sxs-lookup"><span data-stu-id="1e53f-107">DESCRIPTION</span></span>
<span data-ttu-id="1e53f-108">**AzureRmVmssExtension** Cmdlet 會從虛擬電腦縮放集 (VMSS) 中移除延伸。</span><span class="sxs-lookup"><span data-stu-id="1e53f-108">The **Remove-AzureRmVmssExtension** cmdlet removes an extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="1e53f-109">示例</span><span class="sxs-lookup"><span data-stu-id="1e53f-109">EXAMPLES</span></span>

## <span data-ttu-id="1e53f-110">參數</span><span class="sxs-lookup"><span data-stu-id="1e53f-110">PARAMETERS</span></span>

### <span data-ttu-id="1e53f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e53f-111">-DefaultProfile</span></span>
<span data-ttu-id="1e53f-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1e53f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e53f-113">-識別碼</span><span class="sxs-lookup"><span data-stu-id="1e53f-113">-Id</span></span>
<span data-ttu-id="1e53f-114">指定此 Cmdlet 從 VMSS 移除的延伸 ID。</span><span class="sxs-lookup"><span data-stu-id="1e53f-114">Specifies the ID of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e53f-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="1e53f-115">-Name</span></span>
<span data-ttu-id="1e53f-116">指定此 Cmdlet 從 VMSS 中移除之延伸的名稱。</span><span class="sxs-lookup"><span data-stu-id="1e53f-116">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

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

### <span data-ttu-id="1e53f-117">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="1e53f-117">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="1e53f-118">指定要從中移除延伸的 VMSS。</span><span class="sxs-lookup"><span data-stu-id="1e53f-118">Specifies the VMSS from which to remove the extension from.</span></span>

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

### <span data-ttu-id="1e53f-119">-確認</span><span class="sxs-lookup"><span data-stu-id="1e53f-119">-Confirm</span></span>
<span data-ttu-id="1e53f-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1e53f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e53f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e53f-121">-WhatIf</span></span>
<span data-ttu-id="1e53f-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1e53f-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1e53f-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1e53f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e53f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e53f-124">CommonParameters</span></span>
<span data-ttu-id="1e53f-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1e53f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e53f-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1e53f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e53f-127">輸入</span><span class="sxs-lookup"><span data-stu-id="1e53f-127">INPUTS</span></span>

### <span data-ttu-id="1e53f-128">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="1e53f-128">VirtualMachineScaleSet</span></span>
<span data-ttu-id="1e53f-129">形參 "VirtualMachineScaleSet" 接受管線中 "VirtualMachineScaleSet" 類型的值</span><span class="sxs-lookup"><span data-stu-id="1e53f-129">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="1e53f-130">輸出</span><span class="sxs-lookup"><span data-stu-id="1e53f-130">OUTPUTS</span></span>

### <span data-ttu-id="1e53f-131">這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="1e53f-131">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="1e53f-132">筆記</span><span class="sxs-lookup"><span data-stu-id="1e53f-132">NOTES</span></span>

## <span data-ttu-id="1e53f-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="1e53f-133">RELATED LINKS</span></span>

[<span data-ttu-id="1e53f-134">附加 AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="1e53f-134">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)
