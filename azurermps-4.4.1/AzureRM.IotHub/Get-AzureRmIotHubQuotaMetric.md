---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubQuotaMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubQuotaMetric.md
ms.openlocfilehash: f0a3b446c6d40ff07efc35ca51cdf7f422491f33
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453479"
---
# <span data-ttu-id="6334a-101">Get-AzureRmIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="6334a-101">Get-AzureRmIotHubQuotaMetric</span></span>

## <span data-ttu-id="6334a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6334a-102">SYNOPSIS</span></span>
<span data-ttu-id="6334a-103">取得 IotHub 的配額度量單位。</span><span class="sxs-lookup"><span data-stu-id="6334a-103">Gets the Quota Metrics for an IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6334a-104">句法</span><span class="sxs-lookup"><span data-stu-id="6334a-104">SYNTAX</span></span>

```
Get-AzureRmIotHubQuotaMetric [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6334a-105">說明</span><span class="sxs-lookup"><span data-stu-id="6334a-105">DESCRIPTION</span></span>
<span data-ttu-id="6334a-106">取得 IotHub 的配額度量單位。</span><span class="sxs-lookup"><span data-stu-id="6334a-106">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="6334a-107">示例</span><span class="sxs-lookup"><span data-stu-id="6334a-107">EXAMPLES</span></span>

### <span data-ttu-id="6334a-108">範例1取得配額度量單位</span><span class="sxs-lookup"><span data-stu-id="6334a-108">Example 1 Get the Quota Metrics</span></span>
```
PS C:\> Get-AzureRmIotHubQuotaMetric -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="6334a-109">取得名為 "myiothub" 的 IotHub 的配額度量資訊</span><span class="sxs-lookup"><span data-stu-id="6334a-109">Gets the Quota Metric information for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="6334a-110">參數</span><span class="sxs-lookup"><span data-stu-id="6334a-110">PARAMETERS</span></span>

### <span data-ttu-id="6334a-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="6334a-111">-Name</span></span>
<span data-ttu-id="6334a-112">IoT 中樞的名稱。</span><span class="sxs-lookup"><span data-stu-id="6334a-112">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="6334a-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6334a-113">-ResourceGroupName</span></span>
<span data-ttu-id="6334a-114">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="6334a-114">Resource Group Name</span></span>

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

### <span data-ttu-id="6334a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6334a-115">-DefaultProfile</span></span>
<span data-ttu-id="6334a-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6334a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6334a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6334a-117">CommonParameters</span></span>
<span data-ttu-id="6334a-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6334a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6334a-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6334a-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6334a-120">輸入</span><span class="sxs-lookup"><span data-stu-id="6334a-120">INPUTS</span></span>

### <span data-ttu-id="6334a-121">System.object</span><span class="sxs-lookup"><span data-stu-id="6334a-121">System.String</span></span>

## <span data-ttu-id="6334a-122">輸出</span><span class="sxs-lookup"><span data-stu-id="6334a-122">OUTPUTS</span></span>

### <span data-ttu-id="6334a-123">[System.object]。清單 ' 1 [IotHub. PSIotHubQuotaMetric，IotHub，版本 = 1.0.0.0，Culture = 中性，PublicKeyToken = null]]。）））））</span><span class="sxs-lookup"><span data-stu-id="6334a-123">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubQuotaMetric, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="6334a-124">筆記</span><span class="sxs-lookup"><span data-stu-id="6334a-124">NOTES</span></span>

## <span data-ttu-id="6334a-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="6334a-125">RELATED LINKS</span></span>

