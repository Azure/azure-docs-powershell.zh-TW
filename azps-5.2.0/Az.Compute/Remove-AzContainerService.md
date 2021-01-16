---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 8180092D-5B1D-43A0-B830-D009B30E2DDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzContainerService.md
ms.openlocfilehash: 8e029309099b3f28c1a9f0108bf4e6f4a78cb45d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98274215"
---
# <span data-ttu-id="3b5f0-101">Remove-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="3b5f0-101">Remove-AzContainerService</span></span>

## <span data-ttu-id="3b5f0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3b5f0-102">SYNOPSIS</span></span>
<span data-ttu-id="3b5f0-103">移除容器服務。</span><span class="sxs-lookup"><span data-stu-id="3b5f0-103">Removes a container service.</span></span>

## <span data-ttu-id="3b5f0-104">句法</span><span class="sxs-lookup"><span data-stu-id="3b5f0-104">SYNTAX</span></span>

```
Remove-AzContainerService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b5f0-105">說明</span><span class="sxs-lookup"><span data-stu-id="3b5f0-105">DESCRIPTION</span></span>
<span data-ttu-id="3b5f0-106">**AzContainerService** Cmdlet 會從您的 Azure 帳戶中移除容器服務。</span><span class="sxs-lookup"><span data-stu-id="3b5f0-106">The **Remove-AzContainerService** cmdlet removes a container service from your Azure account.</span></span>

## <span data-ttu-id="3b5f0-107">示例</span><span class="sxs-lookup"><span data-stu-id="3b5f0-107">EXAMPLES</span></span>

### <span data-ttu-id="3b5f0-108">範例1：移除容器服務</span><span class="sxs-lookup"><span data-stu-id="3b5f0-108">Example 1: Remove a container service</span></span>
```
PS C:\> Remove-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="3b5f0-109">這個命令會移除名為 CSResourceGroup17 的容器服務。</span><span class="sxs-lookup"><span data-stu-id="3b5f0-109">This command removes the container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="3b5f0-110">參數</span><span class="sxs-lookup"><span data-stu-id="3b5f0-110">PARAMETERS</span></span>

### <span data-ttu-id="3b5f0-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3b5f0-111">-AsJob</span></span>
<span data-ttu-id="3b5f0-112">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="3b5f0-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="3b5f0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b5f0-113">-DefaultProfile</span></span>
<span data-ttu-id="3b5f0-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3b5f0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b5f0-115">-Force</span><span class="sxs-lookup"><span data-stu-id="3b5f0-115">-Force</span></span>
<span data-ttu-id="3b5f0-116">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="3b5f0-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3b5f0-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="3b5f0-117">-Name</span></span>
<span data-ttu-id="3b5f0-118">指定此 Cmdlet 移除的容器服務名稱。</span><span class="sxs-lookup"><span data-stu-id="3b5f0-118">Specifies the name of the container service that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3b5f0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b5f0-119">-ResourceGroupName</span></span>
<span data-ttu-id="3b5f0-120">指定此 Cmdlet 移除之容器服務的 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="3b5f0-120">Specifies the resource group of the container service that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3b5f0-121">-確認</span><span class="sxs-lookup"><span data-stu-id="3b5f0-121">-Confirm</span></span>
<span data-ttu-id="3b5f0-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3b5f0-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b5f0-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b5f0-123">-WhatIf</span></span>
<span data-ttu-id="3b5f0-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3b5f0-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3b5f0-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3b5f0-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b5f0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b5f0-126">CommonParameters</span></span>
<span data-ttu-id="3b5f0-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3b5f0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b5f0-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3b5f0-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b5f0-129">輸入</span><span class="sxs-lookup"><span data-stu-id="3b5f0-129">INPUTS</span></span>

### <span data-ttu-id="3b5f0-130">System.object</span><span class="sxs-lookup"><span data-stu-id="3b5f0-130">System.String</span></span>

## <span data-ttu-id="3b5f0-131">輸出</span><span class="sxs-lookup"><span data-stu-id="3b5f0-131">OUTPUTS</span></span>

### <span data-ttu-id="3b5f0-132">PSOperationStatusResponse 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="3b5f0-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="3b5f0-133">筆記</span><span class="sxs-lookup"><span data-stu-id="3b5f0-133">NOTES</span></span>

## <span data-ttu-id="3b5f0-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="3b5f0-134">RELATED LINKS</span></span>

[<span data-ttu-id="3b5f0-135">AzContainerService</span><span class="sxs-lookup"><span data-stu-id="3b5f0-135">Get-AzContainerService</span></span>](./Get-AzContainerService.md)

[<span data-ttu-id="3b5f0-136">新-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="3b5f0-136">New-AzContainerService</span></span>](./New-AzContainerService.md)

[<span data-ttu-id="3b5f0-137">更新-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="3b5f0-137">Update-AzContainerService</span></span>](./Update-AzContainerService.md)


