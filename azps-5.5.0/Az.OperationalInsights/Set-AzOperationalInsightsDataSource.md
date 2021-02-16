---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 3992E6B5-F794-4C7A-BB59-C8D60E2CD7BC
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsDataSource.md
ms.openlocfilehash: ef90211ccca53a94db2651f17b3a666a725ce8b1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100131043"
---
# <span data-ttu-id="5bf96-101">Set-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="5bf96-101">Set-AzOperationalInsightsDataSource</span></span>

## <span data-ttu-id="5bf96-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5bf96-102">SYNOPSIS</span></span>
<span data-ttu-id="5bf96-103">更新資料來源。</span><span class="sxs-lookup"><span data-stu-id="5bf96-103">Updates a data source.</span></span>

## <span data-ttu-id="5bf96-104">句法</span><span class="sxs-lookup"><span data-stu-id="5bf96-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsDataSource [-DataSource] <PSDataSource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5bf96-105">說明</span><span class="sxs-lookup"><span data-stu-id="5bf96-105">DESCRIPTION</span></span>
<span data-ttu-id="5bf96-106">**AzOperationalInsightsDataSource** Cmdlet 會更新資料來源。</span><span class="sxs-lookup"><span data-stu-id="5bf96-106">The **Set-AzOperationalInsightsDataSource** cmdlet updates a data source.</span></span>

## <span data-ttu-id="5bf96-107">示例</span><span class="sxs-lookup"><span data-stu-id="5bf96-107">EXAMPLES</span></span>

## <span data-ttu-id="5bf96-108">參數</span><span class="sxs-lookup"><span data-stu-id="5bf96-108">PARAMETERS</span></span>

### <span data-ttu-id="5bf96-109">-DataSource</span><span class="sxs-lookup"><span data-stu-id="5bf96-109">-DataSource</span></span>
<span data-ttu-id="5bf96-110">指定此 Cmdlet 更新的資料來源。</span><span class="sxs-lookup"><span data-stu-id="5bf96-110">Specifies the data source that this cmdlet updates.</span></span>

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

### <span data-ttu-id="5bf96-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bf96-111">-DefaultProfile</span></span>
<span data-ttu-id="5bf96-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="5bf96-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5bf96-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bf96-113">CommonParameters</span></span>
<span data-ttu-id="5bf96-114">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5bf96-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bf96-115">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5bf96-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bf96-116">輸入</span><span class="sxs-lookup"><span data-stu-id="5bf96-116">INPUTS</span></span>

### <span data-ttu-id="5bf96-117">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="5bf96-117">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="5bf96-118">輸出</span><span class="sxs-lookup"><span data-stu-id="5bf96-118">OUTPUTS</span></span>

### <span data-ttu-id="5bf96-119">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="5bf96-119">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="5bf96-120">筆記</span><span class="sxs-lookup"><span data-stu-id="5bf96-120">NOTES</span></span>
* <span data-ttu-id="5bf96-121">關鍵字： azure，azurerm，arm，資源，管理，管理員，作業，洞察力</span><span class="sxs-lookup"><span data-stu-id="5bf96-121">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="5bf96-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="5bf96-122">RELATED LINKS</span></span>

[<span data-ttu-id="5bf96-123">AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="5bf96-123">Get-AzOperationalInsightsDataSource</span></span>](./Get-AzOperationalInsightsDataSource.md)

[<span data-ttu-id="5bf96-124">移除-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="5bf96-124">Remove-AzOperationalInsightsDataSource</span></span>](./Remove-AzOperationalInsightsDataSource.md)


