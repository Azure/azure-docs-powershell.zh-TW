---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D342
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/remove-aztrafficmanagercustomheaderfromendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerCustomHeaderFromEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerCustomHeaderFromEndpoint.md
ms.openlocfilehash: f0d179c82292ffb9300791337f40436c4d4c5f36
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910849"
---
# <span data-ttu-id="06d80-101">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span><span class="sxs-lookup"><span data-stu-id="06d80-101">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span></span>

## <span data-ttu-id="06d80-102">簡介</span><span class="sxs-lookup"><span data-stu-id="06d80-102">SYNOPSIS</span></span>
<span data-ttu-id="06d80-103">從本地流量管理員端點物件移除自訂標頭資訊。</span><span class="sxs-lookup"><span data-stu-id="06d80-103">Removes custom header information from a local Traffic Manager endpoint object.</span></span>

## <span data-ttu-id="06d80-104">語法</span><span class="sxs-lookup"><span data-stu-id="06d80-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerCustomHeaderFromEndpoint -Name <String> -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06d80-105">描述</span><span class="sxs-lookup"><span data-stu-id="06d80-105">DESCRIPTION</span></span>
<span data-ttu-id="06d80-106">**Remove-AzTrafficManagerCustomHeaderFromEndpoint** Cmdlet 會從本地 Azure Traffic Manager 端點物件移除自訂標頭資訊。</span><span class="sxs-lookup"><span data-stu-id="06d80-106">The **Remove-AzTrafficManagerCustomHeaderFromEndpoint** cmdlet removes custom header information from a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="06d80-107">您可以使用 Cmdlet 或 Cmdlet New-AzTrafficManagerEndpoint端點Get-AzTrafficManagerEndpoint端點。</span><span class="sxs-lookup"><span data-stu-id="06d80-107">You can get an endpoint by using the New-AzTrafficManagerEndpoint or Get-AzTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="06d80-108">此 Cmdlet 在本地端點物件上操作。</span><span class="sxs-lookup"><span data-stu-id="06d80-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="06d80-109">使用 Cmdlet 來為流量管理員的端點Set-AzTrafficManagerEndpoint變更。</span><span class="sxs-lookup"><span data-stu-id="06d80-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="06d80-110">例子</span><span class="sxs-lookup"><span data-stu-id="06d80-110">EXAMPLES</span></span>

### <span data-ttu-id="06d80-111">範例 1：移除端點的自訂子網資訊</span><span class="sxs-lookup"><span data-stu-id="06d80-111">Example 1: Remove custom subnet information from an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
PS C:\> Remove-AzTrafficManagerCustomHeaderFromEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint -Name "host"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="06d80-112">第一個命令會從名為 ResourceGroup11 的資源群組中名為 ContosoProfile 的設定檔中，獲得名為 contosoProfile 的 Azure 端點，然後將該物件儲存在 $TrafficManagerEndpoint 變數中。</span><span class="sxs-lookup"><span data-stu-id="06d80-112">The first command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="06d80-113">第二個命令會從儲存在 $TrafficManagerEndpoint 的端點移除自訂標題$TrafficManagerEndpoint。</span><span class="sxs-lookup"><span data-stu-id="06d80-113">The second command removes custom header information from the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="06d80-114">最後一個命令會更新 Traffic Manager 中的端點，以符合 $TrafficManagerEndpoint。</span><span class="sxs-lookup"><span data-stu-id="06d80-114">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="06d80-115">參數</span><span class="sxs-lookup"><span data-stu-id="06d80-115">PARAMETERS</span></span>

### <span data-ttu-id="06d80-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06d80-116">-DefaultProfile</span></span>
<span data-ttu-id="06d80-117">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="06d80-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06d80-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="06d80-118">-Name</span></span>
<span data-ttu-id="06d80-119">指定要移除的自訂標題資訊名稱。</span><span class="sxs-lookup"><span data-stu-id="06d80-119">Specifies the name of the custom header information to be removed.</span></span>

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

### <span data-ttu-id="06d80-120">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="06d80-120">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="06d80-121">指定一個本地 **TrafficManagerEndpoint** 物件。</span><span class="sxs-lookup"><span data-stu-id="06d80-121">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="06d80-122">此 Cmdlet 會修改此本機物件。</span><span class="sxs-lookup"><span data-stu-id="06d80-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="06d80-123">若要取得 **TrafficManagerEndpoint** 物件，請使用 Get-AzTrafficManagerEndpoint 或 New-AzTrafficManagerEndpoint Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="06d80-123">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint or New-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="06d80-124">-確認</span><span class="sxs-lookup"><span data-stu-id="06d80-124">-Confirm</span></span>
<span data-ttu-id="06d80-125">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="06d80-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06d80-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06d80-126">-WhatIf</span></span>
<span data-ttu-id="06d80-127">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="06d80-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="06d80-128">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="06d80-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06d80-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06d80-129">CommonParameters</span></span>
<span data-ttu-id="06d80-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="06d80-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06d80-131">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="06d80-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06d80-132">輸入</span><span class="sxs-lookup"><span data-stu-id="06d80-132">INPUTS</span></span>

### <span data-ttu-id="06d80-133">Microsoft.Azure.Commands.TrafficManager.models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="06d80-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="06d80-134">輸出</span><span class="sxs-lookup"><span data-stu-id="06d80-134">OUTPUTS</span></span>

### <span data-ttu-id="06d80-135">Microsoft.Azure.Commands.TrafficManager.models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="06d80-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="06d80-136">筆記</span><span class="sxs-lookup"><span data-stu-id="06d80-136">NOTES</span></span>

## <span data-ttu-id="06d80-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="06d80-137">RELATED LINKS</span></span>

[<span data-ttu-id="06d80-138">Add-AzTrafficManagerCustomHeaderToEndpoint</span><span class="sxs-lookup"><span data-stu-id="06d80-138">Add-AzTrafficManagerCustomHeaderToEndpoint</span></span>](./Add-AzTrafficManagerCustomHeaderToEndpoint.md)

[<span data-ttu-id="06d80-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="06d80-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="06d80-140">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="06d80-140">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="06d80-141">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="06d80-141">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)
