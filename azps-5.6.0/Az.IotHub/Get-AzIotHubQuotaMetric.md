---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubquotametric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubQuotaMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubQuotaMetric.md
ms.openlocfilehash: 70e63723bd9647f003082813cd680a84ae5638c5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911029"
---
# <span data-ttu-id="b977d-101">Get-AzIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="b977d-101">Get-AzIotHubQuotaMetric</span></span>

## <span data-ttu-id="b977d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b977d-102">SYNOPSIS</span></span>
<span data-ttu-id="b977d-103">獲得 IotHub 的配額度量。</span><span class="sxs-lookup"><span data-stu-id="b977d-103">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="b977d-104">語法</span><span class="sxs-lookup"><span data-stu-id="b977d-104">SYNTAX</span></span>

```
Get-AzIotHubQuotaMetric [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b977d-105">描述</span><span class="sxs-lookup"><span data-stu-id="b977d-105">DESCRIPTION</span></span>
<span data-ttu-id="b977d-106">獲得 IotHub 的配額度量。</span><span class="sxs-lookup"><span data-stu-id="b977d-106">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="b977d-107">例子</span><span class="sxs-lookup"><span data-stu-id="b977d-107">EXAMPLES</span></span>

### <span data-ttu-id="b977d-108">範例 1 取得配額計量</span><span class="sxs-lookup"><span data-stu-id="b977d-108">Example 1 Get the Quota Metrics</span></span>
```
PS C:\> Get-AzIotHubQuotaMetric -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="b977d-109">獲得名為 "myiothub" 的 IotHub 的配額計量資訊</span><span class="sxs-lookup"><span data-stu-id="b977d-109">Gets the Quota Metric information for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="b977d-110">參數</span><span class="sxs-lookup"><span data-stu-id="b977d-110">PARAMETERS</span></span>

### <span data-ttu-id="b977d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b977d-111">-DefaultProfile</span></span>
<span data-ttu-id="b977d-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="b977d-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b977d-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="b977d-113">-Name</span></span>
<span data-ttu-id="b977d-114">IoT 中樞的名稱。</span><span class="sxs-lookup"><span data-stu-id="b977d-114">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="b977d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b977d-115">-ResourceGroupName</span></span>
<span data-ttu-id="b977d-116">資源組名</span><span class="sxs-lookup"><span data-stu-id="b977d-116">Resource Group Name</span></span>

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

### <span data-ttu-id="b977d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b977d-117">CommonParameters</span></span>
<span data-ttu-id="b977d-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b977d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b977d-119">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="b977d-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b977d-120">輸入</span><span class="sxs-lookup"><span data-stu-id="b977d-120">INPUTS</span></span>

### <span data-ttu-id="b977d-121">System.String</span><span class="sxs-lookup"><span data-stu-id="b977d-121">System.String</span></span>

## <span data-ttu-id="b977d-122">輸出</span><span class="sxs-lookup"><span data-stu-id="b977d-122">OUTPUTS</span></span>

### <span data-ttu-id="b977d-123">Microsoft.Azure.Commands.management.IotHub.models.PSIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="b977d-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubQuotaMetric</span></span>

## <span data-ttu-id="b977d-124">筆記</span><span class="sxs-lookup"><span data-stu-id="b977d-124">NOTES</span></span>

## <span data-ttu-id="b977d-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="b977d-125">RELATED LINKS</span></span>
