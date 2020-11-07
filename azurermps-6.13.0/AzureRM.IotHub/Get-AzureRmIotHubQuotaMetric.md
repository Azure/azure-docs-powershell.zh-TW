---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubquotametric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubQuotaMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubQuotaMetric.md
ms.openlocfilehash: 1de2d49d6e914635f8fc0d38ffa81755cc622481
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625838"
---
# <span data-ttu-id="33cf6-101">Get-AzureRmIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="33cf6-101">Get-AzureRmIotHubQuotaMetric</span></span>

## <span data-ttu-id="33cf6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="33cf6-102">SYNOPSIS</span></span>
<span data-ttu-id="33cf6-103">取得 IotHub 的配額度量單位。</span><span class="sxs-lookup"><span data-stu-id="33cf6-103">Gets the Quota Metrics for an IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33cf6-104">句法</span><span class="sxs-lookup"><span data-stu-id="33cf6-104">SYNTAX</span></span>

```
Get-AzureRmIotHubQuotaMetric [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33cf6-105">說明</span><span class="sxs-lookup"><span data-stu-id="33cf6-105">DESCRIPTION</span></span>
<span data-ttu-id="33cf6-106">取得 IotHub 的配額度量單位。</span><span class="sxs-lookup"><span data-stu-id="33cf6-106">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="33cf6-107">示例</span><span class="sxs-lookup"><span data-stu-id="33cf6-107">EXAMPLES</span></span>

### <span data-ttu-id="33cf6-108">範例1取得配額度量單位</span><span class="sxs-lookup"><span data-stu-id="33cf6-108">Example 1 Get the Quota Metrics</span></span>
```
PS C:\> Get-AzureRmIotHubQuotaMetric -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="33cf6-109">取得名為 "myiothub" 的 IotHub 的配額度量資訊</span><span class="sxs-lookup"><span data-stu-id="33cf6-109">Gets the Quota Metric information for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="33cf6-110">參數</span><span class="sxs-lookup"><span data-stu-id="33cf6-110">PARAMETERS</span></span>

### <span data-ttu-id="33cf6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33cf6-111">-DefaultProfile</span></span>
<span data-ttu-id="33cf6-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="33cf6-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="33cf6-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="33cf6-113">-Name</span></span>
<span data-ttu-id="33cf6-114">IoT 中樞的名稱。</span><span class="sxs-lookup"><span data-stu-id="33cf6-114">Name of the IoT hub.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33cf6-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33cf6-115">-ResourceGroupName</span></span>
<span data-ttu-id="33cf6-116">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="33cf6-116">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33cf6-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33cf6-117">CommonParameters</span></span>
<span data-ttu-id="33cf6-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="33cf6-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33cf6-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="33cf6-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33cf6-120">輸入</span><span class="sxs-lookup"><span data-stu-id="33cf6-120">INPUTS</span></span>

### <span data-ttu-id="33cf6-121">System.object</span><span class="sxs-lookup"><span data-stu-id="33cf6-121">System.String</span></span>

## <span data-ttu-id="33cf6-122">輸出</span><span class="sxs-lookup"><span data-stu-id="33cf6-122">OUTPUTS</span></span>

### <span data-ttu-id="33cf6-123">PSIotHubQuotaMetric （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="33cf6-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubQuotaMetric</span></span>

## <span data-ttu-id="33cf6-124">筆記</span><span class="sxs-lookup"><span data-stu-id="33cf6-124">NOTES</span></span>

## <span data-ttu-id="33cf6-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="33cf6-125">RELATED LINKS</span></span>
