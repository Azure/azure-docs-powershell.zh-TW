---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5287D4DB-2709-4A3C-97D5-DB494CEEFD18
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/set-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 0000a7a1dba5f175d70fb93631176a49a9da2d13
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958985"
---
# <span data-ttu-id="7ac21-101">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7ac21-101">Set-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="7ac21-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7ac21-102">SYNOPSIS</span></span>
<span data-ttu-id="7ac21-103">更新流量管理器端點。</span><span class="sxs-lookup"><span data-stu-id="7ac21-103">Updates a Traffic Manager endpoint.</span></span>

## <span data-ttu-id="7ac21-104">句法</span><span class="sxs-lookup"><span data-stu-id="7ac21-104">SYNTAX</span></span>

```
Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ac21-105">說明</span><span class="sxs-lookup"><span data-stu-id="7ac21-105">DESCRIPTION</span></span>
<span data-ttu-id="7ac21-106">**AzTrafficManagerEndpoint** Cmdlet 會更新 Azure 流量管理器中的端點。</span><span class="sxs-lookup"><span data-stu-id="7ac21-106">The **Set-AzTrafficManagerEndpoint** cmdlet updates an endpoint in Azure Traffic Manager.</span></span>
<span data-ttu-id="7ac21-107">這個 Cmdlet 會更新本機端點物件的設定。</span><span class="sxs-lookup"><span data-stu-id="7ac21-107">This cmdlet updates the settings from a local endpoint object.</span></span>
<span data-ttu-id="7ac21-108">您可以使用 *TrafficManagerEndpoint* 參數或使用管線來指定端點物件。</span><span class="sxs-lookup"><span data-stu-id="7ac21-108">You can specify the endpoint object either by using the *TrafficManagerEndpoint* parameter or by using the pipeline.</span></span>

<span data-ttu-id="7ac21-109">您可以使用 Get-AzTrafficManagerEndpoint Cmdlet 來取得代表端點的局部物件。</span><span class="sxs-lookup"><span data-stu-id="7ac21-109">You can obtain a local object that represents an endpoint by using the Get-AzTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="7ac21-110">在本機修改物件，然後使用 [ **設定] AzTrafficManagerEndpoint** 來認可您的變更。</span><span class="sxs-lookup"><span data-stu-id="7ac21-110">Modify the object locally and then use **Set-AzTrafficManagerEndpoint** to commit your changes.</span></span>

## <span data-ttu-id="7ac21-111">示例</span><span class="sxs-lookup"><span data-stu-id="7ac21-111">EXAMPLES</span></span>

### <span data-ttu-id="7ac21-112">範例1：更新端點</span><span class="sxs-lookup"><span data-stu-id="7ac21-112">Example 1: Update an endpoint</span></span>
```
PS C:\>$TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "endpoint1" -Type AzureEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> $TrafficManagerEndpoint.Weight = 20
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="7ac21-113">第一個命令會使用 **AzTrafficManagerEndpoint** Cmdlet 來取得 Azure 流量管理器端點。</span><span class="sxs-lookup"><span data-stu-id="7ac21-113">The first command gets an Azure Traffic Manager endpoint by using the **Get-AzTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="7ac21-114">該命令會將端點儲存在本機的 $TrafficManagerEndpoint 變數中。</span><span class="sxs-lookup"><span data-stu-id="7ac21-114">The command stores the endpoint locally in the $TrafficManagerEndpoint variable.</span></span>

<span data-ttu-id="7ac21-115">第二個命令會在本機變更該端點。</span><span class="sxs-lookup"><span data-stu-id="7ac21-115">The second command changes that endpoint locally.</span></span>
<span data-ttu-id="7ac21-116">這個命令會將端點寬度變更為20。</span><span class="sxs-lookup"><span data-stu-id="7ac21-116">This command changes the endpoint weight to 20.</span></span>

<span data-ttu-id="7ac21-117">第三個命令會更新流量管理器中的端點，以符合 $TrafficManagerEndpoint 中的本機值。</span><span class="sxs-lookup"><span data-stu-id="7ac21-117">The third command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="7ac21-118">參數</span><span class="sxs-lookup"><span data-stu-id="7ac21-118">PARAMETERS</span></span>

### <span data-ttu-id="7ac21-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ac21-119">-DefaultProfile</span></span>
<span data-ttu-id="7ac21-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7ac21-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ac21-121">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7ac21-121">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="7ac21-122">指定本機 **TrafficManagerEndpoint** 物件。</span><span class="sxs-lookup"><span data-stu-id="7ac21-122">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="7ac21-123">這個 Cmdlet 會更新流量管理器，以符合這個本機物件。</span><span class="sxs-lookup"><span data-stu-id="7ac21-123">This cmdlet updates Traffic Manager to match this local object.</span></span>

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

### <span data-ttu-id="7ac21-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ac21-124">CommonParameters</span></span>
<span data-ttu-id="7ac21-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7ac21-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ac21-126">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7ac21-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ac21-127">輸入</span><span class="sxs-lookup"><span data-stu-id="7ac21-127">INPUTS</span></span>

### <span data-ttu-id="7ac21-128">TrafficManagerEndpoint 中的 TrafficManager。</span><span class="sxs-lookup"><span data-stu-id="7ac21-128">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="7ac21-129">輸出</span><span class="sxs-lookup"><span data-stu-id="7ac21-129">OUTPUTS</span></span>

### <span data-ttu-id="7ac21-130">TrafficManagerEndpoint 中的 TrafficManager。</span><span class="sxs-lookup"><span data-stu-id="7ac21-130">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="7ac21-131">筆記</span><span class="sxs-lookup"><span data-stu-id="7ac21-131">NOTES</span></span>

## <span data-ttu-id="7ac21-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="7ac21-132">RELATED LINKS</span></span>
