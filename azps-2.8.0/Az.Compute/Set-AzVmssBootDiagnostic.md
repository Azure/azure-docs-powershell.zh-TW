---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssbootdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssBootDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssBootDiagnostic.md
ms.openlocfilehash: 30abfad8ece22505755cf19f2e129a9dfad82b10
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613136"
---
# <span data-ttu-id="9987d-101">Set-AzVmssBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="9987d-101">Set-AzVmssBootDiagnostic</span></span>

## <span data-ttu-id="9987d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9987d-102">SYNOPSIS</span></span>
<span data-ttu-id="9987d-103">設定虛擬機器縮放設定啟動診斷設定檔。</span><span class="sxs-lookup"><span data-stu-id="9987d-103">Sets the virtual machine scale set boot diagnostics profile.</span></span>

## <span data-ttu-id="9987d-104">句法</span><span class="sxs-lookup"><span data-stu-id="9987d-104">SYNTAX</span></span>

```
Set-AzVmssBootDiagnostic [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Enabled] <Boolean>]
 [[-StorageUri] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9987d-105">說明</span><span class="sxs-lookup"><span data-stu-id="9987d-105">DESCRIPTION</span></span>
<span data-ttu-id="9987d-106">設定虛擬機器縮放設定啟動診斷設定檔。</span><span class="sxs-lookup"><span data-stu-id="9987d-106">Sets the virtual machine scale set boot diagnostics profile.</span></span>

## <span data-ttu-id="9987d-107">示例</span><span class="sxs-lookup"><span data-stu-id="9987d-107">EXAMPLES</span></span>

### <span data-ttu-id="9987d-108">範例1：設定 VMSS 的啟動診斷配置檔案屬性</span><span class="sxs-lookup"><span data-stu-id="9987d-108">Example 1: Set the boot diagnostics profile property for a VMSS</span></span>
```
PS C:\> $vmss = New-AzVmssConfig -Location $loc -SkuCapacity 2 -SkuName 'Standard_A0'
PS C:\> Set-AzVmssBootDiagnostic -VirtualMachineScaleSet $vmss -Enabled $true -StorageUri $storageUri;
PS C:\> New-AzVmss -ResourceGroupName $rgname -Name "ContosoVMSS" -VirtualMachineScaleSet $vmss;
```

<span data-ttu-id="9987d-109">這個命令會為名為 ContosoVMSS 的 VMSS 設定啟動診斷配置檔案屬性。</span><span class="sxs-lookup"><span data-stu-id="9987d-109">This command sets boot diagnostics profile property for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="9987d-110">參數</span><span class="sxs-lookup"><span data-stu-id="9987d-110">PARAMETERS</span></span>

### <span data-ttu-id="9987d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9987d-111">-DefaultProfile</span></span>
<span data-ttu-id="9987d-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9987d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9987d-113">-啟用</span><span class="sxs-lookup"><span data-stu-id="9987d-113">-Enabled</span></span>
<span data-ttu-id="9987d-114">是否應該在虛擬機器規模集上啟用引導診斷程式。</span><span class="sxs-lookup"><span data-stu-id="9987d-114">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="9987d-115">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="9987d-115">-StorageUri</span></span>
<span data-ttu-id="9987d-116">要用來放置主控台輸出和螢幕擷取畫面的儲存空間帳戶 URI。</span><span class="sxs-lookup"><span data-stu-id="9987d-116">URI of the storage account to use for placing the console output and screenshot.</span></span>

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

### <span data-ttu-id="9987d-117">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="9987d-117">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="9987d-118">指定 VMSS 物件。</span><span class="sxs-lookup"><span data-stu-id="9987d-118">Specifies the VMSS object.</span></span>
<span data-ttu-id="9987d-119">您可以使用 New-AzVmssConfig Cmdlet 來建立物件。</span><span class="sxs-lookup"><span data-stu-id="9987d-119">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="9987d-120">-確認</span><span class="sxs-lookup"><span data-stu-id="9987d-120">-Confirm</span></span>
<span data-ttu-id="9987d-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9987d-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9987d-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9987d-122">-WhatIf</span></span>
<span data-ttu-id="9987d-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9987d-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9987d-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9987d-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9987d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9987d-125">CommonParameters</span></span>
<span data-ttu-id="9987d-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9987d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9987d-127">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9987d-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9987d-128">輸入</span><span class="sxs-lookup"><span data-stu-id="9987d-128">INPUTS</span></span>

### <span data-ttu-id="9987d-129">PSVirtualMachineScaleSet 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="9987d-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="9987d-130">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中立，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9987d-130">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="9987d-131">System.object</span><span class="sxs-lookup"><span data-stu-id="9987d-131">System.String</span></span>

## <span data-ttu-id="9987d-132">輸出</span><span class="sxs-lookup"><span data-stu-id="9987d-132">OUTPUTS</span></span>

### <span data-ttu-id="9987d-133">PSVirtualMachineScaleSet 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="9987d-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="9987d-134">筆記</span><span class="sxs-lookup"><span data-stu-id="9987d-134">NOTES</span></span>

## <span data-ttu-id="9987d-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="9987d-135">RELATED LINKS</span></span>
