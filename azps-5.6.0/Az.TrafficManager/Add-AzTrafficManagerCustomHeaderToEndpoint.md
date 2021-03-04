---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33E
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/add-aztrafficmanagercustomheadertoendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToEndpoint.md
ms.openlocfilehash: 4a24953dd763c54cba7454bf9e46bb9373b0f450
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910882"
---
# <span data-ttu-id="52a0a-101">Add-AzTrafficManagerCustomHeaderToEndpoint</span><span class="sxs-lookup"><span data-stu-id="52a0a-101">Add-AzTrafficManagerCustomHeaderToEndpoint</span></span>

## <span data-ttu-id="52a0a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="52a0a-102">SYNOPSIS</span></span>
<span data-ttu-id="52a0a-103">新增自訂標頭資訊至本地流量管理員端點物件。</span><span class="sxs-lookup"><span data-stu-id="52a0a-103">Adds custom header information to a local Traffic Manager endpoint object.</span></span>

## <span data-ttu-id="52a0a-104">語法</span><span class="sxs-lookup"><span data-stu-id="52a0a-104">SYNTAX</span></span>

```
Add-AzTrafficManagerCustomHeaderToEndpoint -Name <String> -Value <String>
 -TrafficManagerEndpoint <TrafficManagerEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52a0a-105">描述</span><span class="sxs-lookup"><span data-stu-id="52a0a-105">DESCRIPTION</span></span>
<span data-ttu-id="52a0a-106">**Add-AzTrafficManagerCustomHeaderToEndpoint** Cmdlet 會新增自訂標頭資訊至本地 Azure 流量管理員端點物件。</span><span class="sxs-lookup"><span data-stu-id="52a0a-106">The **Add-AzTrafficManagerCustomHeaderToEndpoint** cmdlet adds custom header information to a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="52a0a-107">您可以使用 Cmdlet 或 Cmdlet New-AzTrafficManagerEndpoint端點Get-AzTrafficManagerEndpoint端點。</span><span class="sxs-lookup"><span data-stu-id="52a0a-107">You can get an endpoint by using the New-AzTrafficManagerEndpoint or Get-AzTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="52a0a-108">此 Cmdlet 在本地端點物件上操作。</span><span class="sxs-lookup"><span data-stu-id="52a0a-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="52a0a-109">使用 Cmdlet 來為流量管理員的端點Set-AzTrafficManagerEndpoint變更。</span><span class="sxs-lookup"><span data-stu-id="52a0a-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="52a0a-110">例子</span><span class="sxs-lookup"><span data-stu-id="52a0a-110">EXAMPLES</span></span>

### <span data-ttu-id="52a0a-111">範例 1：新增自訂頁眉資訊至端點</span><span class="sxs-lookup"><span data-stu-id="52a0a-111">Example 1: Add custom header information to an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
PS C:\> Add-AzTrafficManagerCustomHeaderToEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint -Name "host" -Value "www.contoso.com"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="52a0a-112">第一個命令會使用 **New-AzTrafficManagerEndpoint** Cmdlet 建立 Azure 流量管理員端點。</span><span class="sxs-lookup"><span data-stu-id="52a0a-112">The first command creates an Azure Traffic Manager endpoint by using the **New-AzTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="52a0a-113">該命令將本地端點儲存在 $TrafficManagerEndpoint 變數中。</span><span class="sxs-lookup"><span data-stu-id="52a0a-113">The command stores the local endpoint in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="52a0a-114">第二個命令會將自訂標題資訊新增到儲存在 $TrafficManagerEndpoint。</span><span class="sxs-lookup"><span data-stu-id="52a0a-114">The second command adds custom header information to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="52a0a-115">最後一個命令會更新 Traffic Manager 中的端點，以符合 $TrafficManagerEndpoint。</span><span class="sxs-lookup"><span data-stu-id="52a0a-115">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="52a0a-116">參數</span><span class="sxs-lookup"><span data-stu-id="52a0a-116">PARAMETERS</span></span>

### <span data-ttu-id="52a0a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52a0a-117">-DefaultProfile</span></span>
<span data-ttu-id="52a0a-118">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="52a0a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52a0a-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="52a0a-119">-Name</span></span>
<span data-ttu-id="52a0a-120">指定要新增之自訂標題資訊的名稱。</span><span class="sxs-lookup"><span data-stu-id="52a0a-120">Specifies the name of the custom header information to be added.</span></span>

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

### <span data-ttu-id="52a0a-121">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="52a0a-121">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="52a0a-122">指定一個本地 **TrafficManagerEndpoint** 物件。</span><span class="sxs-lookup"><span data-stu-id="52a0a-122">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="52a0a-123">此 Cmdlet 會修改此本機物件。</span><span class="sxs-lookup"><span data-stu-id="52a0a-123">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="52a0a-124">若要取得 **TrafficManagerEndpoint** 物件，請使用 Get-AzTrafficManagerEndpoint 或 New-AzTrafficManagerEndpoint Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="52a0a-124">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint or New-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="52a0a-125">-值</span><span class="sxs-lookup"><span data-stu-id="52a0a-125">-Value</span></span>
<span data-ttu-id="52a0a-126">指定要新增之自訂標題資訊的值。</span><span class="sxs-lookup"><span data-stu-id="52a0a-126">Specifies the value of the custom header information to be added.</span></span>

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

### <span data-ttu-id="52a0a-127">-確認</span><span class="sxs-lookup"><span data-stu-id="52a0a-127">-Confirm</span></span>
<span data-ttu-id="52a0a-128">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="52a0a-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52a0a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52a0a-129">-WhatIf</span></span>
<span data-ttu-id="52a0a-130">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="52a0a-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="52a0a-131">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="52a0a-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52a0a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52a0a-132">CommonParameters</span></span>
<span data-ttu-id="52a0a-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="52a0a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52a0a-134">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="52a0a-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52a0a-135">輸入</span><span class="sxs-lookup"><span data-stu-id="52a0a-135">INPUTS</span></span>

### <span data-ttu-id="52a0a-136">Microsoft.Azure.Commands.TrafficManager.models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="52a0a-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="52a0a-137">輸出</span><span class="sxs-lookup"><span data-stu-id="52a0a-137">OUTPUTS</span></span>

### <span data-ttu-id="52a0a-138">Microsoft.Azure.Commands.TrafficManager.models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="52a0a-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="52a0a-139">筆記</span><span class="sxs-lookup"><span data-stu-id="52a0a-139">NOTES</span></span>

## <span data-ttu-id="52a0a-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="52a0a-140">RELATED LINKS</span></span>

[<span data-ttu-id="52a0a-141">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span><span class="sxs-lookup"><span data-stu-id="52a0a-141">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span></span>](./Remove-AzTrafficManagerCustomHeaderFromEndpoint.md)

[<span data-ttu-id="52a0a-142">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="52a0a-142">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="52a0a-143">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="52a0a-143">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="52a0a-144">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="52a0a-144">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)
