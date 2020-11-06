---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: A65E82D5-706B-4470-A51E-936E381DA78F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMCustomScriptExtension.md
ms.openlocfilehash: 53c9bc55c2ac8237544f293a4c42352d89681852
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613240"
---
# <span data-ttu-id="c9360-101">Remove-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="c9360-101">Remove-AzVMCustomScriptExtension</span></span>

## <span data-ttu-id="c9360-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c9360-102">SYNOPSIS</span></span>
<span data-ttu-id="c9360-103">從虛擬機器中移除自訂腳本延伸。</span><span class="sxs-lookup"><span data-stu-id="c9360-103">Removes a custom script extension from a virtual machine.</span></span>

## <span data-ttu-id="c9360-104">句法</span><span class="sxs-lookup"><span data-stu-id="c9360-104">SYNTAX</span></span>

```
Remove-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9360-105">說明</span><span class="sxs-lookup"><span data-stu-id="c9360-105">DESCRIPTION</span></span>
<span data-ttu-id="c9360-106">**AzVMCustomScriptExtension** Cmdlet 會從虛擬機器中移除自訂腳本虛擬電腦延伸。</span><span class="sxs-lookup"><span data-stu-id="c9360-106">The **Remove-AzVMCustomScriptExtension** cmdlet removes a custom script Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="c9360-107">示例</span><span class="sxs-lookup"><span data-stu-id="c9360-107">EXAMPLES</span></span>

## <span data-ttu-id="c9360-108">參數</span><span class="sxs-lookup"><span data-stu-id="c9360-108">PARAMETERS</span></span>

### <span data-ttu-id="c9360-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9360-109">-DefaultProfile</span></span>
<span data-ttu-id="c9360-110">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c9360-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9360-111">-Force</span><span class="sxs-lookup"><span data-stu-id="c9360-111">-Force</span></span>
<span data-ttu-id="c9360-112">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="c9360-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c9360-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="c9360-113">-Name</span></span>
<span data-ttu-id="c9360-114">指定此 Cmdlet 移除的自訂腳本副檔名的名稱。</span><span class="sxs-lookup"><span data-stu-id="c9360-114">Specifies the name of the custom script extension that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9360-115">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c9360-115">-NoWait</span></span>
<span data-ttu-id="c9360-116">在作業完成之前，立即開始作業並立即返回。</span><span class="sxs-lookup"><span data-stu-id="c9360-116">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="c9360-117">若要判斷該作業是否已順利完成，請使用一些其他的機制。</span><span class="sxs-lookup"><span data-stu-id="c9360-117">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="c9360-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9360-118">-ResourceGroupName</span></span>
<span data-ttu-id="c9360-119">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c9360-119">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="c9360-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="c9360-120">-VMName</span></span>
<span data-ttu-id="c9360-121">指定此 Cmdlet 從中移除自訂腳本延伸的虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="c9360-121">Specifies the name of a virtual machine from which this cmdlet removes the custom script extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9360-122">-確認</span><span class="sxs-lookup"><span data-stu-id="c9360-122">-Confirm</span></span>
<span data-ttu-id="c9360-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c9360-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9360-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9360-124">-WhatIf</span></span>
<span data-ttu-id="c9360-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c9360-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9360-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c9360-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9360-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9360-127">CommonParameters</span></span>
<span data-ttu-id="c9360-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c9360-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9360-129">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c9360-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9360-130">輸入</span><span class="sxs-lookup"><span data-stu-id="c9360-130">INPUTS</span></span>

### <span data-ttu-id="c9360-131">System.object</span><span class="sxs-lookup"><span data-stu-id="c9360-131">System.String</span></span>

## <span data-ttu-id="c9360-132">輸出</span><span class="sxs-lookup"><span data-stu-id="c9360-132">OUTPUTS</span></span>

### <span data-ttu-id="c9360-133">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="c9360-133">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="c9360-134">筆記</span><span class="sxs-lookup"><span data-stu-id="c9360-134">NOTES</span></span>

## <span data-ttu-id="c9360-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="c9360-135">RELATED LINKS</span></span>

[<span data-ttu-id="c9360-136">AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="c9360-136">Get-AzVMCustomScriptExtension</span></span>](./Get-AzVMCustomScriptExtension.md)

[<span data-ttu-id="c9360-137">Set-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="c9360-137">Set-AzVMCustomScriptExtension</span></span>](./Set-AzVMCustomScriptExtension.md)
