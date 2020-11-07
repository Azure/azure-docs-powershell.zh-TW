---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C7FCF2CA-2C8D-4280-BF68-10DEA96642A5
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDscExtension.md
ms.openlocfilehash: d054cb84ccd4e77ca47caf653c5a3d9322691929
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93788369"
---
# <span data-ttu-id="2bd0f-101">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="2bd0f-101">Remove-AzVMDscExtension</span></span>

## <span data-ttu-id="2bd0f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2bd0f-102">SYNOPSIS</span></span>
<span data-ttu-id="2bd0f-103">從資源群組中的虛擬機器移除 DSC 延伸處理常式。</span><span class="sxs-lookup"><span data-stu-id="2bd0f-103">Removes a DSC extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="2bd0f-104">句法</span><span class="sxs-lookup"><span data-stu-id="2bd0f-104">SYNTAX</span></span>

```
Remove-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2bd0f-105">說明</span><span class="sxs-lookup"><span data-stu-id="2bd0f-105">DESCRIPTION</span></span>
<span data-ttu-id="2bd0f-106">**AzVMDscExtension** Cmdlet 會從資源群組中的虛擬機器 (DSC) 延伸處理常式，移除所需的狀態設定。</span><span class="sxs-lookup"><span data-stu-id="2bd0f-106">The **Remove-AzVMDscExtension** cmdlet removes a Desired State Configuration (DSC) extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="2bd0f-107">示例</span><span class="sxs-lookup"><span data-stu-id="2bd0f-107">EXAMPLES</span></span>

### <span data-ttu-id="2bd0f-108">範例1：移除 DSC 副檔名</span><span class="sxs-lookup"><span data-stu-id="2bd0f-108">Example 1: Remove a DSC extension</span></span>
```
PS C:\> Remove-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="2bd0f-109">這個命令會移除名為 VM07 的虛擬機器上名為 DSC 的延伸。</span><span class="sxs-lookup"><span data-stu-id="2bd0f-109">This command removes the extension named DSC on virtual machine named VM07.</span></span>

## <span data-ttu-id="2bd0f-110">參數</span><span class="sxs-lookup"><span data-stu-id="2bd0f-110">PARAMETERS</span></span>

### <span data-ttu-id="2bd0f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bd0f-111">-DefaultProfile</span></span>
<span data-ttu-id="2bd0f-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2bd0f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2bd0f-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="2bd0f-113">-Name</span></span>
<span data-ttu-id="2bd0f-114">指定此 Cmdlet 移除的 DSC 副檔名名稱。</span><span class="sxs-lookup"><span data-stu-id="2bd0f-114">Specifies the name of the DSC extension that this cmdlet removes.</span></span>
<span data-ttu-id="2bd0f-115">Set-AzVMDscExtension Cmdlet 會將此名稱設定為 AzVMDscExtension，這是 **Remove-** 所使用的預設值。</span><span class="sxs-lookup"><span data-stu-id="2bd0f-115">The Set-AzVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the default value used by **Remove-AzVMDscExtension**.</span></span>

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

### <span data-ttu-id="2bd0f-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bd0f-116">-ResourceGroupName</span></span>
<span data-ttu-id="2bd0f-117">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2bd0f-117">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="2bd0f-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="2bd0f-118">-VMName</span></span>
<span data-ttu-id="2bd0f-119">指定此 Cmdlet 從中移除 DSC 副檔名的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="2bd0f-119">Specifies the name of a virtual machine from which this cmdlet removes the DSC extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bd0f-120">-確認</span><span class="sxs-lookup"><span data-stu-id="2bd0f-120">-Confirm</span></span>
<span data-ttu-id="2bd0f-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2bd0f-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2bd0f-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2bd0f-122">-WhatIf</span></span>
<span data-ttu-id="2bd0f-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2bd0f-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2bd0f-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2bd0f-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2bd0f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bd0f-125">CommonParameters</span></span>
<span data-ttu-id="2bd0f-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2bd0f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bd0f-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2bd0f-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bd0f-128">輸入</span><span class="sxs-lookup"><span data-stu-id="2bd0f-128">INPUTS</span></span>

### <span data-ttu-id="2bd0f-129">System.object</span><span class="sxs-lookup"><span data-stu-id="2bd0f-129">System.String</span></span>

## <span data-ttu-id="2bd0f-130">輸出</span><span class="sxs-lookup"><span data-stu-id="2bd0f-130">OUTPUTS</span></span>

### <span data-ttu-id="2bd0f-131">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="2bd0f-131">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="2bd0f-132">筆記</span><span class="sxs-lookup"><span data-stu-id="2bd0f-132">NOTES</span></span>

## <span data-ttu-id="2bd0f-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="2bd0f-133">RELATED LINKS</span></span>

[<span data-ttu-id="2bd0f-134">AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="2bd0f-134">Get-AzVMDscExtension</span></span>](./Get-AzVMDscExtension.md)

[<span data-ttu-id="2bd0f-135">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="2bd0f-135">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)


