---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azspublicipaddress
schema: 2.0.0
ms.openlocfilehash: d63133d082af8a9938b2e39318d05ec4ba0d0eb3
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968413"
---
# <span data-ttu-id="decaa-101">Get-AzsPublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="decaa-101">Get-AzsPublicIPAddress</span></span>

## <span data-ttu-id="decaa-102">摘要</span><span class="sxs-lookup"><span data-stu-id="decaa-102">SYNOPSIS</span></span>
<span data-ttu-id="decaa-103">公用 ip 地址清單。</span><span class="sxs-lookup"><span data-stu-id="decaa-103">List of public ip addresses.</span></span>

## <span data-ttu-id="decaa-104">句法</span><span class="sxs-lookup"><span data-stu-id="decaa-104">SYNTAX</span></span>

```
Get-AzsPublicIPAddress [-SubscriptionId <String[]>] [-Filter <String>] [-InlineCount <String>]
 [-OrderBy <String>] [-Skip <String>] [-Top <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="decaa-105">說明</span><span class="sxs-lookup"><span data-stu-id="decaa-105">DESCRIPTION</span></span>
<span data-ttu-id="decaa-106">公用 ip 地址清單。</span><span class="sxs-lookup"><span data-stu-id="decaa-106">List of public ip addresses.</span></span>

## <span data-ttu-id="decaa-107">示例</span><span class="sxs-lookup"><span data-stu-id="decaa-107">EXAMPLES</span></span>

### <span data-ttu-id="decaa-108">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="decaa-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```powershell
Get-AzsPublicIPAddress
To view examples, please use the -Online parameter with Get-Help or navigate to: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azspublicipaddress
```

<span data-ttu-id="decaa-109">取得公用 ip 位址的清單（已指派或未分派）。</span><span class="sxs-lookup"><span data-stu-id="decaa-109">Get the list of public ip addresses, either allocated or not allocated.</span></span>

## <span data-ttu-id="decaa-110">參數</span><span class="sxs-lookup"><span data-stu-id="decaa-110">PARAMETERS</span></span>

### <span data-ttu-id="decaa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="decaa-111">-DefaultProfile</span></span>
<span data-ttu-id="decaa-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="decaa-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="decaa-113">-篩選</span><span class="sxs-lookup"><span data-stu-id="decaa-113">-Filter</span></span>
<span data-ttu-id="decaa-114">OData 篩選參數。</span><span class="sxs-lookup"><span data-stu-id="decaa-114">OData filter parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="decaa-115">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="decaa-115">-InlineCount</span></span>
<span data-ttu-id="decaa-116">OData 內嵌計數參數。</span><span class="sxs-lookup"><span data-stu-id="decaa-116">OData inline count parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="decaa-117">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="decaa-117">-OrderBy</span></span>
<span data-ttu-id="decaa-118">OData orderBy 參數。</span><span class="sxs-lookup"><span data-stu-id="decaa-118">OData orderBy parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="decaa-119">-略過</span><span class="sxs-lookup"><span data-stu-id="decaa-119">-Skip</span></span>
<span data-ttu-id="decaa-120">OData 略過參數。</span><span class="sxs-lookup"><span data-stu-id="decaa-120">OData skip parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="decaa-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="decaa-121">-SubscriptionId</span></span>
<span data-ttu-id="decaa-122">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="decaa-122">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="decaa-123">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="decaa-123">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="decaa-124">-上方</span><span class="sxs-lookup"><span data-stu-id="decaa-124">-Top</span></span>
<span data-ttu-id="decaa-125">OData top 參數。</span><span class="sxs-lookup"><span data-stu-id="decaa-125">OData top parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="decaa-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="decaa-126">CommonParameters</span></span>
<span data-ttu-id="decaa-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="decaa-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="decaa-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="decaa-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="decaa-129">輸入</span><span class="sxs-lookup"><span data-stu-id="decaa-129">INPUTS</span></span>

## <span data-ttu-id="decaa-130">輸出</span><span class="sxs-lookup"><span data-stu-id="decaa-130">OUTPUTS</span></span>

### <span data-ttu-id="decaa-131">IPublicIPAddress （NetworkAdmin）。 Api20150615。</span><span class="sxs-lookup"><span data-stu-id="decaa-131">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IPublicIPAddress</span></span>



## <span data-ttu-id="decaa-132">筆記</span><span class="sxs-lookup"><span data-stu-id="decaa-132">NOTES</span></span>

## <span data-ttu-id="decaa-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="decaa-133">RELATED LINKS</span></span>

