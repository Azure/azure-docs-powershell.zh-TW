---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/add-azurertmtrafficmanagercustomheadertoendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerCustomHeaderToEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerCustomHeaderToEndpoint.md
ms.openlocfilehash: a00eb5977ad1a58b12ad3f326d36dba8d083d718
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626029"
---
# <span data-ttu-id="cafa9-101">Add-AzureRmTrafficManagerCustomHeaderToEndpoint</span><span class="sxs-lookup"><span data-stu-id="cafa9-101">Add-AzureRmTrafficManagerCustomHeaderToEndpoint</span></span>

## <span data-ttu-id="cafa9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cafa9-102">SYNOPSIS</span></span>
<span data-ttu-id="cafa9-103">將自訂標頭資訊新增到本機流量管理器端點物件。</span><span class="sxs-lookup"><span data-stu-id="cafa9-103">Adds custom header information to a local Traffic Manager endpoint object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cafa9-104">句法</span><span class="sxs-lookup"><span data-stu-id="cafa9-104">SYNTAX</span></span>

```
Add-AzureRmTrafficManagerCustomHeaderToEndpoint -Name <String> -Value <String>
 -TrafficManagerEndpoint <TrafficManagerEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cafa9-105">說明</span><span class="sxs-lookup"><span data-stu-id="cafa9-105">DESCRIPTION</span></span>
<span data-ttu-id="cafa9-106">**載入 AzureRmTrafficManagerCustomHeaderToEndpoint** Cmdlet 會將自訂標頭資訊新增到本機 Azure 流量管理器端點物件。</span><span class="sxs-lookup"><span data-stu-id="cafa9-106">The **Add-AzureRmTrafficManagerCustomHeaderToEndpoint** cmdlet adds custom header information to a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="cafa9-107">您可以使用 New-AzureRmTrafficManagerEndpoint 或 Get-AzureRmTrafficManagerEndpoint Cmdlet 來取得端點。</span><span class="sxs-lookup"><span data-stu-id="cafa9-107">You can get an endpoint by using the New-AzureRmTrafficManagerEndpoint or Get-AzureRmTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="cafa9-108">這個 Cmdlet 作用於本機端點物件。</span><span class="sxs-lookup"><span data-stu-id="cafa9-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="cafa9-109">使用 Set-AzureRmTrafficManagerEndpoint Cmdlet，將您的變更提交至流量管理器的端點。</span><span class="sxs-lookup"><span data-stu-id="cafa9-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="cafa9-110">示例</span><span class="sxs-lookup"><span data-stu-id="cafa9-110">EXAMPLES</span></span>

### <span data-ttu-id="cafa9-111">範例1：將自訂標頭資訊新增到端點</span><span class="sxs-lookup"><span data-stu-id="cafa9-111">Example 1: Add custom header information to an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = New-AzureRmTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
PS C:\> Add-AzureRmTrafficManagerCustomHeaderToEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint -Name "host" -Value "www.contoso.com"
PS C:\> Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="cafa9-112">第一個命令會使用 **AzureRmTrafficManagerEndpoint** Cmdlet 來建立 Azure 流量管理器端點。</span><span class="sxs-lookup"><span data-stu-id="cafa9-112">The first command creates an Azure Traffic Manager endpoint by using the **New-AzureRmTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="cafa9-113">該命令會將本機端點儲存在 $TrafficManagerEndpoint 變數中。</span><span class="sxs-lookup"><span data-stu-id="cafa9-113">The command stores the local endpoint in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="cafa9-114">第二個命令會將自訂標頭資訊新增至儲存在 $TrafficManagerEndpoint 中的端點。</span><span class="sxs-lookup"><span data-stu-id="cafa9-114">The second command adds custom header information to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="cafa9-115">Final 命令會更新流量管理器中的端點，以符合 $TrafficManagerEndpoint 中的本機值。</span><span class="sxs-lookup"><span data-stu-id="cafa9-115">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="cafa9-116">參數</span><span class="sxs-lookup"><span data-stu-id="cafa9-116">PARAMETERS</span></span>

### <span data-ttu-id="cafa9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cafa9-117">-DefaultProfile</span></span>
<span data-ttu-id="cafa9-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cafa9-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cafa9-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="cafa9-119">-Name</span></span>
<span data-ttu-id="cafa9-120">指定要新增之自訂標頭資訊的名稱。</span><span class="sxs-lookup"><span data-stu-id="cafa9-120">Specifies the name of the custom header information to be added.</span></span>

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

### <span data-ttu-id="cafa9-121">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="cafa9-121">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="cafa9-122">指定本機 **TrafficManagerEndpoint** 物件。</span><span class="sxs-lookup"><span data-stu-id="cafa9-122">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="cafa9-123">這個 Cmdlet 會修改這個本機物件。</span><span class="sxs-lookup"><span data-stu-id="cafa9-123">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="cafa9-124">若要取得 **TrafficManagerEndpoint** 物件，請使用 Get-AzureRmTrafficManagerEndpoint 或 New-AzureRmTrafficManagerEndpoint Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cafa9-124">To obtain a **TrafficManagerEndpoint** object, use the Get-AzureRmTrafficManagerEndpoint or New-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="cafa9-125">-值</span><span class="sxs-lookup"><span data-stu-id="cafa9-125">-Value</span></span>
<span data-ttu-id="cafa9-126">指定要新增之自訂標頭資訊的值。</span><span class="sxs-lookup"><span data-stu-id="cafa9-126">Specifies the value of the custom header information to be added.</span></span>

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

### <span data-ttu-id="cafa9-127">-確認</span><span class="sxs-lookup"><span data-stu-id="cafa9-127">-Confirm</span></span>
<span data-ttu-id="cafa9-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cafa9-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cafa9-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cafa9-129">-WhatIf</span></span>
<span data-ttu-id="cafa9-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cafa9-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cafa9-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cafa9-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cafa9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cafa9-132">CommonParameters</span></span>
<span data-ttu-id="cafa9-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cafa9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cafa9-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cafa9-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cafa9-135">輸入</span><span class="sxs-lookup"><span data-stu-id="cafa9-135">INPUTS</span></span>

### <span data-ttu-id="cafa9-136">TrafficManagerEndpoint （）</span><span class="sxs-lookup"><span data-stu-id="cafa9-136">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="cafa9-137">這個 Cmdlet 接受 **TrafficManagerEndpoint** 物件到這個 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cafa9-137">This cmdlet accepts a **TrafficManagerEndpoint** object to this cmdlet.</span></span>

## <span data-ttu-id="cafa9-138">輸出</span><span class="sxs-lookup"><span data-stu-id="cafa9-138">OUTPUTS</span></span>

### <span data-ttu-id="cafa9-139">TrafficManagerEndpoint （）</span><span class="sxs-lookup"><span data-stu-id="cafa9-139">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="cafa9-140">這個 Cmdlet 會傳回修改過的 **TrafficManagerEndpoint** 物件。</span><span class="sxs-lookup"><span data-stu-id="cafa9-140">This cmdlet returns a modified **TrafficManagerEndpoint** object.</span></span>

## <span data-ttu-id="cafa9-141">筆記</span><span class="sxs-lookup"><span data-stu-id="cafa9-141">NOTES</span></span>

## <span data-ttu-id="cafa9-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="cafa9-142">RELATED LINKS</span></span>

[<span data-ttu-id="cafa9-143">移除-AzureRmTrafficManagerCustomHeaderFromEndpoint</span><span class="sxs-lookup"><span data-stu-id="cafa9-143">Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint</span></span>](./Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint.md)

[<span data-ttu-id="cafa9-144">新-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="cafa9-144">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="cafa9-145">AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="cafa9-145">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="cafa9-146">Set-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="cafa9-146">Set-AzureRmTrafficManagerEndpoint</span></span>](./Set-AzureRmTrafficManagerEndpoint.md)
