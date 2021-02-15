---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D341
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagerIpAddressRange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerIpAddressRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerIpAddressRange.md
ms.openlocfilehash: 2cececec0610b813bf59a1ef8adac59e1fa8ddb2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100138174"
---
# <span data-ttu-id="ec924-101">Add-AzTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="ec924-101">Add-AzTrafficManagerIpAddressRange</span></span>

## <span data-ttu-id="ec924-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ec924-102">SYNOPSIS</span></span>
<span data-ttu-id="ec924-103">將位址範圍或子網新增至本機流量管理器端點物件。</span><span class="sxs-lookup"><span data-stu-id="ec924-103">Adds an address range or subnet to a local Traffic Manager endpoint object.</span></span>

## <span data-ttu-id="ec924-104">句法</span><span class="sxs-lookup"><span data-stu-id="ec924-104">SYNTAX</span></span>

```
Add-AzTrafficManagerIpAddressRange -First <String> [-Last <String>] [-Scope <Int32>]
 -TrafficManagerEndpoint <TrafficManagerEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec924-105">說明</span><span class="sxs-lookup"><span data-stu-id="ec924-105">DESCRIPTION</span></span>
<span data-ttu-id="ec924-106">**載入 AzTrafficManagerIpAddressRange** Cmdlet 會將 IP 位址範圍新增至本機 Azure 流量管理器端點物件。</span><span class="sxs-lookup"><span data-stu-id="ec924-106">The **Add-AzTrafficManagerIpAddressRange** cmdlet adds an IP address range to a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="ec924-107">您可以使用 New-AzTrafficManagerEndpoint 或 Get-AzTrafficManagerEndpoint Cmdlet 來取得端點。</span><span class="sxs-lookup"><span data-stu-id="ec924-107">You can get an endpoint by using the New-AzTrafficManagerEndpoint or Get-AzTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="ec924-108">這個 Cmdlet 作用於本機端點物件。</span><span class="sxs-lookup"><span data-stu-id="ec924-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="ec924-109">使用 Set-AzTrafficManagerEndpoint Cmdlet，將您的變更提交至流量管理器的端點。</span><span class="sxs-lookup"><span data-stu-id="ec924-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="ec924-110">示例</span><span class="sxs-lookup"><span data-stu-id="ec924-110">EXAMPLES</span></span>

### <span data-ttu-id="ec924-111">範例1：將 IP 位址範圍新增至端點</span><span class="sxs-lookup"><span data-stu-id="ec924-111">Example 1: Add IP address ranges to an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
PS C:\> Add-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "1.2.3.4" -Last "5.6.7.8"
PS C:\> Add-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "9.10.11.0" -Scope 24
PS C:\> Add-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "12.13.14.0" -Last "12.13.14.31" -Scope 27
PS C:\> Add-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "15.16.17.18"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="ec924-112">第一個命令會使用 **AzTrafficManagerEndpoint** Cmdlet 來建立 Azure 流量管理器端點。</span><span class="sxs-lookup"><span data-stu-id="ec924-112">The first command creates an Azure Traffic Manager endpoint by using the **New-AzTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="ec924-113">該命令會將本機端點儲存在 $TrafficManagerEndpoint 變數中。</span><span class="sxs-lookup"><span data-stu-id="ec924-113">The command stores the local endpoint in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="ec924-114">第二個命令會將 IP 位址範圍 1.2.3.4 5.6.7.8 至儲存在 $TrafficManagerEndpoint 的端點。</span><span class="sxs-lookup"><span data-stu-id="ec924-114">The second command adds the IP address range 1.2.3.4 to 5.6.7.8 to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="ec924-115">第三個命令會將 IP 位址範圍9.10.11.0 新增至儲存在 $TrafficManagerEndpoint 的端點。</span><span class="sxs-lookup"><span data-stu-id="ec924-115">The third command adds the IP address range 9.10.11.0 to 9.10.11.255 to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="ec924-116">第四個命令會驗證範圍是否與範圍的大小相符，然後將 IP 位址範圍12.13.14.0 新增至儲存在 $TrafficManagerEndpoint 中的端點。</span><span class="sxs-lookup"><span data-stu-id="ec924-116">The fourth command verifies that the scope matches the size of the range, then adds the IP address range 12.13.14.0 to 12.13.14.31 to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="ec924-117">第五個命令會將 IP 位址範圍15.16.17.18 新增至儲存在 $TrafficManagerEndpoint 的端點。</span><span class="sxs-lookup"><span data-stu-id="ec924-117">The fifth command adds the IP address range 15.16.17.18 to 15.16.17.18 to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="ec924-118">Final 命令會更新流量管理器中的端點，以符合 $TrafficManagerEndpoint 中的本機值。</span><span class="sxs-lookup"><span data-stu-id="ec924-118">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="ec924-119">參數</span><span class="sxs-lookup"><span data-stu-id="ec924-119">PARAMETERS</span></span>

### <span data-ttu-id="ec924-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec924-120">-DefaultProfile</span></span>
<span data-ttu-id="ec924-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ec924-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec924-122">-上次</span><span class="sxs-lookup"><span data-stu-id="ec924-122">-Last</span></span>
<span data-ttu-id="ec924-123">指定要新增範圍中的最後一個 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="ec924-123">Specifies the last IP address in the range to be added.</span></span>

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

### <span data-ttu-id="ec924-124">-範圍</span><span class="sxs-lookup"><span data-stu-id="ec924-124">-Scope</span></span>
<span data-ttu-id="ec924-125">指定要新增之 IP 位址範圍的範圍。</span><span class="sxs-lookup"><span data-stu-id="ec924-125">Specifies the scope of the IP address range to be added.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec924-126">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ec924-126">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="ec924-127">指定本機 **TrafficManagerEndpoint** 物件。</span><span class="sxs-lookup"><span data-stu-id="ec924-127">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="ec924-128">這個 Cmdlet 會修改這個本機物件。</span><span class="sxs-lookup"><span data-stu-id="ec924-128">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="ec924-129">若要取得 **TrafficManagerEndpoint** 物件，請使用 Get-AzTrafficManagerEndpoint 或 New-AzTrafficManagerEndpoint Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ec924-129">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint or New-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="ec924-130">-確認</span><span class="sxs-lookup"><span data-stu-id="ec924-130">-Confirm</span></span>
<span data-ttu-id="ec924-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ec924-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec924-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec924-132">-WhatIf</span></span>
<span data-ttu-id="ec924-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ec924-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ec924-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ec924-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec924-135">-優先</span><span class="sxs-lookup"><span data-stu-id="ec924-135">-First</span></span>
<span data-ttu-id="ec924-136">指定要新增範圍中的第一個 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="ec924-136">Specifies the first IP address in the range to be added.</span></span>

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

### <span data-ttu-id="ec924-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec924-137">CommonParameters</span></span>
<span data-ttu-id="ec924-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ec924-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec924-139">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ec924-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec924-140">輸入</span><span class="sxs-lookup"><span data-stu-id="ec924-140">INPUTS</span></span>

### <span data-ttu-id="ec924-141">TrafficManagerEndpoint 中的 TrafficManager。</span><span class="sxs-lookup"><span data-stu-id="ec924-141">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="ec924-142">輸出</span><span class="sxs-lookup"><span data-stu-id="ec924-142">OUTPUTS</span></span>

### <span data-ttu-id="ec924-143">TrafficManagerEndpoint 中的 TrafficManager。</span><span class="sxs-lookup"><span data-stu-id="ec924-143">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="ec924-144">筆記</span><span class="sxs-lookup"><span data-stu-id="ec924-144">NOTES</span></span>

## <span data-ttu-id="ec924-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="ec924-145">RELATED LINKS</span></span>

[<span data-ttu-id="ec924-146">移除-AzTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="ec924-146">Remove-AzTrafficManagerIpAddressRange</span></span>](./Remove-AzTrafficManagerIpAddressRange.md)

[<span data-ttu-id="ec924-147">新-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ec924-147">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="ec924-148">AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ec924-148">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="ec924-149">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ec924-149">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)
