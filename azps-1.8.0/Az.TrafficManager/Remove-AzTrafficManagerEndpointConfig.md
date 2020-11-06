---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 8E12A392-A100-4814-9003-B2999150DCE1
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpointConfig.md
ms.openlocfilehash: f40587460cf5e4a1d7f06bfb88229f6e4e3f7975
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614330"
---
# <span data-ttu-id="b6a89-101">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="b6a89-101">Remove-AzTrafficManagerEndpointConfig</span></span>

## <span data-ttu-id="b6a89-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b6a89-102">SYNOPSIS</span></span>
<span data-ttu-id="b6a89-103">從本機流量管理器設定檔物件移除端點。</span><span class="sxs-lookup"><span data-stu-id="b6a89-103">Removes an endpoint from a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="b6a89-104">句法</span><span class="sxs-lookup"><span data-stu-id="b6a89-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6a89-105">說明</span><span class="sxs-lookup"><span data-stu-id="b6a89-105">DESCRIPTION</span></span>
<span data-ttu-id="b6a89-106">**AzTrafficManagerEndpointConfig** Cmdlet 會從本機 Azure 流量管理器設定檔物件中移除端點。</span><span class="sxs-lookup"><span data-stu-id="b6a89-106">The **Remove-AzTrafficManagerEndpointConfig** cmdlet removes an endpoint from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="b6a89-107">您可以使用 Get-AzTrafficManagerProfile Cmdlet 來取得設定檔。</span><span class="sxs-lookup"><span data-stu-id="b6a89-107">You can get a profile by using the Get-AzTrafficManagerProfile cmdlet.</span></span>

<span data-ttu-id="b6a89-108">這個 Cmdlet 作用於本機設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="b6a89-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="b6a89-109">使用 Set-AzTrafficManagerProfile Cmdlet，將您的變更提交至流量管理器的設定檔。</span><span class="sxs-lookup"><span data-stu-id="b6a89-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="b6a89-110">若要移除端點並在單一作業中提交變更，請使用 Remove-AzTrafficManagerEndpoint Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b6a89-110">To remove an endpoint and commit changes in a single operation, use the Remove-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="b6a89-111">示例</span><span class="sxs-lookup"><span data-stu-id="b6a89-111">EXAMPLES</span></span>

### <span data-ttu-id="b6a89-112">範例1：移除端點</span><span class="sxs-lookup"><span data-stu-id="b6a89-112">Example 1: Remove an endpoint</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzTrafficManagerEndpointConfig -EndpointName "contoso" -TrafficManagerProfile $TrafficManagerProfile 
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="b6a89-113">第一個命令會使用 **AzTrafficManagerProfile** Cmdlet 取得 Azure 流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="b6a89-113">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="b6a89-114">該命令會將本機設定檔儲存在 $TrafficManagerProfile 變數中。</span><span class="sxs-lookup"><span data-stu-id="b6a89-114">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="b6a89-115">第二個命令會將名為 contoso 的 Azure 端點從儲存在 $TrafficManagerProfile 的設定檔中移除。</span><span class="sxs-lookup"><span data-stu-id="b6a89-115">The second command removes an Azure endpoint named contoso from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="b6a89-116">這個命令只會變更本機物件。</span><span class="sxs-lookup"><span data-stu-id="b6a89-116">This command changes only the local object.</span></span>

<span data-ttu-id="b6a89-117">Final 命令會更新名為 ContosoProfile 的流量管理器設定檔，以符合 $TrafficManagerProfile 中的本機值。</span><span class="sxs-lookup"><span data-stu-id="b6a89-117">The final command updates the Traffic Manager profile named ContosoProfile to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="b6a89-118">參數</span><span class="sxs-lookup"><span data-stu-id="b6a89-118">PARAMETERS</span></span>

### <span data-ttu-id="b6a89-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6a89-119">-DefaultProfile</span></span>
<span data-ttu-id="b6a89-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b6a89-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6a89-121">-終結點</span><span class="sxs-lookup"><span data-stu-id="b6a89-121">-EndpointName</span></span>
<span data-ttu-id="b6a89-122">指定此 Cmdlet 移除之流量管理器端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="b6a89-122">Specifies the name of the Traffic Manager endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b6a89-123">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b6a89-123">-TrafficManagerProfile</span></span>
<span data-ttu-id="b6a89-124">指定本機 **TrafficManagerProfile** 物件。</span><span class="sxs-lookup"><span data-stu-id="b6a89-124">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="b6a89-125">這個 Cmdlet 會修改這個本機物件。</span><span class="sxs-lookup"><span data-stu-id="b6a89-125">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="b6a89-126">若要取得 **TrafficManagerProfile** 物件，請使用 Get-AzTrafficManagerProfile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b6a89-126">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="b6a89-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6a89-127">CommonParameters</span></span>
<span data-ttu-id="b6a89-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b6a89-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6a89-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b6a89-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6a89-130">輸入</span><span class="sxs-lookup"><span data-stu-id="b6a89-130">INPUTS</span></span>

### <span data-ttu-id="b6a89-131">TrafficManagerProfile 中的 TrafficManager。</span><span class="sxs-lookup"><span data-stu-id="b6a89-131">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="b6a89-132">輸出</span><span class="sxs-lookup"><span data-stu-id="b6a89-132">OUTPUTS</span></span>

### <span data-ttu-id="b6a89-133">TrafficManagerProfile 中的 TrafficManager。</span><span class="sxs-lookup"><span data-stu-id="b6a89-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="b6a89-134">筆記</span><span class="sxs-lookup"><span data-stu-id="b6a89-134">NOTES</span></span>

## <span data-ttu-id="b6a89-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="b6a89-135">RELATED LINKS</span></span>

[<span data-ttu-id="b6a89-136">附加 AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="b6a89-136">Add-AzTrafficManagerEndpointConfig</span></span>](./Add-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="b6a89-137">AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b6a89-137">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="b6a89-138">移除-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b6a89-138">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="b6a89-139">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b6a89-139">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)

