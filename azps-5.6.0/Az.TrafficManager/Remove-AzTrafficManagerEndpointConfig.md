---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 8E12A392-A100-4814-9003-B2999150DCE1
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/remove-aztrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpointConfig.md
ms.openlocfilehash: 1dac991645d6f57ba4fe30a82955531b7fdb3f5a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910842"
---
# <span data-ttu-id="ad335-101">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="ad335-101">Remove-AzTrafficManagerEndpointConfig</span></span>

## <span data-ttu-id="ad335-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ad335-102">SYNOPSIS</span></span>
<span data-ttu-id="ad335-103">從本地流量管理員設定檔物件移除端點。</span><span class="sxs-lookup"><span data-stu-id="ad335-103">Removes an endpoint from a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="ad335-104">語法</span><span class="sxs-lookup"><span data-stu-id="ad335-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad335-105">描述</span><span class="sxs-lookup"><span data-stu-id="ad335-105">DESCRIPTION</span></span>
<span data-ttu-id="ad335-106">**Remove-AzTrafficManagerEndpointConfig** Cmdlet 會從本地 Azure 流量管理員設定檔物件移除端點。</span><span class="sxs-lookup"><span data-stu-id="ad335-106">The **Remove-AzTrafficManagerEndpointConfig** cmdlet removes an endpoint from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="ad335-107">您可以使用 Cmdlet 取得Get-AzTrafficManagerProfile設定檔。</span><span class="sxs-lookup"><span data-stu-id="ad335-107">You can get a profile by using the Get-AzTrafficManagerProfile cmdlet.</span></span>

<span data-ttu-id="ad335-108">此 Cmdlet 可在本地設定檔物件上操作。</span><span class="sxs-lookup"><span data-stu-id="ad335-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="ad335-109">使用 Cmdlet 來針對流量管理員的設定檔Set-AzTrafficManagerProfile變更。</span><span class="sxs-lookup"><span data-stu-id="ad335-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="ad335-110">若要在單一作業中移除端點並提交變更，請使用 Remove-AzTrafficManagerEndpoint Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ad335-110">To remove an endpoint and commit changes in a single operation, use the Remove-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="ad335-111">例子</span><span class="sxs-lookup"><span data-stu-id="ad335-111">EXAMPLES</span></span>

### <span data-ttu-id="ad335-112">範例 1：移除端點</span><span class="sxs-lookup"><span data-stu-id="ad335-112">Example 1: Remove an endpoint</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzTrafficManagerEndpointConfig -EndpointName "contoso" -TrafficManagerProfile $TrafficManagerProfile 
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="ad335-113">第一個命令會使用 **Get-AzTrafficManagerProfile** Cmdlet 取得 Azure 流量管理員設定檔。</span><span class="sxs-lookup"><span data-stu-id="ad335-113">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="ad335-114">該命令將本地設定檔儲存在 $TrafficManagerProfile 變數中。</span><span class="sxs-lookup"><span data-stu-id="ad335-114">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="ad335-115">第二個命令會從儲存在 $TrafficManagerProfile 中的設定檔移除名為 contoso 的 Azure 端點。</span><span class="sxs-lookup"><span data-stu-id="ad335-115">The second command removes an Azure endpoint named contoso from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="ad335-116">此命令只會變更本機物件。</span><span class="sxs-lookup"><span data-stu-id="ad335-116">This command changes only the local object.</span></span>

<span data-ttu-id="ad335-117">最後一個命令會更新名為 ContosoProfile 的流量管理員設定檔，以符合 $TrafficManagerProfile。</span><span class="sxs-lookup"><span data-stu-id="ad335-117">The final command updates the Traffic Manager profile named ContosoProfile to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="ad335-118">參數</span><span class="sxs-lookup"><span data-stu-id="ad335-118">PARAMETERS</span></span>

### <span data-ttu-id="ad335-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad335-119">-DefaultProfile</span></span>
<span data-ttu-id="ad335-120">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ad335-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad335-121">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="ad335-121">-EndpointName</span></span>
<span data-ttu-id="ad335-122">指定此 Cmdlet 移除的流量管理員端點名稱。</span><span class="sxs-lookup"><span data-stu-id="ad335-122">Specifies the name of the Traffic Manager endpoint that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad335-123">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ad335-123">-TrafficManagerProfile</span></span>
<span data-ttu-id="ad335-124">指定一個本地 **TrafficManagerProfile** 物件。</span><span class="sxs-lookup"><span data-stu-id="ad335-124">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="ad335-125">此 Cmdlet 會修改此本機物件。</span><span class="sxs-lookup"><span data-stu-id="ad335-125">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="ad335-126">若要取得 **TrafficManagerProfile** 物件，請使用 Get-AzTrafficManagerProfile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ad335-126">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad335-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad335-127">CommonParameters</span></span>
<span data-ttu-id="ad335-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ad335-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad335-129">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="ad335-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad335-130">輸入</span><span class="sxs-lookup"><span data-stu-id="ad335-130">INPUTS</span></span>

### <span data-ttu-id="ad335-131">Microsoft.Azure.Commands.TrafficManager.models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ad335-131">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="ad335-132">輸出</span><span class="sxs-lookup"><span data-stu-id="ad335-132">OUTPUTS</span></span>

### <span data-ttu-id="ad335-133">Microsoft.Azure.Commands.TrafficManager.models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ad335-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="ad335-134">筆記</span><span class="sxs-lookup"><span data-stu-id="ad335-134">NOTES</span></span>

## <span data-ttu-id="ad335-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="ad335-135">RELATED LINKS</span></span>

[<span data-ttu-id="ad335-136">Add-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="ad335-136">Add-AzTrafficManagerEndpointConfig</span></span>](./Add-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="ad335-137">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ad335-137">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="ad335-138">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ad335-138">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="ad335-139">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ad335-139">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


