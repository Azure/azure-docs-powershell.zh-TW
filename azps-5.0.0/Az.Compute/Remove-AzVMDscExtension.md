---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C7FCF2CA-2C8D-4280-BF68-10DEA96642A5
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDscExtension.md
ms.openlocfilehash: 13140b5434cdc29754b8041a32f328e0b855fed2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137680"
---
# <span data-ttu-id="ad360-101">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="ad360-101">Remove-AzVMDscExtension</span></span>

## <span data-ttu-id="ad360-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ad360-102">SYNOPSIS</span></span>
<span data-ttu-id="ad360-103">從資源群組中的虛擬機器移除 DSC 延伸處理常式。</span><span class="sxs-lookup"><span data-stu-id="ad360-103">Removes a DSC extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="ad360-104">句法</span><span class="sxs-lookup"><span data-stu-id="ad360-104">SYNTAX</span></span>

```
Remove-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad360-105">說明</span><span class="sxs-lookup"><span data-stu-id="ad360-105">DESCRIPTION</span></span>
<span data-ttu-id="ad360-106">**AzVMDscExtension** Cmdlet 會從資源群組中的虛擬機器 (DSC) 延伸處理常式，移除所需的狀態設定。</span><span class="sxs-lookup"><span data-stu-id="ad360-106">The **Remove-AzVMDscExtension** cmdlet removes a Desired State Configuration (DSC) extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="ad360-107">示例</span><span class="sxs-lookup"><span data-stu-id="ad360-107">EXAMPLES</span></span>

### <span data-ttu-id="ad360-108">範例1：移除 DSC 副檔名</span><span class="sxs-lookup"><span data-stu-id="ad360-108">Example 1: Remove a DSC extension</span></span>
```
PS C:\> Remove-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="ad360-109">這個命令會移除名為 VM07 的虛擬機器上名為 DSC 的延伸。</span><span class="sxs-lookup"><span data-stu-id="ad360-109">This command removes the extension named DSC on virtual machine named VM07.</span></span>

## <span data-ttu-id="ad360-110">參數</span><span class="sxs-lookup"><span data-stu-id="ad360-110">PARAMETERS</span></span>

### <span data-ttu-id="ad360-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad360-111">-DefaultProfile</span></span>
<span data-ttu-id="ad360-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ad360-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad360-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="ad360-113">-Name</span></span>
<span data-ttu-id="ad360-114">指定此 Cmdlet 移除的 DSC 副檔名名稱。</span><span class="sxs-lookup"><span data-stu-id="ad360-114">Specifies the name of the DSC extension that this cmdlet removes.</span></span>
<span data-ttu-id="ad360-115">Set-AzVMDscExtension Cmdlet 會將此名稱設定為 AzVMDscExtension，這是 **Remove-** 所使用的預設值。</span><span class="sxs-lookup"><span data-stu-id="ad360-115">The Set-AzVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the default value used by **Remove-AzVMDscExtension**.</span></span>

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

### <span data-ttu-id="ad360-116">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ad360-116">-NoWait</span></span>
<span data-ttu-id="ad360-117">在作業完成之前，立即開始作業並立即返回。</span><span class="sxs-lookup"><span data-stu-id="ad360-117">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="ad360-118">若要判斷該作業是否已順利完成，請使用一些其他的機制。</span><span class="sxs-lookup"><span data-stu-id="ad360-118">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad360-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad360-119">-ResourceGroupName</span></span>
<span data-ttu-id="ad360-120">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ad360-120">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="ad360-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="ad360-121">-VMName</span></span>
<span data-ttu-id="ad360-122">指定此 Cmdlet 從中移除 DSC 副檔名的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="ad360-122">Specifies the name of a virtual machine from which this cmdlet removes the DSC extension.</span></span>

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

### <span data-ttu-id="ad360-123">-確認</span><span class="sxs-lookup"><span data-stu-id="ad360-123">-Confirm</span></span>
<span data-ttu-id="ad360-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ad360-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad360-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad360-125">-WhatIf</span></span>
<span data-ttu-id="ad360-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ad360-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad360-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ad360-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad360-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad360-128">CommonParameters</span></span>
<span data-ttu-id="ad360-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ad360-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad360-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ad360-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad360-131">輸入</span><span class="sxs-lookup"><span data-stu-id="ad360-131">INPUTS</span></span>

### <span data-ttu-id="ad360-132">System.object</span><span class="sxs-lookup"><span data-stu-id="ad360-132">System.String</span></span>

## <span data-ttu-id="ad360-133">輸出</span><span class="sxs-lookup"><span data-stu-id="ad360-133">OUTPUTS</span></span>

### <span data-ttu-id="ad360-134">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="ad360-134">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="ad360-135">筆記</span><span class="sxs-lookup"><span data-stu-id="ad360-135">NOTES</span></span>

## <span data-ttu-id="ad360-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="ad360-136">RELATED LINKS</span></span>

[<span data-ttu-id="ad360-137">AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="ad360-137">Get-AzVMDscExtension</span></span>](./Get-AzVMDscExtension.md)

[<span data-ttu-id="ad360-138">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="ad360-138">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)


