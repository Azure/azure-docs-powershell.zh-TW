---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 3992E6B5-F794-4C7A-BB59-C8D60E2CD7BC
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/set-azoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsDataSource.md
ms.openlocfilehash: 4156bc414105d6d104e8315d83f92f0fb6e19ab3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911550"
---
# <span data-ttu-id="9715a-101">Set-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="9715a-101">Set-AzOperationalInsightsDataSource</span></span>

## <span data-ttu-id="9715a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9715a-102">SYNOPSIS</span></span>
<span data-ttu-id="9715a-103">更新資料來源。</span><span class="sxs-lookup"><span data-stu-id="9715a-103">Updates a data source.</span></span>

## <span data-ttu-id="9715a-104">語法</span><span class="sxs-lookup"><span data-stu-id="9715a-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsDataSource [-DataSource] <PSDataSource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9715a-105">描述</span><span class="sxs-lookup"><span data-stu-id="9715a-105">DESCRIPTION</span></span>
<span data-ttu-id="9715a-106">**Set-AzOperationalInsightsDataSource** Cmdlet 會更新資料來源。</span><span class="sxs-lookup"><span data-stu-id="9715a-106">The **Set-AzOperationalInsightsDataSource** cmdlet updates a data source.</span></span>

## <span data-ttu-id="9715a-107">例子</span><span class="sxs-lookup"><span data-stu-id="9715a-107">EXAMPLES</span></span>

## <span data-ttu-id="9715a-108">參數</span><span class="sxs-lookup"><span data-stu-id="9715a-108">PARAMETERS</span></span>

### <span data-ttu-id="9715a-109">-DataSource</span><span class="sxs-lookup"><span data-stu-id="9715a-109">-DataSource</span></span>
<span data-ttu-id="9715a-110">指定此 Cmdlet 更新的資料來源。</span><span class="sxs-lookup"><span data-stu-id="9715a-110">Specifies the data source that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9715a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9715a-111">-DefaultProfile</span></span>
<span data-ttu-id="9715a-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="9715a-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9715a-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9715a-113">CommonParameters</span></span>
<span data-ttu-id="9715a-114">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9715a-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9715a-115">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="9715a-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9715a-116">輸入</span><span class="sxs-lookup"><span data-stu-id="9715a-116">INPUTS</span></span>

### <span data-ttu-id="9715a-117">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="9715a-117">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="9715a-118">輸出</span><span class="sxs-lookup"><span data-stu-id="9715a-118">OUTPUTS</span></span>

### <span data-ttu-id="9715a-119">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="9715a-119">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="9715a-120">筆記</span><span class="sxs-lookup"><span data-stu-id="9715a-120">NOTES</span></span>
* <span data-ttu-id="9715a-121">關鍵字：azure、azurerm、arm、資源、管理、主管、營運、深入資訊</span><span class="sxs-lookup"><span data-stu-id="9715a-121">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="9715a-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="9715a-122">RELATED LINKS</span></span>

[<span data-ttu-id="9715a-123">Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="9715a-123">Get-AzOperationalInsightsDataSource</span></span>](./Get-AzOperationalInsightsDataSource.md)

[<span data-ttu-id="9715a-124">Remove-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="9715a-124">Remove-AzOperationalInsightsDataSource</span></span>](./Remove-AzOperationalInsightsDataSource.md)


