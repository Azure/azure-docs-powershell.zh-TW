---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33E
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagercustomheadertoendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToEndpoint.md
ms.openlocfilehash: 9a1be7c45c507746ae3b8c97f883a61de0da78db
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957599"
---
# <span data-ttu-id="d2c68-101">Add-AzTrafficManagerCustomHeaderToEndpoint</span><span class="sxs-lookup"><span data-stu-id="d2c68-101">Add-AzTrafficManagerCustomHeaderToEndpoint</span></span>

## <span data-ttu-id="d2c68-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d2c68-102">SYNOPSIS</span></span>
<span data-ttu-id="d2c68-103">將自訂標頭資訊新增到本機流量管理器端點物件。</span><span class="sxs-lookup"><span data-stu-id="d2c68-103">Adds custom header information to a local Traffic Manager endpoint object.</span></span>

## <span data-ttu-id="d2c68-104">句法</span><span class="sxs-lookup"><span data-stu-id="d2c68-104">SYNTAX</span></span>

```
Add-AzTrafficManagerCustomHeaderToEndpoint -Name <String> -Value <String>
 -TrafficManagerEndpoint <TrafficManagerEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2c68-105">說明</span><span class="sxs-lookup"><span data-stu-id="d2c68-105">DESCRIPTION</span></span>
<span data-ttu-id="d2c68-106">**載入 AzTrafficManagerCustomHeaderToEndpoint** Cmdlet 會將自訂標頭資訊新增到本機 Azure 流量管理器端點物件。</span><span class="sxs-lookup"><span data-stu-id="d2c68-106">The **Add-AzTrafficManagerCustomHeaderToEndpoint** cmdlet adds custom header information to a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="d2c68-107">您可以使用 New-AzTrafficManagerEndpoint 或 Get-AzTrafficManagerEndpoint Cmdlet 來取得端點。</span><span class="sxs-lookup"><span data-stu-id="d2c68-107">You can get an endpoint by using the New-AzTrafficManagerEndpoint or Get-AzTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="d2c68-108">這個 Cmdlet 作用於本機端點物件。</span><span class="sxs-lookup"><span data-stu-id="d2c68-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="d2c68-109">使用 Set-AzTrafficManagerEndpoint Cmdlet，將您的變更提交至流量管理器的端點。</span><span class="sxs-lookup"><span data-stu-id="d2c68-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="d2c68-110">示例</span><span class="sxs-lookup"><span data-stu-id="d2c68-110">EXAMPLES</span></span>

### <span data-ttu-id="d2c68-111">範例1：將自訂標頭資訊新增到端點</span><span class="sxs-lookup"><span data-stu-id="d2c68-111">Example 1: Add custom header information to an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
PS C:\> Add-AzTrafficManagerCustomHeaderToEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint -Name "host" -Value "www.contoso.com"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="d2c68-112">第一個命令會使用 **AzTrafficManagerEndpoint** Cmdlet 來建立 Azure 流量管理器端點。</span><span class="sxs-lookup"><span data-stu-id="d2c68-112">The first command creates an Azure Traffic Manager endpoint by using the **New-AzTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="d2c68-113">該命令會將本機端點儲存在 $TrafficManagerEndpoint 變數中。</span><span class="sxs-lookup"><span data-stu-id="d2c68-113">The command stores the local endpoint in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="d2c68-114">第二個命令會將自訂標頭資訊新增至儲存在 $TrafficManagerEndpoint 中的端點。</span><span class="sxs-lookup"><span data-stu-id="d2c68-114">The second command adds custom header information to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="d2c68-115">Final 命令會更新流量管理器中的端點，以符合 $TrafficManagerEndpoint 中的本機值。</span><span class="sxs-lookup"><span data-stu-id="d2c68-115">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="d2c68-116">參數</span><span class="sxs-lookup"><span data-stu-id="d2c68-116">PARAMETERS</span></span>

### <span data-ttu-id="d2c68-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2c68-117">-DefaultProfile</span></span>
<span data-ttu-id="d2c68-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d2c68-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2c68-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="d2c68-119">-Name</span></span>
<span data-ttu-id="d2c68-120">指定要新增之自訂標頭資訊的名稱。</span><span class="sxs-lookup"><span data-stu-id="d2c68-120">Specifies the name of the custom header information to be added.</span></span>

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

### <span data-ttu-id="d2c68-121">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d2c68-121">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="d2c68-122">指定本機 **TrafficManagerEndpoint** 物件。</span><span class="sxs-lookup"><span data-stu-id="d2c68-122">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="d2c68-123">這個 Cmdlet 會修改這個本機物件。</span><span class="sxs-lookup"><span data-stu-id="d2c68-123">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="d2c68-124">若要取得 **TrafficManagerEndpoint** 物件，請使用 Get-AzTrafficManagerEndpoint 或 New-AzTrafficManagerEndpoint Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d2c68-124">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint or New-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="d2c68-125">-值</span><span class="sxs-lookup"><span data-stu-id="d2c68-125">-Value</span></span>
<span data-ttu-id="d2c68-126">指定要新增之自訂標頭資訊的值。</span><span class="sxs-lookup"><span data-stu-id="d2c68-126">Specifies the value of the custom header information to be added.</span></span>

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

### <span data-ttu-id="d2c68-127">-確認</span><span class="sxs-lookup"><span data-stu-id="d2c68-127">-Confirm</span></span>
<span data-ttu-id="d2c68-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d2c68-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2c68-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2c68-129">-WhatIf</span></span>
<span data-ttu-id="d2c68-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d2c68-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d2c68-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d2c68-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2c68-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2c68-132">CommonParameters</span></span>
<span data-ttu-id="d2c68-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d2c68-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2c68-134">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d2c68-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2c68-135">輸入</span><span class="sxs-lookup"><span data-stu-id="d2c68-135">INPUTS</span></span>

### <span data-ttu-id="d2c68-136">TrafficManagerEndpoint 中的 TrafficManager。</span><span class="sxs-lookup"><span data-stu-id="d2c68-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="d2c68-137">輸出</span><span class="sxs-lookup"><span data-stu-id="d2c68-137">OUTPUTS</span></span>

### <span data-ttu-id="d2c68-138">TrafficManagerEndpoint 中的 TrafficManager。</span><span class="sxs-lookup"><span data-stu-id="d2c68-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="d2c68-139">筆記</span><span class="sxs-lookup"><span data-stu-id="d2c68-139">NOTES</span></span>

## <span data-ttu-id="d2c68-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="d2c68-140">RELATED LINKS</span></span>

[<span data-ttu-id="d2c68-141">移除-AzTrafficManagerCustomHeaderFromEndpoint</span><span class="sxs-lookup"><span data-stu-id="d2c68-141">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span></span>](./Remove-AzTrafficManagerCustomHeaderFromEndpoint.md)

[<span data-ttu-id="d2c68-142">新-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d2c68-142">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="d2c68-143">AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d2c68-143">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="d2c68-144">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d2c68-144">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)
