---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 8E12A392-A100-4814-9003-B2999150DCE1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/remove-azurermtrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerEndpointConfig.md
ms.openlocfilehash: 3468730caa727c7c8cde46ddbf431c374361b8fa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445344"
---
# <span data-ttu-id="f845b-101">Remove-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="f845b-101">Remove-AzureRmTrafficManagerEndpointConfig</span></span>

## <span data-ttu-id="f845b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f845b-102">SYNOPSIS</span></span>
<span data-ttu-id="f845b-103">從本機流量管理器設定檔物件移除端點。</span><span class="sxs-lookup"><span data-stu-id="f845b-103">Removes an endpoint from a local Traffic Manager profile object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f845b-104">句法</span><span class="sxs-lookup"><span data-stu-id="f845b-104">SYNTAX</span></span>

```
Remove-AzureRmTrafficManagerEndpointConfig -EndpointName <String>
 -TrafficManagerProfile <TrafficManagerProfile> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f845b-105">說明</span><span class="sxs-lookup"><span data-stu-id="f845b-105">DESCRIPTION</span></span>
<span data-ttu-id="f845b-106">**AzureRmTrafficManagerEndpointConfig** Cmdlet 會從本機 Azure 流量管理器設定檔物件中移除端點。</span><span class="sxs-lookup"><span data-stu-id="f845b-106">The **Remove-AzureRmTrafficManagerEndpointConfig** cmdlet removes an endpoint from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="f845b-107">您可以使用 Get-AzureRmTrafficManagerProfile Cmdlet 來取得設定檔。</span><span class="sxs-lookup"><span data-stu-id="f845b-107">You can get a profile by using the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

<span data-ttu-id="f845b-108">這個 Cmdlet 作用於本機設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="f845b-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="f845b-109">使用 Set-AzureRmTrafficManagerProfile Cmdlet，將您的變更提交至流量管理器的設定檔。</span><span class="sxs-lookup"><span data-stu-id="f845b-109">Commit your changes to the profile for Traffic Manager by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="f845b-110">若要移除端點並在單一作業中提交變更，請使用 Remove-AzureRmTrafficManagerEndpoint Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f845b-110">To remove an endpoint and commit changes in a single operation, use the Remove-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="f845b-111">示例</span><span class="sxs-lookup"><span data-stu-id="f845b-111">EXAMPLES</span></span>

### <span data-ttu-id="f845b-112">範例1：移除端點</span><span class="sxs-lookup"><span data-stu-id="f845b-112">Example 1: Remove an endpoint</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzureRmTrafficManagerEndpointConfig -EndpointName "contoso" -TrafficManagerProfile $TrafficManagerProfile 
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="f845b-113">第一個命令會使用 **AzureRmTrafficManagerProfile** Cmdlet 取得 Azure 流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="f845b-113">The first command gets an Azure Traffic Manager profile by using the **Get-AzureRmTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="f845b-114">該命令會將本機設定檔儲存在 $TrafficManagerProfile 變數中。</span><span class="sxs-lookup"><span data-stu-id="f845b-114">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="f845b-115">第二個命令會將名為 contoso 的 Azure 端點從儲存在 $TrafficManagerProfile 的設定檔中移除。</span><span class="sxs-lookup"><span data-stu-id="f845b-115">The second command removes an Azure endpoint named contoso from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="f845b-116">這個命令只會變更本機物件。</span><span class="sxs-lookup"><span data-stu-id="f845b-116">This command changes only the local object.</span></span>

<span data-ttu-id="f845b-117">Final 命令會更新名為 ContosoProfile 的流量管理器設定檔，以符合 $TrafficManagerProfile 中的本機值。</span><span class="sxs-lookup"><span data-stu-id="f845b-117">The final command updates the Traffic Manager profile named ContosoProfile to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="f845b-118">參數</span><span class="sxs-lookup"><span data-stu-id="f845b-118">PARAMETERS</span></span>

### <span data-ttu-id="f845b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f845b-119">-DefaultProfile</span></span>
<span data-ttu-id="f845b-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f845b-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f845b-121">-終結點</span><span class="sxs-lookup"><span data-stu-id="f845b-121">-EndpointName</span></span>
<span data-ttu-id="f845b-122">指定此 Cmdlet 移除之流量管理器端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="f845b-122">Specifies the name of the Traffic Manager endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f845b-123">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f845b-123">-TrafficManagerProfile</span></span>
<span data-ttu-id="f845b-124">指定本機 **TrafficManagerProfile** 物件。</span><span class="sxs-lookup"><span data-stu-id="f845b-124">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="f845b-125">這個 Cmdlet 會修改這個本機物件。</span><span class="sxs-lookup"><span data-stu-id="f845b-125">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="f845b-126">若要取得 **TrafficManagerProfile** 物件，請使用 Get-AzureRmTrafficManagerProfile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f845b-126">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="f845b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f845b-127">CommonParameters</span></span>
<span data-ttu-id="f845b-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f845b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f845b-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f845b-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f845b-130">輸入</span><span class="sxs-lookup"><span data-stu-id="f845b-130">INPUTS</span></span>

### <span data-ttu-id="f845b-131">TrafficManagerProfile （）</span><span class="sxs-lookup"><span data-stu-id="f845b-131">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="f845b-132">這個 Cmdlet 接受 **TrafficManagerProfile** 物件到這個 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f845b-132">This cmdlet accepts a **TrafficManagerProfile** object to this cmdlet.</span></span>

## <span data-ttu-id="f845b-133">輸出</span><span class="sxs-lookup"><span data-stu-id="f845b-133">OUTPUTS</span></span>

### <span data-ttu-id="f845b-134">TrafficManagerProfile （）</span><span class="sxs-lookup"><span data-stu-id="f845b-134">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="f845b-135">這個 Cmdlet 會傳回修改過的 TrafficManagerProfile 物件。</span><span class="sxs-lookup"><span data-stu-id="f845b-135">This cmdlet returns a modified TrafficManagerProfile object.</span></span>

## <span data-ttu-id="f845b-136">筆記</span><span class="sxs-lookup"><span data-stu-id="f845b-136">NOTES</span></span>

## <span data-ttu-id="f845b-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="f845b-137">RELATED LINKS</span></span>

[<span data-ttu-id="f845b-138">附加 AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="f845b-138">Add-AzureRmTrafficManagerEndpointConfig</span></span>](./Add-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="f845b-139">AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f845b-139">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="f845b-140">移除-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f845b-140">Remove-AzureRmTrafficManagerEndpoint</span></span>](./Remove-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="f845b-141">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f845b-141">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


