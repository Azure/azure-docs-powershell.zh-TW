---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: d5986694ad0064265bbd4bad6e1efc378683ce97
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93965533"
---
# <span data-ttu-id="0b1ab-101">Get-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="0b1ab-101">Get-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="0b1ab-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0b1ab-102">SYNOPSIS</span></span>
<span data-ttu-id="0b1ab-103">取得私人連結範圍</span><span class="sxs-lookup"><span data-stu-id="0b1ab-103">Get private link scope</span></span>

## <span data-ttu-id="0b1ab-104">句法</span><span class="sxs-lookup"><span data-stu-id="0b1ab-104">SYNTAX</span></span>

### <span data-ttu-id="0b1ab-105">ByResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="0b1ab-105">ByResourceGroupParameterSet (Default)</span></span>
```
Get-AzInsightsPrivateLinkScope [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0b1ab-106">ByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0b1ab-106">ByResourceNameParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScope -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0b1ab-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0b1ab-107">ByResourceIdParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScope -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0b1ab-108">說明</span><span class="sxs-lookup"><span data-stu-id="0b1ab-108">DESCRIPTION</span></span>
<span data-ttu-id="0b1ab-109">[清單] 或 [取得私人連結範圍]</span><span class="sxs-lookup"><span data-stu-id="0b1ab-109">List or get private link scope</span></span> 

## <span data-ttu-id="0b1ab-110">示例</span><span class="sxs-lookup"><span data-stu-id="0b1ab-110">EXAMPLES</span></span>

### <span data-ttu-id="0b1ab-111">範例1</span><span class="sxs-lookup"><span data-stu-id="0b1ab-111">Example 1</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name"
```

<span data-ttu-id="0b1ab-112">[資源群組] 的 [rg_name] 下列出私人連結範圍</span><span class="sxs-lookup"><span data-stu-id="0b1ab-112">List private link scopes under resource group "rg_name"</span></span>

### <span data-ttu-id="0b1ab-113">範例2</span><span class="sxs-lookup"><span data-stu-id="0b1ab-113">Example 2</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name"
```

<span data-ttu-id="0b1ab-114">在資源群組 "rg_name" 下取得名稱為 "scope_name" 的私人連結範圍</span><span class="sxs-lookup"><span data-stu-id="0b1ab-114">Get private link scope with name "scope_name" under resource group "rg_name"</span></span>

## <span data-ttu-id="0b1ab-115">參數</span><span class="sxs-lookup"><span data-stu-id="0b1ab-115">PARAMETERS</span></span>

### <span data-ttu-id="0b1ab-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b1ab-116">-DefaultProfile</span></span>
<span data-ttu-id="0b1ab-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0b1ab-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b1ab-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="0b1ab-118">-Name</span></span>
<span data-ttu-id="0b1ab-119">私人連結範圍名稱</span><span class="sxs-lookup"><span data-stu-id="0b1ab-119">Private Link Scope Name</span></span>

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

### <span data-ttu-id="0b1ab-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b1ab-120">-ResourceGroupName</span></span>
<span data-ttu-id="0b1ab-121">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="0b1ab-121">Resource Group Name</span></span>

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

### <span data-ttu-id="0b1ab-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0b1ab-122">-ResourceId</span></span>
<span data-ttu-id="0b1ab-123">資源識別碼</span><span class="sxs-lookup"><span data-stu-id="0b1ab-123">Resource Id</span></span>

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

### <span data-ttu-id="0b1ab-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b1ab-124">CommonParameters</span></span>
<span data-ttu-id="0b1ab-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0b1ab-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b1ab-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0b1ab-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b1ab-127">輸入</span><span class="sxs-lookup"><span data-stu-id="0b1ab-127">INPUTS</span></span>

### <span data-ttu-id="0b1ab-128">System.object</span><span class="sxs-lookup"><span data-stu-id="0b1ab-128">System.String</span></span>

## <span data-ttu-id="0b1ab-129">輸出</span><span class="sxs-lookup"><span data-stu-id="0b1ab-129">OUTPUTS</span></span>

### <span data-ttu-id="0b1ab-130">PSMonitorPrivateLinkScope 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="0b1ab-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

## <span data-ttu-id="0b1ab-131">筆記</span><span class="sxs-lookup"><span data-stu-id="0b1ab-131">NOTES</span></span>

## <span data-ttu-id="0b1ab-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="0b1ab-132">RELATED LINKS</span></span>
