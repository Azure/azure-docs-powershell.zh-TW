---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/get-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: ff4e75e2301ef9ae2ccd6f2e5064e06aedc2dbd4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908933"
---
# <span data-ttu-id="f2a08-101">Get-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="f2a08-101">Get-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="f2a08-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f2a08-102">SYNOPSIS</span></span>
<span data-ttu-id="f2a08-103">取得私人連結範圍資源</span><span class="sxs-lookup"><span data-stu-id="f2a08-103">Get for private link scoped resource</span></span>

## <span data-ttu-id="f2a08-104">語法</span><span class="sxs-lookup"><span data-stu-id="f2a08-104">SYNTAX</span></span>

### <span data-ttu-id="f2a08-105">ByScopeParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f2a08-105">ByScopeParameterSet (Default)</span></span>
```
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName <String> -ScopeName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2a08-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2a08-106">ByInputObjectParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScopedResource [-Name <String>] -InputObject <PSMonitorPrivateLinkScope>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2a08-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2a08-107">ByResourceIdParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScopedResource -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f2a08-108">描述</span><span class="sxs-lookup"><span data-stu-id="f2a08-108">DESCRIPTION</span></span>
<span data-ttu-id="f2a08-109">取得或列出私人連結範圍資源，範圍資源可能是 Log Analytics 工作區或應用程式深入解析元件</span><span class="sxs-lookup"><span data-stu-id="f2a08-109">Get or list for private link scoped resource, scoped resource could be Log Analytics workspace or Application Insights component</span></span>

## <span data-ttu-id="f2a08-110">例子</span><span class="sxs-lookup"><span data-stu-id="f2a08-110">EXAMPLES</span></span>

### <span data-ttu-id="f2a08-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="f2a08-111">Example 1</span></span>
```powershell
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name"
```

<span data-ttu-id="f2a08-112">在私人連結範圍 "scope_name" 下列出範圍資源</span><span class="sxs-lookup"><span data-stu-id="f2a08-112">List scoped resource under private link scope "scope_name"</span></span>

### <span data-ttu-id="f2a08-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="f2a08-113">Example 2</span></span>
```powershell
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="f2a08-114">在私人連結範圍 "scope_name" 下取得具有名稱 "scoped_resource_name" 的範圍資源</span><span class="sxs-lookup"><span data-stu-id="f2a08-114">Get scoped resource under private link scope "scope_name" with name "scoped_resource_name"</span></span>

## <span data-ttu-id="f2a08-115">參數</span><span class="sxs-lookup"><span data-stu-id="f2a08-115">PARAMETERS</span></span>

### <span data-ttu-id="f2a08-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2a08-116">-DefaultProfile</span></span>
<span data-ttu-id="f2a08-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f2a08-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2a08-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f2a08-118">-InputObject</span></span>
<span data-ttu-id="f2a08-119">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="f2a08-119">PSMonitorPrivateLinkScope</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2a08-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="f2a08-120">-Name</span></span>
<span data-ttu-id="f2a08-121">範圍資源名稱</span><span class="sxs-lookup"><span data-stu-id="f2a08-121">Scoped resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByScopeParameterSet, ByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2a08-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2a08-122">-ResourceGroupName</span></span>
<span data-ttu-id="f2a08-123">資源組名</span><span class="sxs-lookup"><span data-stu-id="f2a08-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByScopeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2a08-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f2a08-124">-ResourceId</span></span>
<span data-ttu-id="f2a08-125">資源識別碼</span><span class="sxs-lookup"><span data-stu-id="f2a08-125">Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2a08-126">-ScopeName</span><span class="sxs-lookup"><span data-stu-id="f2a08-126">-ScopeName</span></span>
<span data-ttu-id="f2a08-127">私人連結範圍名稱</span><span class="sxs-lookup"><span data-stu-id="f2a08-127">Private Link Scope Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByScopeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2a08-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2a08-128">CommonParameters</span></span>
<span data-ttu-id="f2a08-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f2a08-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2a08-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f2a08-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2a08-131">輸入</span><span class="sxs-lookup"><span data-stu-id="f2a08-131">INPUTS</span></span>

### <span data-ttu-id="f2a08-132">System.String</span><span class="sxs-lookup"><span data-stu-id="f2a08-132">System.String</span></span>

## <span data-ttu-id="f2a08-133">輸出</span><span class="sxs-lookup"><span data-stu-id="f2a08-133">OUTPUTS</span></span>

### <span data-ttu-id="f2a08-134">icrosoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="f2a08-134">icrosoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span></span>

## <span data-ttu-id="f2a08-135">筆記</span><span class="sxs-lookup"><span data-stu-id="f2a08-135">NOTES</span></span>

## <span data-ttu-id="f2a08-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="f2a08-136">RELATED LINKS</span></span>
