---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 3992E6B5-F794-4C7A-BB59-C8D60E2CD7BC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/set-azurermoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsDataSource.md
ms.openlocfilehash: 5bf4f178ee3343b5100dad87836c3215fba4cfb4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453640"
---
# <span data-ttu-id="f6a43-101">Set-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="f6a43-101">Set-AzureRmOperationalInsightsDataSource</span></span>

## <span data-ttu-id="f6a43-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f6a43-102">SYNOPSIS</span></span>
<span data-ttu-id="f6a43-103">更新資料來源。</span><span class="sxs-lookup"><span data-stu-id="f6a43-103">Updates a data source.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6a43-104">句法</span><span class="sxs-lookup"><span data-stu-id="f6a43-104">SYNTAX</span></span>

```
Set-AzureRmOperationalInsightsDataSource [-DataSource] <PSDataSource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6a43-105">說明</span><span class="sxs-lookup"><span data-stu-id="f6a43-105">DESCRIPTION</span></span>
<span data-ttu-id="f6a43-106">**AzureRmOperationalInsightsDataSource** Cmdlet 會更新資料來源。</span><span class="sxs-lookup"><span data-stu-id="f6a43-106">The **Set-AzureRmOperationalInsightsDataSource** cmdlet updates a data source.</span></span>

## <span data-ttu-id="f6a43-107">示例</span><span class="sxs-lookup"><span data-stu-id="f6a43-107">EXAMPLES</span></span>

## <span data-ttu-id="f6a43-108">參數</span><span class="sxs-lookup"><span data-stu-id="f6a43-108">PARAMETERS</span></span>

### <span data-ttu-id="f6a43-109">-DataSource</span><span class="sxs-lookup"><span data-stu-id="f6a43-109">-DataSource</span></span>
<span data-ttu-id="f6a43-110">指定此 Cmdlet 更新的資料來源。</span><span class="sxs-lookup"><span data-stu-id="f6a43-110">Specifies the data source that this cmdlet updates.</span></span>

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

### <span data-ttu-id="f6a43-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6a43-111">-DefaultProfile</span></span>
<span data-ttu-id="f6a43-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="f6a43-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f6a43-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6a43-113">CommonParameters</span></span>
<span data-ttu-id="f6a43-114">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f6a43-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6a43-115">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f6a43-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6a43-116">輸入</span><span class="sxs-lookup"><span data-stu-id="f6a43-116">INPUTS</span></span>

### <span data-ttu-id="f6a43-117">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="f6a43-117">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>
<span data-ttu-id="f6a43-118">參數： DataSource (ByValue) </span><span class="sxs-lookup"><span data-stu-id="f6a43-118">Parameters: DataSource (ByValue)</span></span>

## <span data-ttu-id="f6a43-119">輸出</span><span class="sxs-lookup"><span data-stu-id="f6a43-119">OUTPUTS</span></span>

### <span data-ttu-id="f6a43-120">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="f6a43-120">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="f6a43-121">筆記</span><span class="sxs-lookup"><span data-stu-id="f6a43-121">NOTES</span></span>
* <span data-ttu-id="f6a43-122">關鍵字： azure，azurerm，arm，資源，管理，管理員，作業，洞察力</span><span class="sxs-lookup"><span data-stu-id="f6a43-122">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="f6a43-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="f6a43-123">RELATED LINKS</span></span>

[<span data-ttu-id="f6a43-124">AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="f6a43-124">Get-AzureRmOperationalInsightsDataSource</span></span>](./Get-AzureRmOperationalInsightsDataSource.md)

[<span data-ttu-id="f6a43-125">移除-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="f6a43-125">Remove-AzureRmOperationalInsightsDataSource</span></span>](./Remove-AzureRmOperationalInsightsDataSource.md)


