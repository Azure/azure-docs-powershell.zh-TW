---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 8C1C12AD-5130-42E7-99BB-B13900D7A712
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssExtension.md
ms.openlocfilehash: f99df428f99ec0e75eb4b1b220dde657be6f7458
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445047"
---
# <span data-ttu-id="23b1b-101">Remove-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="23b1b-101">Remove-AzureRmVmssExtension</span></span>

## <span data-ttu-id="23b1b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="23b1b-102">SYNOPSIS</span></span>
<span data-ttu-id="23b1b-103">從 VMSS 中移除延伸。</span><span class="sxs-lookup"><span data-stu-id="23b1b-103">Removes an extension from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23b1b-104">句法</span><span class="sxs-lookup"><span data-stu-id="23b1b-104">SYNTAX</span></span>

### <span data-ttu-id="23b1b-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="23b1b-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23b1b-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="23b1b-106">IdParameterSet</span></span>
```
Remove-AzureRmVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23b1b-107">說明</span><span class="sxs-lookup"><span data-stu-id="23b1b-107">DESCRIPTION</span></span>
<span data-ttu-id="23b1b-108">**AzureRmVmssExtension** Cmdlet 會從虛擬電腦縮放集 (VMSS) 中移除延伸。</span><span class="sxs-lookup"><span data-stu-id="23b1b-108">The **Remove-AzureRmVmssExtension** cmdlet removes an extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="23b1b-109">示例</span><span class="sxs-lookup"><span data-stu-id="23b1b-109">EXAMPLES</span></span>

## <span data-ttu-id="23b1b-110">參數</span><span class="sxs-lookup"><span data-stu-id="23b1b-110">PARAMETERS</span></span>

### <span data-ttu-id="23b1b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23b1b-111">-DefaultProfile</span></span>
<span data-ttu-id="23b1b-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="23b1b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23b1b-113">-識別碼</span><span class="sxs-lookup"><span data-stu-id="23b1b-113">-Id</span></span>
<span data-ttu-id="23b1b-114">指定此 Cmdlet 從 VMSS 移除的延伸 ID。</span><span class="sxs-lookup"><span data-stu-id="23b1b-114">Specifies the ID of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23b1b-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="23b1b-115">-Name</span></span>
<span data-ttu-id="23b1b-116">指定此 Cmdlet 從 VMSS 中移除之延伸的名稱。</span><span class="sxs-lookup"><span data-stu-id="23b1b-116">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

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

### <span data-ttu-id="23b1b-117">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="23b1b-117">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="23b1b-118">指定要從中移除延伸的 VMSS。</span><span class="sxs-lookup"><span data-stu-id="23b1b-118">Specifies the VMSS from which to remove the extension from.</span></span>

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

### <span data-ttu-id="23b1b-119">-確認</span><span class="sxs-lookup"><span data-stu-id="23b1b-119">-Confirm</span></span>
<span data-ttu-id="23b1b-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="23b1b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23b1b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23b1b-121">-WhatIf</span></span>
<span data-ttu-id="23b1b-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="23b1b-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="23b1b-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="23b1b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23b1b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23b1b-124">CommonParameters</span></span>
<span data-ttu-id="23b1b-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="23b1b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23b1b-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="23b1b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23b1b-127">輸入</span><span class="sxs-lookup"><span data-stu-id="23b1b-127">INPUTS</span></span>

## <span data-ttu-id="23b1b-128">輸出</span><span class="sxs-lookup"><span data-stu-id="23b1b-128">OUTPUTS</span></span>

### <span data-ttu-id="23b1b-129">這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="23b1b-129">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="23b1b-130">筆記</span><span class="sxs-lookup"><span data-stu-id="23b1b-130">NOTES</span></span>

## <span data-ttu-id="23b1b-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="23b1b-131">RELATED LINKS</span></span>

[<span data-ttu-id="23b1b-132">附加 AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="23b1b-132">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)
