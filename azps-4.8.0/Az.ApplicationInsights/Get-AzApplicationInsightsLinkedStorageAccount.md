---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/get-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: 7e879cd4e513ebdad297933269e373c625f2e407
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969423"
---
# <span data-ttu-id="218ab-101">Get-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="218ab-101">Get-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="218ab-102">摘要</span><span class="sxs-lookup"><span data-stu-id="218ab-102">SYNOPSIS</span></span>
<span data-ttu-id="218ab-103">取得 application insights 連結儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="218ab-103">Get application insights linked storage account</span></span>

## <span data-ttu-id="218ab-104">句法</span><span class="sxs-lookup"><span data-stu-id="218ab-104">SYNTAX</span></span>

### <span data-ttu-id="218ab-105">ByResourceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="218ab-105">ByResourceNameParameterSet (Default)</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="218ab-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="218ab-106">ByInputObjectParameterSet</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="218ab-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="218ab-107">ByResourceIdParameterSet</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="218ab-108">說明</span><span class="sxs-lookup"><span data-stu-id="218ab-108">DESCRIPTION</span></span>
<span data-ttu-id="218ab-109">取得 application insights 連結儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="218ab-109">Get application insights linked storage account</span></span>

## <span data-ttu-id="218ab-110">示例</span><span class="sxs-lookup"><span data-stu-id="218ab-110">EXAMPLES</span></span>

### <span data-ttu-id="218ab-111">範例1</span><span class="sxs-lookup"><span data-stu-id="218ab-111">Example 1</span></span>
```powershell
Get-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName "rgName" -Name "componentName"
```

<span data-ttu-id="218ab-112">取得與元件 "componentName" 相關聯的連結儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="218ab-112">Get linked storage account associated with component "componentName"</span></span>

## <span data-ttu-id="218ab-113">參數</span><span class="sxs-lookup"><span data-stu-id="218ab-113">PARAMETERS</span></span>

### <span data-ttu-id="218ab-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="218ab-114">-ComponentName</span></span>
<span data-ttu-id="218ab-115">元件名稱</span><span class="sxs-lookup"><span data-stu-id="218ab-115">Component Name</span></span>

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

### <span data-ttu-id="218ab-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="218ab-116">-DefaultProfile</span></span>
<span data-ttu-id="218ab-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="218ab-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="218ab-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="218ab-118">-InputObject</span></span>
<span data-ttu-id="218ab-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="218ab-119">PSApplicationInsightsComponent</span></span>

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

### <span data-ttu-id="218ab-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="218ab-120">-ResourceGroupName</span></span>
<span data-ttu-id="218ab-121">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="218ab-121">Resource Group Name</span></span>

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

### <span data-ttu-id="218ab-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="218ab-122">-ResourceId</span></span>
<span data-ttu-id="218ab-123">元件 ResourceId</span><span class="sxs-lookup"><span data-stu-id="218ab-123">Component ResourceId</span></span>

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

### <span data-ttu-id="218ab-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="218ab-124">CommonParameters</span></span>
<span data-ttu-id="218ab-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="218ab-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="218ab-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="218ab-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="218ab-127">輸入</span><span class="sxs-lookup"><span data-stu-id="218ab-127">INPUTS</span></span>

### <span data-ttu-id="218ab-128">System.object</span><span class="sxs-lookup"><span data-stu-id="218ab-128">System.String</span></span>

### <span data-ttu-id="218ab-129">PSApplicationInsightsComponent 中的 ApplicationInsights。</span><span class="sxs-lookup"><span data-stu-id="218ab-129">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="218ab-130">輸出</span><span class="sxs-lookup"><span data-stu-id="218ab-130">OUTPUTS</span></span>

### <span data-ttu-id="218ab-131">PSComponentLinkedStorageAccounts 中的 ApplicationInsights。</span><span class="sxs-lookup"><span data-stu-id="218ab-131">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span></span>

## <span data-ttu-id="218ab-132">筆記</span><span class="sxs-lookup"><span data-stu-id="218ab-132">NOTES</span></span>

## <span data-ttu-id="218ab-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="218ab-133">RELATED LINKS</span></span>