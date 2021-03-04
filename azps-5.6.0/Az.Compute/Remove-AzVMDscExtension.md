---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C7FCF2CA-2C8D-4280-BF68-10DEA96642A5
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDscExtension.md
ms.openlocfilehash: 30b3ee76a538b4db69e79397bff65e723a9bf908
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916218"
---
# <span data-ttu-id="eb6d2-101">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="eb6d2-101">Remove-AzVMDscExtension</span></span>

## <span data-ttu-id="eb6d2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="eb6d2-102">SYNOPSIS</span></span>
<span data-ttu-id="eb6d2-103">從資源群組中的虛擬機器移除 DSC 擴充處理常式。</span><span class="sxs-lookup"><span data-stu-id="eb6d2-103">Removes a DSC extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="eb6d2-104">語法</span><span class="sxs-lookup"><span data-stu-id="eb6d2-104">SYNTAX</span></span>

```
Remove-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb6d2-105">描述</span><span class="sxs-lookup"><span data-stu-id="eb6d2-105">DESCRIPTION</span></span>
<span data-ttu-id="eb6d2-106">**Remove-Az VIRTUALDscExtension** Cmdlet 會從資源群組中的虛擬機器移除想要的狀態組態 (DSC) 副檔名處理常式。</span><span class="sxs-lookup"><span data-stu-id="eb6d2-106">The **Remove-AzVMDscExtension** cmdlet removes a Desired State Configuration (DSC) extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="eb6d2-107">例子</span><span class="sxs-lookup"><span data-stu-id="eb6d2-107">EXAMPLES</span></span>

### <span data-ttu-id="eb6d2-108">範例 1：移除 DSC 擴充功能</span><span class="sxs-lookup"><span data-stu-id="eb6d2-108">Example 1: Remove a DSC extension</span></span>
```
PS C:\> Remove-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="eb6d2-109">此命令會移除名為 VM07 的虛擬機器上名為 DSC 的擴充功能。</span><span class="sxs-lookup"><span data-stu-id="eb6d2-109">This command removes the extension named DSC on virtual machine named VM07.</span></span>

## <span data-ttu-id="eb6d2-110">參數</span><span class="sxs-lookup"><span data-stu-id="eb6d2-110">PARAMETERS</span></span>

### <span data-ttu-id="eb6d2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb6d2-111">-DefaultProfile</span></span>
<span data-ttu-id="eb6d2-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="eb6d2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb6d2-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="eb6d2-113">-Name</span></span>
<span data-ttu-id="eb6d2-114">指定此 Cmdlet 移除的 DSC 副檔名。</span><span class="sxs-lookup"><span data-stu-id="eb6d2-114">Specifies the name of the DSC extension that this cmdlet removes.</span></span>
<span data-ttu-id="eb6d2-115">Cmdlet Set-AzVMDscExtension將這個名稱設定為 Microsoft.Powershell.DSC，這是 **Remove-AzCMDscExtension** 所使用的預設值。</span><span class="sxs-lookup"><span data-stu-id="eb6d2-115">The Set-AzVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the default value used by **Remove-AzVMDscExtension**.</span></span>

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

### <span data-ttu-id="eb6d2-116">-NoWait</span><span class="sxs-lookup"><span data-stu-id="eb6d2-116">-NoWait</span></span>
<span data-ttu-id="eb6d2-117">啟動作業，並立即在作業完成之前返回。</span><span class="sxs-lookup"><span data-stu-id="eb6d2-117">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="eb6d2-118">若要判斷作業是否成功完成，請使用一些其他機制。</span><span class="sxs-lookup"><span data-stu-id="eb6d2-118">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="eb6d2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb6d2-119">-ResourceGroupName</span></span>
<span data-ttu-id="eb6d2-120">指定虛擬機器的資源組名。</span><span class="sxs-lookup"><span data-stu-id="eb6d2-120">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="eb6d2-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="eb6d2-121">-VMName</span></span>
<span data-ttu-id="eb6d2-122">指定此 Cmdlet 會移除 DSC 副檔名的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="eb6d2-122">Specifies the name of a virtual machine from which this cmdlet removes the DSC extension.</span></span>

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

### <span data-ttu-id="eb6d2-123">-確認</span><span class="sxs-lookup"><span data-stu-id="eb6d2-123">-Confirm</span></span>
<span data-ttu-id="eb6d2-124">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="eb6d2-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb6d2-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb6d2-125">-WhatIf</span></span>
<span data-ttu-id="eb6d2-126">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="eb6d2-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb6d2-127">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="eb6d2-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb6d2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb6d2-128">CommonParameters</span></span>
<span data-ttu-id="eb6d2-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="eb6d2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb6d2-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eb6d2-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb6d2-131">輸入</span><span class="sxs-lookup"><span data-stu-id="eb6d2-131">INPUTS</span></span>

### <span data-ttu-id="eb6d2-132">System.String</span><span class="sxs-lookup"><span data-stu-id="eb6d2-132">System.String</span></span>

## <span data-ttu-id="eb6d2-133">輸出</span><span class="sxs-lookup"><span data-stu-id="eb6d2-133">OUTPUTS</span></span>

### <span data-ttu-id="eb6d2-134">Microsoft.Azure.Commands.Compute.models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="eb6d2-134">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="eb6d2-135">筆記</span><span class="sxs-lookup"><span data-stu-id="eb6d2-135">NOTES</span></span>

## <span data-ttu-id="eb6d2-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="eb6d2-136">RELATED LINKS</span></span>

[<span data-ttu-id="eb6d2-137">Get-AzMSDscExtension</span><span class="sxs-lookup"><span data-stu-id="eb6d2-137">Get-AzVMDscExtension</span></span>](./Get-AzVMDscExtension.md)

[<span data-ttu-id="eb6d2-138">Set-AzMSDscExtension</span><span class="sxs-lookup"><span data-stu-id="eb6d2-138">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)


