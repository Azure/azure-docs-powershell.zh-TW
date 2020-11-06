---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 8180092D-5B1D-43A0-B830-D009B30E2DDF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmContainerService.md
ms.openlocfilehash: 19c94fae0192766b87f430e6137fe8d3652325c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447420"
---
# <span data-ttu-id="b879d-101">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="b879d-101">Remove-AzureRmContainerService</span></span>

## <span data-ttu-id="b879d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b879d-102">SYNOPSIS</span></span>
<span data-ttu-id="b879d-103">移除容器服務。</span><span class="sxs-lookup"><span data-stu-id="b879d-103">Removes a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b879d-104">句法</span><span class="sxs-lookup"><span data-stu-id="b879d-104">SYNTAX</span></span>

```
Remove-AzureRmContainerService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b879d-105">說明</span><span class="sxs-lookup"><span data-stu-id="b879d-105">DESCRIPTION</span></span>
<span data-ttu-id="b879d-106">**AzureRmContainerService** Cmdlet 會從您的 Azure 帳戶中移除容器服務。</span><span class="sxs-lookup"><span data-stu-id="b879d-106">The **Remove-AzureRmContainerService** cmdlet removes a container service from your Azure account.</span></span>

## <span data-ttu-id="b879d-107">示例</span><span class="sxs-lookup"><span data-stu-id="b879d-107">EXAMPLES</span></span>

### <span data-ttu-id="b879d-108">範例1：移除容器服務</span><span class="sxs-lookup"><span data-stu-id="b879d-108">Example 1: Remove a container service</span></span>
```
PS C:\> Remove-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="b879d-109">這個命令會移除名為 CSResourceGroup17 的容器服務。</span><span class="sxs-lookup"><span data-stu-id="b879d-109">This command removes the container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="b879d-110">參數</span><span class="sxs-lookup"><span data-stu-id="b879d-110">PARAMETERS</span></span>

### <span data-ttu-id="b879d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b879d-111">-AsJob</span></span>
<span data-ttu-id="b879d-112">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="b879d-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="b879d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b879d-113">-DefaultProfile</span></span>
<span data-ttu-id="b879d-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b879d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b879d-115">-Force</span><span class="sxs-lookup"><span data-stu-id="b879d-115">-Force</span></span>
<span data-ttu-id="b879d-116">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="b879d-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b879d-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="b879d-117">-Name</span></span>
<span data-ttu-id="b879d-118">指定此 Cmdlet 移除的容器服務名稱。</span><span class="sxs-lookup"><span data-stu-id="b879d-118">Specifies the name of the container service that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b879d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b879d-119">-ResourceGroupName</span></span>
<span data-ttu-id="b879d-120">指定此 Cmdlet 移除之容器服務的 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="b879d-120">Specifies the resource group of the container service that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b879d-121">-確認</span><span class="sxs-lookup"><span data-stu-id="b879d-121">-Confirm</span></span>
<span data-ttu-id="b879d-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b879d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b879d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b879d-123">-WhatIf</span></span>
<span data-ttu-id="b879d-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b879d-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b879d-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b879d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b879d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b879d-126">CommonParameters</span></span>
<span data-ttu-id="b879d-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b879d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b879d-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b879d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b879d-129">輸入</span><span class="sxs-lookup"><span data-stu-id="b879d-129">INPUTS</span></span>

### <span data-ttu-id="b879d-130">System.object</span><span class="sxs-lookup"><span data-stu-id="b879d-130">System.String</span></span>

## <span data-ttu-id="b879d-131">輸出</span><span class="sxs-lookup"><span data-stu-id="b879d-131">OUTPUTS</span></span>

### <span data-ttu-id="b879d-132">System.void</span><span class="sxs-lookup"><span data-stu-id="b879d-132">System.Void</span></span>

## <span data-ttu-id="b879d-133">筆記</span><span class="sxs-lookup"><span data-stu-id="b879d-133">NOTES</span></span>

## <span data-ttu-id="b879d-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="b879d-134">RELATED LINKS</span></span>

[<span data-ttu-id="b879d-135">AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="b879d-135">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)

[<span data-ttu-id="b879d-136">新-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="b879d-136">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)

[<span data-ttu-id="b879d-137">更新-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="b879d-137">Update-AzureRmContainerService</span></span>](./Update-AzureRmContainerService.md)


