---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 8C1C12AD-5130-42E7-99BB-B13900D7A712
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVmssExtension.md
ms.openlocfilehash: 8044be4e6d9c353dd50420fe73066a8f47d53855
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795978"
---
# <span data-ttu-id="08a37-101">Remove-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="08a37-101">Remove-AzVmssExtension</span></span>

## <span data-ttu-id="08a37-102">摘要</span><span class="sxs-lookup"><span data-stu-id="08a37-102">SYNOPSIS</span></span>
<span data-ttu-id="08a37-103">從 VMSS 中移除延伸。</span><span class="sxs-lookup"><span data-stu-id="08a37-103">Removes an extension from the VMSS.</span></span>

## <span data-ttu-id="08a37-104">句法</span><span class="sxs-lookup"><span data-stu-id="08a37-104">SYNTAX</span></span>

### <span data-ttu-id="08a37-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="08a37-105">NameParameterSet</span></span>
```
Remove-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08a37-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="08a37-106">IdParameterSet</span></span>
```
Remove-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08a37-107">說明</span><span class="sxs-lookup"><span data-stu-id="08a37-107">DESCRIPTION</span></span>
<span data-ttu-id="08a37-108">**AzVmssExtension** Cmdlet 會從虛擬電腦縮放集 (VMSS) 中移除延伸。</span><span class="sxs-lookup"><span data-stu-id="08a37-108">The **Remove-AzVmssExtension** cmdlet removes an extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="08a37-109">示例</span><span class="sxs-lookup"><span data-stu-id="08a37-109">EXAMPLES</span></span>

### <span data-ttu-id="08a37-110">範例1：移除 VMSS 的延伸功能</span><span class="sxs-lookup"><span data-stu-id="08a37-110">Example 1: Remove extension from the VMSS</span></span>
```
PS C:\> Remove-AzVmssExtension -VirtualMachineScaleSet $VMSS -Name $extName
```

## <span data-ttu-id="08a37-111">參數</span><span class="sxs-lookup"><span data-stu-id="08a37-111">PARAMETERS</span></span>

### <span data-ttu-id="08a37-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08a37-112">-DefaultProfile</span></span>
<span data-ttu-id="08a37-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="08a37-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08a37-114">-識別碼</span><span class="sxs-lookup"><span data-stu-id="08a37-114">-Id</span></span>
<span data-ttu-id="08a37-115">指定此 Cmdlet 從 VMSS 移除的延伸 ID。</span><span class="sxs-lookup"><span data-stu-id="08a37-115">Specifies the ID of the extension that this cmdlet removes from the VMSS.</span></span>

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

### <span data-ttu-id="08a37-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="08a37-116">-Name</span></span>
<span data-ttu-id="08a37-117">指定此 Cmdlet 從 VMSS 中移除之延伸的名稱。</span><span class="sxs-lookup"><span data-stu-id="08a37-117">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

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

### <span data-ttu-id="08a37-118">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="08a37-118">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="08a37-119">指定要從中移除延伸的 VMSS。</span><span class="sxs-lookup"><span data-stu-id="08a37-119">Specifies the VMSS from which to remove the extension from.</span></span>

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

### <span data-ttu-id="08a37-120">-確認</span><span class="sxs-lookup"><span data-stu-id="08a37-120">-Confirm</span></span>
<span data-ttu-id="08a37-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="08a37-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08a37-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08a37-122">-WhatIf</span></span>
<span data-ttu-id="08a37-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="08a37-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="08a37-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="08a37-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08a37-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08a37-125">CommonParameters</span></span>
<span data-ttu-id="08a37-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="08a37-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08a37-127">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="08a37-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08a37-128">輸入</span><span class="sxs-lookup"><span data-stu-id="08a37-128">INPUTS</span></span>

### <span data-ttu-id="08a37-129">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="08a37-129">VirtualMachineScaleSet</span></span>
<span data-ttu-id="08a37-130">形參 "VirtualMachineScaleSet" 接受管線中 "VirtualMachineScaleSet" 類型的值</span><span class="sxs-lookup"><span data-stu-id="08a37-130">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="08a37-131">輸出</span><span class="sxs-lookup"><span data-stu-id="08a37-131">OUTPUTS</span></span>

### <span data-ttu-id="08a37-132">這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="08a37-132">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="08a37-133">筆記</span><span class="sxs-lookup"><span data-stu-id="08a37-133">NOTES</span></span>

## <span data-ttu-id="08a37-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="08a37-134">RELATED LINKS</span></span>

[<span data-ttu-id="08a37-135">附加 AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="08a37-135">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)
