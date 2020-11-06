---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 5287D4DB-2709-4A3C-97D5-DB494CEEFD18
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 8856a2f9f1a65d6d312571d75e2400a7dcf30bc0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451568"
---
# <span data-ttu-id="522d5-101">Set-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="522d5-101">Set-AzureRmTrafficManagerEndpoint</span></span>

## <span data-ttu-id="522d5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="522d5-102">SYNOPSIS</span></span>
<span data-ttu-id="522d5-103">更新流量管理器端點。</span><span class="sxs-lookup"><span data-stu-id="522d5-103">Updates a Traffic Manager endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="522d5-104">句法</span><span class="sxs-lookup"><span data-stu-id="522d5-104">SYNTAX</span></span>

```
Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="522d5-105">說明</span><span class="sxs-lookup"><span data-stu-id="522d5-105">DESCRIPTION</span></span>
<span data-ttu-id="522d5-106">**AzureRmTrafficManagerEndpoint** Cmdlet 會更新 Azure 流量管理器中的端點。</span><span class="sxs-lookup"><span data-stu-id="522d5-106">The **Set-AzureRmTrafficManagerEndpoint** cmdlet updates an endpoint in Azure Traffic Manager.</span></span>
<span data-ttu-id="522d5-107">這個 Cmdlet 會更新本機端點物件的設定。</span><span class="sxs-lookup"><span data-stu-id="522d5-107">This cmdlet updates the settings from a local endpoint object.</span></span>
<span data-ttu-id="522d5-108">您可以使用 *TrafficManagerEndpoint* 參數或使用管線來指定端點物件。</span><span class="sxs-lookup"><span data-stu-id="522d5-108">You can specify the endpoint object either by using the *TrafficManagerEndpoint* parameter or by using the pipeline.</span></span>

<span data-ttu-id="522d5-109">您可以使用 Get-AzureRmTrafficManagerEndpoint Cmdlet 來取得代表端點的局部物件。</span><span class="sxs-lookup"><span data-stu-id="522d5-109">You can obtain a local object that represents an endpoint by using the Get-AzureRmTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="522d5-110">在本機修改物件，然後使用 [ **設定] AzureRmTrafficManagerEndpoint** 來認可您的變更。</span><span class="sxs-lookup"><span data-stu-id="522d5-110">Modify the object locally and then use **Set-AzureRmTrafficManagerEndpoint** to commit your changes.</span></span>

## <span data-ttu-id="522d5-111">示例</span><span class="sxs-lookup"><span data-stu-id="522d5-111">EXAMPLES</span></span>

### <span data-ttu-id="522d5-112">範例1：更新端點</span><span class="sxs-lookup"><span data-stu-id="522d5-112">Example 1: Update an endpoint</span></span>
```
PS C:\>$TrafficManagerEndpoint = Get-AzureRmTrafficManagerEndpoint -Name "endpoint1" -Type AzureEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> $TrafficManagerEndpoint.Weight = 20
PS C:\> Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="522d5-113">第一個命令會使用 **AzureRmTrafficManagerEndpoint** Cmdlet 來取得 Azure 流量管理器端點。</span><span class="sxs-lookup"><span data-stu-id="522d5-113">The first command gets an Azure Traffic Manager endpoint by using the **Get-AzureRmTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="522d5-114">該命令會將端點儲存在本機的 $TrafficManagerEndpoint 變數中。</span><span class="sxs-lookup"><span data-stu-id="522d5-114">The command stores the endpoint locally in the $TrafficManagerEndpoint variable.</span></span>

<span data-ttu-id="522d5-115">第二個命令會在本機變更該端點。</span><span class="sxs-lookup"><span data-stu-id="522d5-115">The second command changes that endpoint locally.</span></span>
<span data-ttu-id="522d5-116">這個命令會將端點寬度變更為20。</span><span class="sxs-lookup"><span data-stu-id="522d5-116">This command changes the endpoint weight to 20.</span></span>

<span data-ttu-id="522d5-117">第三個命令會更新流量管理器中的端點，以符合 $TrafficManagerEndpoint 中的本機值。</span><span class="sxs-lookup"><span data-stu-id="522d5-117">The third command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="522d5-118">參數</span><span class="sxs-lookup"><span data-stu-id="522d5-118">PARAMETERS</span></span>

### <span data-ttu-id="522d5-119">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="522d5-119">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="522d5-120">指定本機 **TrafficManagerEndpoint** 物件。</span><span class="sxs-lookup"><span data-stu-id="522d5-120">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="522d5-121">這個 Cmdlet 會更新流量管理器，以符合這個本機物件。</span><span class="sxs-lookup"><span data-stu-id="522d5-121">This cmdlet updates Traffic Manager to match this local object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="522d5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="522d5-122">-DefaultProfile</span></span>
<span data-ttu-id="522d5-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="522d5-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="522d5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="522d5-124">CommonParameters</span></span>
<span data-ttu-id="522d5-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="522d5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="522d5-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="522d5-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="522d5-127">輸入</span><span class="sxs-lookup"><span data-stu-id="522d5-127">INPUTS</span></span>

### <span data-ttu-id="522d5-128">TrafficManagerEndpoint （）</span><span class="sxs-lookup"><span data-stu-id="522d5-128">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="522d5-129">這個 Cmdlet 接受 **TrafficManagerEndpoint** 物件。</span><span class="sxs-lookup"><span data-stu-id="522d5-129">This cmdlet accepts a **TrafficManagerEndpoint** object.</span></span>

## <span data-ttu-id="522d5-130">輸出</span><span class="sxs-lookup"><span data-stu-id="522d5-130">OUTPUTS</span></span>

### <span data-ttu-id="522d5-131">TrafficManagerEndpoint （）</span><span class="sxs-lookup"><span data-stu-id="522d5-131">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="522d5-132">這個 Cmdlet 會傳回 **TrafficManagerEndpoint** 物件。</span><span class="sxs-lookup"><span data-stu-id="522d5-132">This cmdlet returns a **TrafficManagerEndpoint** object.</span></span>

## <span data-ttu-id="522d5-133">筆記</span><span class="sxs-lookup"><span data-stu-id="522d5-133">NOTES</span></span>

## <span data-ttu-id="522d5-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="522d5-134">RELATED LINKS</span></span>

