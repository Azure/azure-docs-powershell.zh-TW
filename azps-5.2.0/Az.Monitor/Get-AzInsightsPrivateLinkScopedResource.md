---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: f3d00ba82bbafce42cca49c60d443cd244f83df3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98283619"
---
# <span data-ttu-id="cab8c-101">Get-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="cab8c-101">Get-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="cab8c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cab8c-102">SYNOPSIS</span></span>
<span data-ttu-id="cab8c-103">取得私人連結範圍資源</span><span class="sxs-lookup"><span data-stu-id="cab8c-103">Get for private link scoped resource</span></span>

## <span data-ttu-id="cab8c-104">句法</span><span class="sxs-lookup"><span data-stu-id="cab8c-104">SYNTAX</span></span>

### <span data-ttu-id="cab8c-105">ByScopeParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="cab8c-105">ByScopeParameterSet (Default)</span></span>
```
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName <String> -ScopeName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cab8c-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cab8c-106">ByInputObjectParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScopedResource [-Name <String>] -InputObject <PSMonitorPrivateLinkScope>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cab8c-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cab8c-107">ByResourceIdParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScopedResource -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cab8c-108">說明</span><span class="sxs-lookup"><span data-stu-id="cab8c-108">DESCRIPTION</span></span>
<span data-ttu-id="cab8c-109">[取得] 或 [清單] 專用連結範圍的資源，範圍資源可以是 Log Analytics 工作區或 Application Insights 元件</span><span class="sxs-lookup"><span data-stu-id="cab8c-109">Get or list for private link scoped resource, scoped resource could be Log Analytics workspace or Application Insights component</span></span>

## <span data-ttu-id="cab8c-110">示例</span><span class="sxs-lookup"><span data-stu-id="cab8c-110">EXAMPLES</span></span>

### <span data-ttu-id="cab8c-111">範例1</span><span class="sxs-lookup"><span data-stu-id="cab8c-111">Example 1</span></span>
```powershell
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name"
```

<span data-ttu-id="cab8c-112">[私人連結範圍] 下的 [清單範圍的資源] [scope_name "</span><span class="sxs-lookup"><span data-stu-id="cab8c-112">List scoped resource under private link scope "scope_name"</span></span>

### <span data-ttu-id="cab8c-113">範例2</span><span class="sxs-lookup"><span data-stu-id="cab8c-113">Example 2</span></span>
```powershell
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="cab8c-114">在 [私人連結範圍] 下取得名稱為 "scoped_resource_name" 的 [scope_name]，取得作用中的資源</span><span class="sxs-lookup"><span data-stu-id="cab8c-114">Get scoped resource under private link scope "scope_name" with name "scoped_resource_name"</span></span>

## <span data-ttu-id="cab8c-115">參數</span><span class="sxs-lookup"><span data-stu-id="cab8c-115">PARAMETERS</span></span>

### <span data-ttu-id="cab8c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cab8c-116">-DefaultProfile</span></span>
<span data-ttu-id="cab8c-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cab8c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cab8c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cab8c-118">-InputObject</span></span>
<span data-ttu-id="cab8c-119">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="cab8c-119">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="cab8c-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="cab8c-120">-Name</span></span>
<span data-ttu-id="cab8c-121">範圍的資源名稱</span><span class="sxs-lookup"><span data-stu-id="cab8c-121">Scoped resource Name</span></span>

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

### <span data-ttu-id="cab8c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cab8c-122">-ResourceGroupName</span></span>
<span data-ttu-id="cab8c-123">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="cab8c-123">Resource Group Name</span></span>

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

### <span data-ttu-id="cab8c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cab8c-124">-ResourceId</span></span>
<span data-ttu-id="cab8c-125">資源識別碼</span><span class="sxs-lookup"><span data-stu-id="cab8c-125">Resource Id</span></span>

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

### <span data-ttu-id="cab8c-126">-ScopeName</span><span class="sxs-lookup"><span data-stu-id="cab8c-126">-ScopeName</span></span>
<span data-ttu-id="cab8c-127">私人連結範圍名稱</span><span class="sxs-lookup"><span data-stu-id="cab8c-127">Private Link Scope Name</span></span>

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

### <span data-ttu-id="cab8c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cab8c-128">CommonParameters</span></span>
<span data-ttu-id="cab8c-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cab8c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cab8c-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="cab8c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cab8c-131">輸入</span><span class="sxs-lookup"><span data-stu-id="cab8c-131">INPUTS</span></span>

### <span data-ttu-id="cab8c-132">System.object</span><span class="sxs-lookup"><span data-stu-id="cab8c-132">System.String</span></span>

## <span data-ttu-id="cab8c-133">輸出</span><span class="sxs-lookup"><span data-stu-id="cab8c-133">OUTPUTS</span></span>

### <span data-ttu-id="cab8c-134">PSMonitorPrivateLinkScopedResource icrosoft. OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="cab8c-134">icrosoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span></span>

## <span data-ttu-id="cab8c-135">筆記</span><span class="sxs-lookup"><span data-stu-id="cab8c-135">NOTES</span></span>

## <span data-ttu-id="cab8c-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="cab8c-136">RELATED LINKS</span></span>
