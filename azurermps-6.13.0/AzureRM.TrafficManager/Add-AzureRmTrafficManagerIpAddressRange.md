---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D341
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/add-azurermtrafficmanagerIpAddressRange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerIpAddressRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerIpAddressRange.md
ms.openlocfilehash: 213e959ecfec178644246f56be11e5b7306ef07f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445372"
---
# <span data-ttu-id="475f1-101">Add-AzureRmTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="475f1-101">Add-AzureRmTrafficManagerIpAddressRange</span></span>

## <span data-ttu-id="475f1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="475f1-102">SYNOPSIS</span></span>
<span data-ttu-id="475f1-103">將位址範圍或子網新增至本機流量管理器端點物件。</span><span class="sxs-lookup"><span data-stu-id="475f1-103">Adds an address range or subnet to a local Traffic Manager endpoint object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="475f1-104">句法</span><span class="sxs-lookup"><span data-stu-id="475f1-104">SYNTAX</span></span>

```
Add-AzureRmTrafficManagerIpAddressRange -First <String> [-Last <String>] [-Scope <Int32>]
 -TrafficManagerEndpoint <TrafficManagerEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="475f1-105">說明</span><span class="sxs-lookup"><span data-stu-id="475f1-105">DESCRIPTION</span></span>
<span data-ttu-id="475f1-106">**載入 AzureRmTrafficManagerIpAddressRange** Cmdlet 會將 IP 位址範圍新增至本機 Azure 流量管理器端點物件。</span><span class="sxs-lookup"><span data-stu-id="475f1-106">The **Add-AzureRmTrafficManagerIpAddressRange** cmdlet adds an IP address range to a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="475f1-107">您可以使用 New-AzureRmTrafficManagerEndpoint 或 Get-AzureRmTrafficManagerEndpoint Cmdlet 來取得端點。</span><span class="sxs-lookup"><span data-stu-id="475f1-107">You can get an endpoint by using the New-AzureRmTrafficManagerEndpoint or Get-AzureRmTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="475f1-108">這個 Cmdlet 作用於本機端點物件。</span><span class="sxs-lookup"><span data-stu-id="475f1-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="475f1-109">使用 Set-AzureRmTrafficManagerEndpoint Cmdlet，將您的變更提交至流量管理器的端點。</span><span class="sxs-lookup"><span data-stu-id="475f1-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="475f1-110">示例</span><span class="sxs-lookup"><span data-stu-id="475f1-110">EXAMPLES</span></span>

### <span data-ttu-id="475f1-111">範例1：將 IP 位址範圍新增至端點</span><span class="sxs-lookup"><span data-stu-id="475f1-111">Example 1: Add IP address ranges to an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = New-AzureRmTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
PS C:\> Add-AzureRmTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "1.2.3.4" -Last "5.6.7.8"
PS C:\> Add-AzureRmTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "9.10.11.0" -Scope 24
PS C:\> Add-AzureRmTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "12.13.14.0" -Last "12.13.14.31" -Scope 27
PS C:\> Add-AzureRmTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "15.16.17.18"
PS C:\> Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="475f1-112">第一個命令會使用 **AzureRmTrafficManagerEndpoint** Cmdlet 來建立 Azure 流量管理器端點。</span><span class="sxs-lookup"><span data-stu-id="475f1-112">The first command creates an Azure Traffic Manager endpoint by using the **New-AzureRmTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="475f1-113">該命令會將本機端點儲存在 $TrafficManagerEndpoint 變數中。</span><span class="sxs-lookup"><span data-stu-id="475f1-113">The command stores the local endpoint in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="475f1-114">第二個命令會將 IP 位址範圍 1.2.3.4 5.6.7.8 至儲存在 $TrafficManagerEndpoint 的端點。</span><span class="sxs-lookup"><span data-stu-id="475f1-114">The second command adds the IP address range 1.2.3.4 to 5.6.7.8 to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="475f1-115">第三個命令會將 IP 位址範圍9.10.11.0 新增至儲存在 $TrafficManagerEndpoint 的端點。</span><span class="sxs-lookup"><span data-stu-id="475f1-115">The third command adds the IP address range 9.10.11.0 to 9.10.11.255 to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="475f1-116">第四個命令會驗證範圍是否與範圍的大小相符，然後將 IP 位址範圍12.13.14.0 新增至儲存在 $TrafficManagerEndpoint 中的端點。</span><span class="sxs-lookup"><span data-stu-id="475f1-116">The fourth command verifies that the scope matches the size of the range, then adds the IP address range 12.13.14.0 to 12.13.14.31 to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="475f1-117">第五個命令會將 IP 位址範圍15.16.17.18 新增至儲存在 $TrafficManagerEndpoint 的端點。</span><span class="sxs-lookup"><span data-stu-id="475f1-117">The fifth command adds the IP address range 15.16.17.18 to 15.16.17.18 to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="475f1-118">Final 命令會更新流量管理器中的端點，以符合 $TrafficManagerEndpoint 中的本機值。</span><span class="sxs-lookup"><span data-stu-id="475f1-118">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="475f1-119">參數</span><span class="sxs-lookup"><span data-stu-id="475f1-119">PARAMETERS</span></span>

### <span data-ttu-id="475f1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="475f1-120">-DefaultProfile</span></span>
<span data-ttu-id="475f1-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="475f1-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="475f1-122">-上次</span><span class="sxs-lookup"><span data-stu-id="475f1-122">-Last</span></span>
<span data-ttu-id="475f1-123">指定要新增範圍中的最後一個 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="475f1-123">Specifies the last IP address in the range to be added.</span></span>

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

### <span data-ttu-id="475f1-124">-範圍</span><span class="sxs-lookup"><span data-stu-id="475f1-124">-Scope</span></span>
<span data-ttu-id="475f1-125">指定要新增之 IP 位址範圍的範圍。</span><span class="sxs-lookup"><span data-stu-id="475f1-125">Specifies the scope of the IP address range to be added.</span></span>

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

### <span data-ttu-id="475f1-126">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="475f1-126">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="475f1-127">指定本機 **TrafficManagerEndpoint** 物件。</span><span class="sxs-lookup"><span data-stu-id="475f1-127">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="475f1-128">這個 Cmdlet 會修改這個本機物件。</span><span class="sxs-lookup"><span data-stu-id="475f1-128">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="475f1-129">若要取得 **TrafficManagerEndpoint** 物件，請使用 Get-AzureRmTrafficManagerEndpoint 或 New-AzureRmTrafficManagerEndpoint Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="475f1-129">To obtain a **TrafficManagerEndpoint** object, use the Get-AzureRmTrafficManagerEndpoint or New-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="475f1-130">-確認</span><span class="sxs-lookup"><span data-stu-id="475f1-130">-Confirm</span></span>
<span data-ttu-id="475f1-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="475f1-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="475f1-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="475f1-132">-WhatIf</span></span>
<span data-ttu-id="475f1-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="475f1-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="475f1-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="475f1-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="475f1-135">-優先</span><span class="sxs-lookup"><span data-stu-id="475f1-135">-First</span></span>
<span data-ttu-id="475f1-136">指定要新增範圍中的第一個 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="475f1-136">Specifies the first IP address in the range to be added.</span></span>

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

### <span data-ttu-id="475f1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="475f1-137">CommonParameters</span></span>
<span data-ttu-id="475f1-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="475f1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="475f1-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="475f1-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="475f1-140">輸入</span><span class="sxs-lookup"><span data-stu-id="475f1-140">INPUTS</span></span>

### <span data-ttu-id="475f1-141">TrafficManagerEndpoint （）</span><span class="sxs-lookup"><span data-stu-id="475f1-141">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="475f1-142">這個 Cmdlet 接受 **TrafficManagerEndpoint** 物件到這個 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="475f1-142">This cmdlet accepts a **TrafficManagerEndpoint** object to this cmdlet.</span></span>

## <span data-ttu-id="475f1-143">輸出</span><span class="sxs-lookup"><span data-stu-id="475f1-143">OUTPUTS</span></span>

### <span data-ttu-id="475f1-144">TrafficManagerEndpoint （）</span><span class="sxs-lookup"><span data-stu-id="475f1-144">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="475f1-145">這個 Cmdlet 會傳回修改過的 **TrafficManagerEndpoint** 物件。</span><span class="sxs-lookup"><span data-stu-id="475f1-145">This cmdlet returns a modified **TrafficManagerEndpoint** object.</span></span>

## <span data-ttu-id="475f1-146">筆記</span><span class="sxs-lookup"><span data-stu-id="475f1-146">NOTES</span></span>

## <span data-ttu-id="475f1-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="475f1-147">RELATED LINKS</span></span>

[<span data-ttu-id="475f1-148">移除-AzureRmTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="475f1-148">Remove-AzureRmTrafficManagerIpAddressRange</span></span>](./Remove-AzureRmTrafficManagerIpAddressRange.md)

[<span data-ttu-id="475f1-149">新-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="475f1-149">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="475f1-150">AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="475f1-150">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="475f1-151">Set-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="475f1-151">Set-AzureRmTrafficManagerEndpoint</span></span>](./Set-AzureRmTrafficManagerEndpoint.md)
