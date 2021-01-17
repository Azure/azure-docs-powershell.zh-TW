---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D345
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerIpAddressRange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerIpAddressRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerIpAddressRange.md
ms.openlocfilehash: bfeef76b700eb408da89561464bc5457f94cdd4a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98287951"
---
# <span data-ttu-id="69fc7-101">Remove-AzTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="69fc7-101">Remove-AzTrafficManagerIpAddressRange</span></span>

## <span data-ttu-id="69fc7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="69fc7-102">SYNOPSIS</span></span>
<span data-ttu-id="69fc7-103">從本機流量管理器端點物件移除位址範圍或子網。</span><span class="sxs-lookup"><span data-stu-id="69fc7-103">Removes an address range or subnet from a local Traffic Manager endpoint object.</span></span>

## <span data-ttu-id="69fc7-104">句法</span><span class="sxs-lookup"><span data-stu-id="69fc7-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerIpAddressRange -First <String> -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69fc7-105">說明</span><span class="sxs-lookup"><span data-stu-id="69fc7-105">DESCRIPTION</span></span>
<span data-ttu-id="69fc7-106">**AzTrafficManagerIpAddressRange** Cmdlet 會從本機 Azure 流量管理器端點物件中移除 IP 位址範圍。</span><span class="sxs-lookup"><span data-stu-id="69fc7-106">The **Remove-AzTrafficManagerIpAddressRange** cmdlet removes an IP address range from a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="69fc7-107">您可以使用 New-AzTrafficManagerEndpoint 或 Get-AzTrafficManagerEndpoint Cmdlet 來取得端點。</span><span class="sxs-lookup"><span data-stu-id="69fc7-107">You can get an endpoint by using the New-AzTrafficManagerEndpoint or Get-AzTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="69fc7-108">這個 Cmdlet 作用於本機端點物件。</span><span class="sxs-lookup"><span data-stu-id="69fc7-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="69fc7-109">使用 Set-AzTrafficManagerEndpoint Cmdlet，將您的變更提交至流量管理器的端點。</span><span class="sxs-lookup"><span data-stu-id="69fc7-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="69fc7-110">示例</span><span class="sxs-lookup"><span data-stu-id="69fc7-110">EXAMPLES</span></span>

### <span data-ttu-id="69fc7-111">範例1：從端點移除 IP 位址範圍</span><span class="sxs-lookup"><span data-stu-id="69fc7-111">Example 1: Remove IP address ranges from an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
PS C:\> Remove-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "1.2.3.4"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="69fc7-112">第一個命令會從名為 ResourceGroup11 的資源群組中，從名為 contoso 的設定檔中取得名為 contoso 的 Azure 端點，然後將該物件儲存在 $TrafficManagerEndpoint 變數中。</span><span class="sxs-lookup"><span data-stu-id="69fc7-112">The first command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="69fc7-113">第二個命令會從儲存在 $TrafficManagerEndpoint 中的端點中移除 IP 位址範圍。</span><span class="sxs-lookup"><span data-stu-id="69fc7-113">The second command removes an IP address range from the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="69fc7-114">Final 命令會更新流量管理器中的端點，以符合 $TrafficManagerEndpoint 中的本機值。</span><span class="sxs-lookup"><span data-stu-id="69fc7-114">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="69fc7-115">參數</span><span class="sxs-lookup"><span data-stu-id="69fc7-115">PARAMETERS</span></span>

### <span data-ttu-id="69fc7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69fc7-116">-DefaultProfile</span></span>
<span data-ttu-id="69fc7-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="69fc7-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69fc7-118">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="69fc7-118">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="69fc7-119">指定本機 **TrafficManagerEndpoint** 物件。</span><span class="sxs-lookup"><span data-stu-id="69fc7-119">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="69fc7-120">這個 Cmdlet 會修改這個本機物件。</span><span class="sxs-lookup"><span data-stu-id="69fc7-120">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="69fc7-121">若要取得 **TrafficManagerEndpoint** 物件，請使用 Get-AzTrafficManagerEndpoint 或 New-AzTrafficManagerEndpoint Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="69fc7-121">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint or New-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="69fc7-122">-確認</span><span class="sxs-lookup"><span data-stu-id="69fc7-122">-Confirm</span></span>
<span data-ttu-id="69fc7-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="69fc7-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69fc7-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69fc7-124">-WhatIf</span></span>
<span data-ttu-id="69fc7-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="69fc7-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="69fc7-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="69fc7-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69fc7-127">-優先</span><span class="sxs-lookup"><span data-stu-id="69fc7-127">-First</span></span>
<span data-ttu-id="69fc7-128">指定要移除之範圍內的第一個 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="69fc7-128">Specifies the first IP address in the range to be removed.</span></span>

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

### <span data-ttu-id="69fc7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69fc7-129">CommonParameters</span></span>
<span data-ttu-id="69fc7-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="69fc7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69fc7-131">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="69fc7-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69fc7-132">輸入</span><span class="sxs-lookup"><span data-stu-id="69fc7-132">INPUTS</span></span>

### <span data-ttu-id="69fc7-133">TrafficManagerEndpoint 中的 TrafficManager。</span><span class="sxs-lookup"><span data-stu-id="69fc7-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="69fc7-134">輸出</span><span class="sxs-lookup"><span data-stu-id="69fc7-134">OUTPUTS</span></span>

### <span data-ttu-id="69fc7-135">TrafficManagerEndpoint 中的 TrafficManager。</span><span class="sxs-lookup"><span data-stu-id="69fc7-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="69fc7-136">筆記</span><span class="sxs-lookup"><span data-stu-id="69fc7-136">NOTES</span></span>

## <span data-ttu-id="69fc7-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="69fc7-137">RELATED LINKS</span></span>

[<span data-ttu-id="69fc7-138">附加 AzTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="69fc7-138">Add-AzTrafficManagerIpAddressRange</span></span>](./Add-AzTrafficManagerIpAddressRange.md)

[<span data-ttu-id="69fc7-139">AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="69fc7-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="69fc7-140">新-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="69fc7-140">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="69fc7-141">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="69fc7-141">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)
