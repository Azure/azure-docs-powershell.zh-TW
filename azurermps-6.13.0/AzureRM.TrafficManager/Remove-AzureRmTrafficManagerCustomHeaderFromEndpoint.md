---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D342
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/remove-azurermtrafficmanagercustomheaderfromendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint.md
ms.openlocfilehash: 452e252b7bf9368ea89e81f2d37fd5a80ab079b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445347"
---
# <span data-ttu-id="190e9-101">Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint</span><span class="sxs-lookup"><span data-stu-id="190e9-101">Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint</span></span>

## <span data-ttu-id="190e9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="190e9-102">SYNOPSIS</span></span>
<span data-ttu-id="190e9-103">從本機流量管理器端點物件移除自訂標頭資訊。</span><span class="sxs-lookup"><span data-stu-id="190e9-103">Removes custom header information from a local Traffic Manager endpoint object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="190e9-104">句法</span><span class="sxs-lookup"><span data-stu-id="190e9-104">SYNTAX</span></span>

```
Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint -Name <String>
 -TrafficManagerEndpoint <TrafficManagerEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="190e9-105">說明</span><span class="sxs-lookup"><span data-stu-id="190e9-105">DESCRIPTION</span></span>
<span data-ttu-id="190e9-106">**AzureRmTrafficManagerCustomHeaderFromEndpoint** Cmdlet 會從本機 Azure 流量管理器端點物件中移除自訂標頭資訊。</span><span class="sxs-lookup"><span data-stu-id="190e9-106">The **Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint** cmdlet removes custom header information from a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="190e9-107">您可以使用 New-AzureRmTrafficManagerEndpoint 或 Get-AzureRmTrafficManagerEndpoint Cmdlet 來取得端點。</span><span class="sxs-lookup"><span data-stu-id="190e9-107">You can get an endpoint by using the New-AzureRmTrafficManagerEndpoint or Get-AzureRmTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="190e9-108">這個 Cmdlet 作用於本機端點物件。</span><span class="sxs-lookup"><span data-stu-id="190e9-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="190e9-109">使用 Set-AzureRmTrafficManagerEndpoint Cmdlet，將您的變更提交至流量管理器的端點。</span><span class="sxs-lookup"><span data-stu-id="190e9-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="190e9-110">示例</span><span class="sxs-lookup"><span data-stu-id="190e9-110">EXAMPLES</span></span>

### <span data-ttu-id="190e9-111">範例1：從端點中移除自訂子網資訊</span><span class="sxs-lookup"><span data-stu-id="190e9-111">Example 1: Remove custom subnet information from an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = Get-AzureRmTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
PS C:\> Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint -Name "host"
PS C:\> Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="190e9-112">第一個命令會從名為 ResourceGroup11 的資源群組中，從名為 contoso 的設定檔中取得名為 contoso 的 Azure 端點，然後將該物件儲存在 $TrafficManagerEndpoint 變數中。</span><span class="sxs-lookup"><span data-stu-id="190e9-112">The first command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="190e9-113">第二個命令會從儲存在 $TrafficManagerEndpoint 中的端點中移除自訂標頭資訊。</span><span class="sxs-lookup"><span data-stu-id="190e9-113">The second command removes custom header information from the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="190e9-114">Final 命令會更新流量管理器中的端點，以符合 $TrafficManagerEndpoint 中的本機值。</span><span class="sxs-lookup"><span data-stu-id="190e9-114">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="190e9-115">參數</span><span class="sxs-lookup"><span data-stu-id="190e9-115">PARAMETERS</span></span>

### <span data-ttu-id="190e9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="190e9-116">-DefaultProfile</span></span>
<span data-ttu-id="190e9-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="190e9-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="190e9-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="190e9-118">-Name</span></span>
<span data-ttu-id="190e9-119">指定要移除的自訂標頭資訊的名稱。</span><span class="sxs-lookup"><span data-stu-id="190e9-119">Specifies the name of the custom header information to be removed.</span></span>

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

### <span data-ttu-id="190e9-120">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="190e9-120">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="190e9-121">指定本機 **TrafficManagerEndpoint** 物件。</span><span class="sxs-lookup"><span data-stu-id="190e9-121">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="190e9-122">這個 Cmdlet 會修改這個本機物件。</span><span class="sxs-lookup"><span data-stu-id="190e9-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="190e9-123">若要取得 **TrafficManagerEndpoint** 物件，請使用 Get-AzureRmTrafficManagerEndpoint 或 New-AzureRmTrafficManagerEndpoint Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="190e9-123">To obtain a **TrafficManagerEndpoint** object, use the Get-AzureRmTrafficManagerEndpoint or New-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="190e9-124">-確認</span><span class="sxs-lookup"><span data-stu-id="190e9-124">-Confirm</span></span>
<span data-ttu-id="190e9-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="190e9-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="190e9-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="190e9-126">-WhatIf</span></span>
<span data-ttu-id="190e9-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="190e9-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="190e9-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="190e9-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="190e9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="190e9-129">CommonParameters</span></span>
<span data-ttu-id="190e9-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="190e9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="190e9-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="190e9-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="190e9-132">輸入</span><span class="sxs-lookup"><span data-stu-id="190e9-132">INPUTS</span></span>

### <span data-ttu-id="190e9-133">TrafficManagerEndpoint （）</span><span class="sxs-lookup"><span data-stu-id="190e9-133">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="190e9-134">這個 Cmdlet 接受 **TrafficManagerEndpoint** 物件到這個 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="190e9-134">This cmdlet accepts a **TrafficManagerEndpoint** object to this cmdlet.</span></span>

## <span data-ttu-id="190e9-135">輸出</span><span class="sxs-lookup"><span data-stu-id="190e9-135">OUTPUTS</span></span>

### <span data-ttu-id="190e9-136">TrafficManagerEndpoint （）</span><span class="sxs-lookup"><span data-stu-id="190e9-136">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="190e9-137">這個 Cmdlet 會傳回修改過的 TrafficManagerEndpoint 物件。</span><span class="sxs-lookup"><span data-stu-id="190e9-137">This cmdlet returns a modified TrafficManagerEndpoint object.</span></span>

## <span data-ttu-id="190e9-138">筆記</span><span class="sxs-lookup"><span data-stu-id="190e9-138">NOTES</span></span>

## <span data-ttu-id="190e9-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="190e9-139">RELATED LINKS</span></span>

[<span data-ttu-id="190e9-140">附加 AzureRmTrafficManagerCustomHeaderToEndpoint</span><span class="sxs-lookup"><span data-stu-id="190e9-140">Add-AzureRmTrafficManagerCustomHeaderToEndpoint</span></span>](./Add-AzureRmTrafficManagerCustomHeaderToEndpoint.md)

[<span data-ttu-id="190e9-141">AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="190e9-141">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="190e9-142">新-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="190e9-142">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="190e9-143">Set-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="190e9-143">Set-AzureRmTrafficManagerEndpoint</span></span>](./Set-AzureRmTrafficManagerEndpoint.md)
