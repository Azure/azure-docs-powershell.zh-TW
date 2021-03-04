---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmssbootdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssBootDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssBootDiagnostic.md
ms.openlocfilehash: 58a45d6f9e3a24ca11c298935fc0d9676617737e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910526"
---
# <span data-ttu-id="8b5b9-101">Set-AzVmssBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="8b5b9-101">Set-AzVmssBootDiagnostic</span></span>

## <span data-ttu-id="8b5b9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8b5b9-102">SYNOPSIS</span></span>
<span data-ttu-id="8b5b9-103">設定虛擬機器縮放比例集開機診斷設定檔。</span><span class="sxs-lookup"><span data-stu-id="8b5b9-103">Sets the virtual machine scale set boot diagnostics profile.</span></span>

## <span data-ttu-id="8b5b9-104">語法</span><span class="sxs-lookup"><span data-stu-id="8b5b9-104">SYNTAX</span></span>

```
Set-AzVmssBootDiagnostic [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Enabled] <Boolean>]
 [[-StorageUri] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b5b9-105">描述</span><span class="sxs-lookup"><span data-stu-id="8b5b9-105">DESCRIPTION</span></span>
<span data-ttu-id="8b5b9-106">設定虛擬機器縮放比例集開機診斷設定檔。</span><span class="sxs-lookup"><span data-stu-id="8b5b9-106">Sets the virtual machine scale set boot diagnostics profile.</span></span>

## <span data-ttu-id="8b5b9-107">例子</span><span class="sxs-lookup"><span data-stu-id="8b5b9-107">EXAMPLES</span></span>

### <span data-ttu-id="8b5b9-108">範例 1：設定 VMSS 的開機診斷配置檔案屬性</span><span class="sxs-lookup"><span data-stu-id="8b5b9-108">Example 1: Set the boot diagnostics profile property for a VMSS</span></span>
```
PS C:\> $vmss = New-AzVmssConfig -Location $loc -SkuCapacity 2 -SkuName 'Standard_A0'
PS C:\> Set-AzVmssBootDiagnostic -VirtualMachineScaleSet $vmss -Enabled $true -StorageUri $storageUri;
PS C:\> New-AzVmss -ResourceGroupName $rgname -Name "ContosoVMSS" -VirtualMachineScaleSet $vmss;
```

<span data-ttu-id="8b5b9-109">此命令會針對名為 Contoso VMSS 的 VMSS 設定開機診斷配置檔案屬性。</span><span class="sxs-lookup"><span data-stu-id="8b5b9-109">This command sets boot diagnostics profile property for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="8b5b9-110">參數</span><span class="sxs-lookup"><span data-stu-id="8b5b9-110">PARAMETERS</span></span>

### <span data-ttu-id="8b5b9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b5b9-111">-DefaultProfile</span></span>
<span data-ttu-id="8b5b9-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="8b5b9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b5b9-113">-已啟用</span><span class="sxs-lookup"><span data-stu-id="8b5b9-113">-Enabled</span></span>
<span data-ttu-id="8b5b9-114">是否應該在虛擬機器縮放比例集上啟用開機診斷。</span><span class="sxs-lookup"><span data-stu-id="8b5b9-114">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b5b9-115">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="8b5b9-115">-StorageUri</span></span>
<span data-ttu-id="8b5b9-116">儲存空間帳戶的 URI，用於放置主機輸出和螢幕擷取畫面。</span><span class="sxs-lookup"><span data-stu-id="8b5b9-116">URI of the storage account to use for placing the console output and screenshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b5b9-117">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8b5b9-117">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="8b5b9-118">指定 VMSS 物件。</span><span class="sxs-lookup"><span data-stu-id="8b5b9-118">Specifies the VMSS object.</span></span>
<span data-ttu-id="8b5b9-119">您可以使用 New-AzVmssConfig Cmdlet 來建立物件。</span><span class="sxs-lookup"><span data-stu-id="8b5b9-119">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="8b5b9-120">-確認</span><span class="sxs-lookup"><span data-stu-id="8b5b9-120">-Confirm</span></span>
<span data-ttu-id="8b5b9-121">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="8b5b9-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b5b9-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b5b9-122">-WhatIf</span></span>
<span data-ttu-id="8b5b9-123">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8b5b9-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b5b9-124">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8b5b9-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b5b9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b5b9-125">CommonParameters</span></span>
<span data-ttu-id="8b5b9-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8b5b9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b5b9-127">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8b5b9-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b5b9-128">輸入</span><span class="sxs-lookup"><span data-stu-id="8b5b9-128">INPUTS</span></span>

### <span data-ttu-id="8b5b9-129">Microsoft.Azure.Commands.Compute.Automation.models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8b5b9-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="8b5b9-130">System.Nullable'1[[System.Boolean， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8b5b9-130">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="8b5b9-131">System.String</span><span class="sxs-lookup"><span data-stu-id="8b5b9-131">System.String</span></span>

## <span data-ttu-id="8b5b9-132">輸出</span><span class="sxs-lookup"><span data-stu-id="8b5b9-132">OUTPUTS</span></span>

### <span data-ttu-id="8b5b9-133">Microsoft.Azure.Commands.Compute.Automation.models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8b5b9-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="8b5b9-134">筆記</span><span class="sxs-lookup"><span data-stu-id="8b5b9-134">NOTES</span></span>

## <span data-ttu-id="8b5b9-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="8b5b9-135">RELATED LINKS</span></span>
