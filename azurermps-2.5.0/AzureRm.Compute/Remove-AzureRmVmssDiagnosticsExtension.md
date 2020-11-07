---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 5F135E64-9432-4D08-961F-4604410378A3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmssdiagnosticsextension
schema: 2.0.0
ms.openlocfilehash: 74bb0bee84615618f464cfbfd86dcb2b7dde387b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801701"
---
# <span data-ttu-id="78fe7-101">Remove-AzureRmVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="78fe7-101">Remove-AzureRmVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="78fe7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="78fe7-102">SYNOPSIS</span></span>
<span data-ttu-id="78fe7-103">從 VMSS 移除診斷延伸。</span><span class="sxs-lookup"><span data-stu-id="78fe7-103">Removes a diagnostics extension from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78fe7-104">句法</span><span class="sxs-lookup"><span data-stu-id="78fe7-104">SYNTAX</span></span>

```
Remove-AzureRmVmssDiagnosticsExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78fe7-105">說明</span><span class="sxs-lookup"><span data-stu-id="78fe7-105">DESCRIPTION</span></span>
<span data-ttu-id="78fe7-106">**AzureRmVmssDiagnosticsExtension** Cmdlet 會從虛擬機器縮放集 (VMSS) 中移除診斷延伸。</span><span class="sxs-lookup"><span data-stu-id="78fe7-106">The **Remove-AzureRmVmssDiagnosticsExtension** cmdlet removes a diagnostics extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="78fe7-107">示例</span><span class="sxs-lookup"><span data-stu-id="78fe7-107">EXAMPLES</span></span>

### <span data-ttu-id="78fe7-108">範例1：從 VMSS 移除診斷延伸</span><span class="sxs-lookup"><span data-stu-id="78fe7-108">Example 1: Remove a diagnostics extension from the VMSS</span></span>
```
PS C:\> Remove-AzureRmVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -Name $extName
```

<span data-ttu-id="78fe7-109">這個命令會從 VMSS 中移除診斷延伸。</span><span class="sxs-lookup"><span data-stu-id="78fe7-109">This command removes diagnostics extension from the VMSS.</span></span>

## <span data-ttu-id="78fe7-110">參數</span><span class="sxs-lookup"><span data-stu-id="78fe7-110">PARAMETERS</span></span>

### <span data-ttu-id="78fe7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78fe7-111">-DefaultProfile</span></span>
<span data-ttu-id="78fe7-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="78fe7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78fe7-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="78fe7-113">-Name</span></span>
<span data-ttu-id="78fe7-114">指定此 Cmdlet 從 VMSS 中移除之延伸的名稱。</span><span class="sxs-lookup"><span data-stu-id="78fe7-114">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78fe7-115">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="78fe7-115">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="78fe7-116">指定要移除延伸的 VMSS。</span><span class="sxs-lookup"><span data-stu-id="78fe7-116">Specifies the VMSS from which to remove the extension.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="78fe7-117">-確認</span><span class="sxs-lookup"><span data-stu-id="78fe7-117">-Confirm</span></span>
<span data-ttu-id="78fe7-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="78fe7-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78fe7-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78fe7-119">-WhatIf</span></span>
<span data-ttu-id="78fe7-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="78fe7-120">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="78fe7-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="78fe7-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78fe7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78fe7-122">CommonParameters</span></span>
<span data-ttu-id="78fe7-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="78fe7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78fe7-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="78fe7-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78fe7-125">輸入</span><span class="sxs-lookup"><span data-stu-id="78fe7-125">INPUTS</span></span>

### <span data-ttu-id="78fe7-126">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="78fe7-126">VirtualMachineScaleSet</span></span>
<span data-ttu-id="78fe7-127">形參 "VirtualMachineScaleSet" 接受管線中 "VirtualMachineScaleSet" 類型的值</span><span class="sxs-lookup"><span data-stu-id="78fe7-127">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="78fe7-128">輸出</span><span class="sxs-lookup"><span data-stu-id="78fe7-128">OUTPUTS</span></span>

###  
<span data-ttu-id="78fe7-129">這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="78fe7-129">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="78fe7-130">筆記</span><span class="sxs-lookup"><span data-stu-id="78fe7-130">NOTES</span></span>

## <span data-ttu-id="78fe7-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="78fe7-131">RELATED LINKS</span></span>

[<span data-ttu-id="78fe7-132">附加 AzureRmVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="78fe7-132">Add-AzureRmVmssDiagnosticsExtension</span></span>](./Add-AzureRmVmssDiagnosticsExtension.md)

[<span data-ttu-id="78fe7-133">移除-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="78fe7-133">Remove-AzureRmVMDiagnosticsExtension</span></span>](./Remove-AzureRmVMDiagnosticsExtension.md)

[<span data-ttu-id="78fe7-134">移除-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="78fe7-134">Remove-AzureRmVmssExtension</span></span>](./Remove-AzureRmVmssExtension.md)


