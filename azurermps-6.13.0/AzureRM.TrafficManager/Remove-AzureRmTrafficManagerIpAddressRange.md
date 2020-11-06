---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D345
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/remove-azurermtrafficmanagerIpAddressRange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerIpAddressRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerIpAddressRange.md
ms.openlocfilehash: 5bb661dbc5a65b9a245fcfa35cdc194bbcded1eb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445339"
---
# <span data-ttu-id="9db05-101">Remove-AzureRmTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="9db05-101">Remove-AzureRmTrafficManagerIpAddressRange</span></span>

## <span data-ttu-id="9db05-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9db05-102">SYNOPSIS</span></span>
<span data-ttu-id="9db05-103">從本機流量管理器端點物件移除位址範圍或子網。</span><span class="sxs-lookup"><span data-stu-id="9db05-103">Removes an address range or subnet from a local Traffic Manager endpoint object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9db05-104">句法</span><span class="sxs-lookup"><span data-stu-id="9db05-104">SYNTAX</span></span>

```
Remove-AzureRmTrafficManagerIpAddressRange -First <String> -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9db05-105">說明</span><span class="sxs-lookup"><span data-stu-id="9db05-105">DESCRIPTION</span></span>
<span data-ttu-id="9db05-106">**AzureRmTrafficManagerIpAddressRange** Cmdlet 會從本機 Azure 流量管理器端點物件中移除 IP 位址範圍。</span><span class="sxs-lookup"><span data-stu-id="9db05-106">The **Remove-AzureRmTrafficManagerIpAddressRange** cmdlet removes an IP address range from a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="9db05-107">您可以使用 New-AzureRmTrafficManagerEndpoint 或 Get-AzureRmTrafficManagerEndpoint Cmdlet 來取得端點。</span><span class="sxs-lookup"><span data-stu-id="9db05-107">You can get an endpoint by using the New-AzureRmTrafficManagerEndpoint or Get-AzureRmTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="9db05-108">這個 Cmdlet 作用於本機端點物件。</span><span class="sxs-lookup"><span data-stu-id="9db05-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="9db05-109">使用 Set-AzureRmTrafficManagerEndpoint Cmdlet，將您的變更提交至流量管理器的端點。</span><span class="sxs-lookup"><span data-stu-id="9db05-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="9db05-110">示例</span><span class="sxs-lookup"><span data-stu-id="9db05-110">EXAMPLES</span></span>

### <span data-ttu-id="9db05-111">範例1：從端點移除 IP 位址範圍</span><span class="sxs-lookup"><span data-stu-id="9db05-111">Example 1: Remove IP address ranges from an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = Get-AzureRmTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
PS C:\> Remove-AzureRmTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "1.2.3.4"
PS C:\> Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="9db05-112">第一個命令會從名為 ResourceGroup11 的資源群組中，從名為 contoso 的設定檔中取得名為 contoso 的 Azure 端點，然後將該物件儲存在 $TrafficManagerEndpoint 變數中。</span><span class="sxs-lookup"><span data-stu-id="9db05-112">The first command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="9db05-113">第二個命令會從儲存在 $TrafficManagerEndpoint 中的端點中移除 IP 位址範圍。</span><span class="sxs-lookup"><span data-stu-id="9db05-113">The second command removes an IP address range from the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="9db05-114">Final 命令會更新流量管理器中的端點，以符合 $TrafficManagerEndpoint 中的本機值。</span><span class="sxs-lookup"><span data-stu-id="9db05-114">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="9db05-115">參數</span><span class="sxs-lookup"><span data-stu-id="9db05-115">PARAMETERS</span></span>

### <span data-ttu-id="9db05-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9db05-116">-DefaultProfile</span></span>
<span data-ttu-id="9db05-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9db05-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9db05-118">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9db05-118">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="9db05-119">指定本機 **TrafficManagerEndpoint** 物件。</span><span class="sxs-lookup"><span data-stu-id="9db05-119">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="9db05-120">這個 Cmdlet 會修改這個本機物件。</span><span class="sxs-lookup"><span data-stu-id="9db05-120">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="9db05-121">若要取得 **TrafficManagerEndpoint** 物件，請使用 Get-AzureRmTrafficManagerEndpoint 或 New-AzureRmTrafficManagerEndpoint Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9db05-121">To obtain a **TrafficManagerEndpoint** object, use the Get-AzureRmTrafficManagerEndpoint or New-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="9db05-122">-確認</span><span class="sxs-lookup"><span data-stu-id="9db05-122">-Confirm</span></span>
<span data-ttu-id="9db05-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9db05-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9db05-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9db05-124">-WhatIf</span></span>
<span data-ttu-id="9db05-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9db05-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9db05-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9db05-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9db05-127">-優先</span><span class="sxs-lookup"><span data-stu-id="9db05-127">-First</span></span>
<span data-ttu-id="9db05-128">指定要移除之範圍內的第一個 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="9db05-128">Specifies the first IP address in the range to be removed.</span></span>

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

### <span data-ttu-id="9db05-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9db05-129">CommonParameters</span></span>
<span data-ttu-id="9db05-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9db05-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9db05-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9db05-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9db05-132">輸入</span><span class="sxs-lookup"><span data-stu-id="9db05-132">INPUTS</span></span>

### <span data-ttu-id="9db05-133">TrafficManagerEndpoint （）</span><span class="sxs-lookup"><span data-stu-id="9db05-133">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="9db05-134">這個 Cmdlet 接受 **TrafficManagerEndpoint** 物件到這個 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9db05-134">This cmdlet accepts a **TrafficManagerEndpoint** object to this cmdlet.</span></span>

## <span data-ttu-id="9db05-135">輸出</span><span class="sxs-lookup"><span data-stu-id="9db05-135">OUTPUTS</span></span>

### <span data-ttu-id="9db05-136">TrafficManagerEndpoint （）</span><span class="sxs-lookup"><span data-stu-id="9db05-136">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="9db05-137">這個 Cmdlet 會傳回修改過的 TrafficManagerEndpoint 物件。</span><span class="sxs-lookup"><span data-stu-id="9db05-137">This cmdlet returns a modified TrafficManagerEndpoint object.</span></span>

## <span data-ttu-id="9db05-138">筆記</span><span class="sxs-lookup"><span data-stu-id="9db05-138">NOTES</span></span>

## <span data-ttu-id="9db05-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="9db05-139">RELATED LINKS</span></span>

[<span data-ttu-id="9db05-140">附加 AzureRmTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="9db05-140">Add-AzureRmTrafficManagerIpAddressRange</span></span>](./Add-AzureRmTrafficManagerIpAddressRange.md)

[<span data-ttu-id="9db05-141">AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9db05-141">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="9db05-142">新-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9db05-142">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="9db05-143">Set-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9db05-143">Set-AzureRmTrafficManagerEndpoint</span></span>](./Set-AzureRmTrafficManagerEndpoint.md)
