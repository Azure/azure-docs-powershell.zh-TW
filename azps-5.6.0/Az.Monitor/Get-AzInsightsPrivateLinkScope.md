---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/get-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: 941b60da0282bdad523b06657639a730d1776ce3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908934"
---
# <span data-ttu-id="82879-101">Get-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="82879-101">Get-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="82879-102">簡介</span><span class="sxs-lookup"><span data-stu-id="82879-102">SYNOPSIS</span></span>
<span data-ttu-id="82879-103">取得私人連結範圍</span><span class="sxs-lookup"><span data-stu-id="82879-103">Get private link scope</span></span>

## <span data-ttu-id="82879-104">語法</span><span class="sxs-lookup"><span data-stu-id="82879-104">SYNTAX</span></span>

### <span data-ttu-id="82879-105">ByResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="82879-105">ByResourceGroupParameterSet (Default)</span></span>
```
Get-AzInsightsPrivateLinkScope [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="82879-106">ByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="82879-106">ByResourceNameParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScope -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82879-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="82879-107">ByResourceIdParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScope -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="82879-108">描述</span><span class="sxs-lookup"><span data-stu-id="82879-108">DESCRIPTION</span></span>
<span data-ttu-id="82879-109">清單或取得私人連結範圍</span><span class="sxs-lookup"><span data-stu-id="82879-109">List or get private link scope</span></span> 

## <span data-ttu-id="82879-110">例子</span><span class="sxs-lookup"><span data-stu-id="82879-110">EXAMPLES</span></span>

### <span data-ttu-id="82879-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="82879-111">Example 1</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name"
```

<span data-ttu-id="82879-112">在資源群組 "rg_name" 下列出私人連結範圍</span><span class="sxs-lookup"><span data-stu-id="82879-112">List private link scopes under resource group "rg_name"</span></span>

### <span data-ttu-id="82879-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="82879-113">Example 2</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name"
```

<span data-ttu-id="82879-114">在資源群組 "scope_name" 下取得名稱為 "rg_name" 的私人連結範圍</span><span class="sxs-lookup"><span data-stu-id="82879-114">Get private link scope with name "scope_name" under resource group "rg_name"</span></span>

## <span data-ttu-id="82879-115">參數</span><span class="sxs-lookup"><span data-stu-id="82879-115">PARAMETERS</span></span>

### <span data-ttu-id="82879-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82879-116">-DefaultProfile</span></span>
<span data-ttu-id="82879-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="82879-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82879-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="82879-118">-Name</span></span>
<span data-ttu-id="82879-119">私人連結範圍名稱</span><span class="sxs-lookup"><span data-stu-id="82879-119">Private Link Scope Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82879-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82879-120">-ResourceGroupName</span></span>
<span data-ttu-id="82879-121">資源組名</span><span class="sxs-lookup"><span data-stu-id="82879-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82879-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="82879-122">-ResourceId</span></span>
<span data-ttu-id="82879-123">資源識別碼</span><span class="sxs-lookup"><span data-stu-id="82879-123">Resource Id</span></span>

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

### <span data-ttu-id="82879-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82879-124">CommonParameters</span></span>
<span data-ttu-id="82879-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="82879-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82879-126">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="82879-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82879-127">輸入</span><span class="sxs-lookup"><span data-stu-id="82879-127">INPUTS</span></span>

### <span data-ttu-id="82879-128">System.String</span><span class="sxs-lookup"><span data-stu-id="82879-128">System.String</span></span>

## <span data-ttu-id="82879-129">輸出</span><span class="sxs-lookup"><span data-stu-id="82879-129">OUTPUTS</span></span>

### <span data-ttu-id="82879-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="82879-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

## <span data-ttu-id="82879-131">筆記</span><span class="sxs-lookup"><span data-stu-id="82879-131">NOTES</span></span>

## <span data-ttu-id="82879-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="82879-132">RELATED LINKS</span></span>
