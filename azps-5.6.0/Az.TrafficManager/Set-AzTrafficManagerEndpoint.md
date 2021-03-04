---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5287D4DB-2709-4A3C-97D5-DB494CEEFD18
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/set-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 8f8ba0297ac0302e50dfdfdc25ddc3941fb10e34
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910834"
---
# <span data-ttu-id="b8c2c-101">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b8c2c-101">Set-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="b8c2c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b8c2c-102">SYNOPSIS</span></span>
<span data-ttu-id="b8c2c-103">更新流量管理員端點。</span><span class="sxs-lookup"><span data-stu-id="b8c2c-103">Updates a Traffic Manager endpoint.</span></span>

## <span data-ttu-id="b8c2c-104">語法</span><span class="sxs-lookup"><span data-stu-id="b8c2c-104">SYNTAX</span></span>

```
Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8c2c-105">描述</span><span class="sxs-lookup"><span data-stu-id="b8c2c-105">DESCRIPTION</span></span>
<span data-ttu-id="b8c2c-106">**Set-AzTrafficManagerEndpoint** Cmdlet 會更新 Azure 流量管理員中的端點。</span><span class="sxs-lookup"><span data-stu-id="b8c2c-106">The **Set-AzTrafficManagerEndpoint** cmdlet updates an endpoint in Azure Traffic Manager.</span></span>
<span data-ttu-id="b8c2c-107">此 Cmdlet 會更新來自本地端點物件的設定。</span><span class="sxs-lookup"><span data-stu-id="b8c2c-107">This cmdlet updates the settings from a local endpoint object.</span></span>
<span data-ttu-id="b8c2c-108">您可以使用 *TrafficManagerEndpoint* 參數或管道來指定端點物件。</span><span class="sxs-lookup"><span data-stu-id="b8c2c-108">You can specify the endpoint object either by using the *TrafficManagerEndpoint* parameter or by using the pipeline.</span></span>

<span data-ttu-id="b8c2c-109">您可以使用 Cmdlet 取得代表端點的Get-AzTrafficManagerEndpoint物件。</span><span class="sxs-lookup"><span data-stu-id="b8c2c-109">You can obtain a local object that represents an endpoint by using the Get-AzTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="b8c2c-110">在本地修改物件，然後使用 **Set-AzTrafficManagerEndpoint** 來提交變更。</span><span class="sxs-lookup"><span data-stu-id="b8c2c-110">Modify the object locally and then use **Set-AzTrafficManagerEndpoint** to commit your changes.</span></span>

## <span data-ttu-id="b8c2c-111">例子</span><span class="sxs-lookup"><span data-stu-id="b8c2c-111">EXAMPLES</span></span>

### <span data-ttu-id="b8c2c-112">範例 1：更新端點</span><span class="sxs-lookup"><span data-stu-id="b8c2c-112">Example 1: Update an endpoint</span></span>
```
PS C:\>$TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "endpoint1" -Type AzureEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> $TrafficManagerEndpoint.Weight = 20
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="b8c2c-113">第一個命令會使用 **Get-AzTrafficManagerEndpoint** Cmdlet 取得 Azure 流量管理員端點。</span><span class="sxs-lookup"><span data-stu-id="b8c2c-113">The first command gets an Azure Traffic Manager endpoint by using the **Get-AzTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="b8c2c-114">該命令將端點儲存在 $TrafficManagerEndpoint 變數中。</span><span class="sxs-lookup"><span data-stu-id="b8c2c-114">The command stores the endpoint locally in the $TrafficManagerEndpoint variable.</span></span>

<span data-ttu-id="b8c2c-115">第二個命令會變更本地端點。</span><span class="sxs-lookup"><span data-stu-id="b8c2c-115">The second command changes that endpoint locally.</span></span>
<span data-ttu-id="b8c2c-116">此命令將端點粗細變更為 20。</span><span class="sxs-lookup"><span data-stu-id="b8c2c-116">This command changes the endpoint weight to 20.</span></span>

<span data-ttu-id="b8c2c-117">第三個命令會更新 Traffic Manager 中的端點，以符合 $TrafficManagerEndpoint。</span><span class="sxs-lookup"><span data-stu-id="b8c2c-117">The third command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="b8c2c-118">參數</span><span class="sxs-lookup"><span data-stu-id="b8c2c-118">PARAMETERS</span></span>

### <span data-ttu-id="b8c2c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8c2c-119">-DefaultProfile</span></span>
<span data-ttu-id="b8c2c-120">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b8c2c-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8c2c-121">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b8c2c-121">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="b8c2c-122">指定一個本地 **TrafficManagerEndpoint** 物件。</span><span class="sxs-lookup"><span data-stu-id="b8c2c-122">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="b8c2c-123">此 Cmdlet 會更新流量管理員，以符合此本機物件。</span><span class="sxs-lookup"><span data-stu-id="b8c2c-123">This cmdlet updates Traffic Manager to match this local object.</span></span>

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

### <span data-ttu-id="b8c2c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8c2c-124">CommonParameters</span></span>
<span data-ttu-id="b8c2c-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b8c2c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8c2c-126">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="b8c2c-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8c2c-127">輸入</span><span class="sxs-lookup"><span data-stu-id="b8c2c-127">INPUTS</span></span>

### <span data-ttu-id="b8c2c-128">Microsoft.Azure.Commands.TrafficManager.models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b8c2c-128">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="b8c2c-129">輸出</span><span class="sxs-lookup"><span data-stu-id="b8c2c-129">OUTPUTS</span></span>

### <span data-ttu-id="b8c2c-130">Microsoft.Azure.Commands.TrafficManager.models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b8c2c-130">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="b8c2c-131">筆記</span><span class="sxs-lookup"><span data-stu-id="b8c2c-131">NOTES</span></span>

## <span data-ttu-id="b8c2c-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="b8c2c-132">RELATED LINKS</span></span>
