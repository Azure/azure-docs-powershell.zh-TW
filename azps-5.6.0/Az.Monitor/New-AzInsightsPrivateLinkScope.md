---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: ec9245c15a0c07da92874daa42c387e4109258c7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910057"
---
# <span data-ttu-id="63651-101">New-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="63651-101">New-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="63651-102">簡介</span><span class="sxs-lookup"><span data-stu-id="63651-102">SYNOPSIS</span></span>
<span data-ttu-id="63651-103">建立私人連結範圍</span><span class="sxs-lookup"><span data-stu-id="63651-103">create private link scope</span></span>

## <span data-ttu-id="63651-104">語法</span><span class="sxs-lookup"><span data-stu-id="63651-104">SYNTAX</span></span>

```
New-AzInsightsPrivateLinkScope -Location <String> -ResourceGroupName <String> -Name <String> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63651-105">描述</span><span class="sxs-lookup"><span data-stu-id="63651-105">DESCRIPTION</span></span>
<span data-ttu-id="63651-106">建立私人連結範圍</span><span class="sxs-lookup"><span data-stu-id="63651-106">create private link scope</span></span>

## <span data-ttu-id="63651-107">例子</span><span class="sxs-lookup"><span data-stu-id="63651-107">EXAMPLES</span></span>

### <span data-ttu-id="63651-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="63651-108">Example 1</span></span>
```powershell
New-AzInsightsPrivateLinkScope -Location "eastus" -ResourceGroupName "rg_name" -Name "scope_name"
```

<span data-ttu-id="63651-109">在位置 "eastus" scope_name資源群組 "rg_name" 下建立名稱為 "rg_name" 的私人連結範圍</span><span class="sxs-lookup"><span data-stu-id="63651-109">create private link scope with name "scope_name" under resource group "rg_name" in location "eastus"</span></span>

## <span data-ttu-id="63651-110">參數</span><span class="sxs-lookup"><span data-stu-id="63651-110">PARAMETERS</span></span>

### <span data-ttu-id="63651-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63651-111">-DefaultProfile</span></span>
<span data-ttu-id="63651-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="63651-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63651-113">-位置</span><span class="sxs-lookup"><span data-stu-id="63651-113">-Location</span></span>
<span data-ttu-id="63651-114">位置</span><span class="sxs-lookup"><span data-stu-id="63651-114">Location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63651-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="63651-115">-Name</span></span>
<span data-ttu-id="63651-116">私人連結範圍名稱</span><span class="sxs-lookup"><span data-stu-id="63651-116">Private Link Scope Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63651-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63651-117">-ResourceGroupName</span></span>
<span data-ttu-id="63651-118">資源組名</span><span class="sxs-lookup"><span data-stu-id="63651-118">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63651-119">-標記</span><span class="sxs-lookup"><span data-stu-id="63651-119">-Tags</span></span>
<span data-ttu-id="63651-120">標籤</span><span class="sxs-lookup"><span data-stu-id="63651-120">Tags</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63651-121">-確認</span><span class="sxs-lookup"><span data-stu-id="63651-121">-Confirm</span></span>
<span data-ttu-id="63651-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="63651-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63651-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63651-123">-WhatIf</span></span>
<span data-ttu-id="63651-124">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="63651-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63651-125">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="63651-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63651-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63651-126">CommonParameters</span></span>
<span data-ttu-id="63651-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="63651-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63651-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="63651-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63651-129">輸入</span><span class="sxs-lookup"><span data-stu-id="63651-129">INPUTS</span></span>

### <span data-ttu-id="63651-130">System.String</span><span class="sxs-lookup"><span data-stu-id="63651-130">System.String</span></span>

## <span data-ttu-id="63651-131">輸出</span><span class="sxs-lookup"><span data-stu-id="63651-131">OUTPUTS</span></span>

### <span data-ttu-id="63651-132">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="63651-132">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

## <span data-ttu-id="63651-133">筆記</span><span class="sxs-lookup"><span data-stu-id="63651-133">NOTES</span></span>

## <span data-ttu-id="63651-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="63651-134">RELATED LINKS</span></span>
