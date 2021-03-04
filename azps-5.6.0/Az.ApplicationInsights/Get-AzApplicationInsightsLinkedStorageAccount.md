---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/get-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: a059209e993f17ffb5eed1b29d1854f8387f3d8c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905230"
---
# <span data-ttu-id="94bdf-101">Get-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="94bdf-101">Get-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="94bdf-102">簡介</span><span class="sxs-lookup"><span data-stu-id="94bdf-102">SYNOPSIS</span></span>
<span data-ttu-id="94bdf-103">取得應用程式深入資訊連結的儲存帳戶</span><span class="sxs-lookup"><span data-stu-id="94bdf-103">Get application insights linked storage account</span></span>

## <span data-ttu-id="94bdf-104">語法</span><span class="sxs-lookup"><span data-stu-id="94bdf-104">SYNTAX</span></span>

### <span data-ttu-id="94bdf-105">ByResourceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="94bdf-105">ByResourceNameParameterSet (Default)</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94bdf-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="94bdf-106">ByInputObjectParameterSet</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94bdf-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="94bdf-107">ByResourceIdParameterSet</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="94bdf-108">描述</span><span class="sxs-lookup"><span data-stu-id="94bdf-108">DESCRIPTION</span></span>
<span data-ttu-id="94bdf-109">取得應用程式深入資訊連結的儲存帳戶</span><span class="sxs-lookup"><span data-stu-id="94bdf-109">Get application insights linked storage account</span></span>

## <span data-ttu-id="94bdf-110">例子</span><span class="sxs-lookup"><span data-stu-id="94bdf-110">EXAMPLES</span></span>

### <span data-ttu-id="94bdf-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="94bdf-111">Example 1</span></span>
```powershell
Get-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName "rgName" -Name "componentName"
```

<span data-ttu-id="94bdf-112">取得與元件 "componentName" 相關聯的連結儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="94bdf-112">Get linked storage account associated with component "componentName"</span></span>

## <span data-ttu-id="94bdf-113">參數</span><span class="sxs-lookup"><span data-stu-id="94bdf-113">PARAMETERS</span></span>

### <span data-ttu-id="94bdf-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="94bdf-114">-ComponentName</span></span>
<span data-ttu-id="94bdf-115">元件名稱</span><span class="sxs-lookup"><span data-stu-id="94bdf-115">Component Name</span></span>

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

### <span data-ttu-id="94bdf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94bdf-116">-DefaultProfile</span></span>
<span data-ttu-id="94bdf-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="94bdf-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94bdf-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="94bdf-118">-InputObject</span></span>
<span data-ttu-id="94bdf-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="94bdf-119">PSApplicationInsightsComponent</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="94bdf-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94bdf-120">-ResourceGroupName</span></span>
<span data-ttu-id="94bdf-121">資源組名</span><span class="sxs-lookup"><span data-stu-id="94bdf-121">Resource Group Name</span></span>

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

### <span data-ttu-id="94bdf-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="94bdf-122">-ResourceId</span></span>
<span data-ttu-id="94bdf-123">元件 ResourceId</span><span class="sxs-lookup"><span data-stu-id="94bdf-123">Component ResourceId</span></span>

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

### <span data-ttu-id="94bdf-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94bdf-124">CommonParameters</span></span>
<span data-ttu-id="94bdf-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="94bdf-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94bdf-126">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="94bdf-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94bdf-127">輸入</span><span class="sxs-lookup"><span data-stu-id="94bdf-127">INPUTS</span></span>

### <span data-ttu-id="94bdf-128">System.String</span><span class="sxs-lookup"><span data-stu-id="94bdf-128">System.String</span></span>

### <span data-ttu-id="94bdf-129">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="94bdf-129">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="94bdf-130">輸出</span><span class="sxs-lookup"><span data-stu-id="94bdf-130">OUTPUTS</span></span>

### <span data-ttu-id="94bdf-131">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="94bdf-131">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span></span>

## <span data-ttu-id="94bdf-132">筆記</span><span class="sxs-lookup"><span data-stu-id="94bdf-132">NOTES</span></span>

## <span data-ttu-id="94bdf-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="94bdf-133">RELATED LINKS</span></span>
