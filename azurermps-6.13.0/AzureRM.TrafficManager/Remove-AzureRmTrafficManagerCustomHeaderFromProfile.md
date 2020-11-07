---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D343
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/remove-azurermtrafficmanagercustomheaderfromprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerCustomHeaderFromProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerCustomHeaderFromProfile.md
ms.openlocfilehash: af18a5a93cf08fe4806af429aee667b569c527d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626028"
---
# <span data-ttu-id="a9874-101">Remove-AzureRmTrafficManagerCustomHeaderFromProfile</span><span class="sxs-lookup"><span data-stu-id="a9874-101">Remove-AzureRmTrafficManagerCustomHeaderFromProfile</span></span>

## <span data-ttu-id="a9874-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a9874-102">SYNOPSIS</span></span>
<span data-ttu-id="a9874-103">從本機流量管理器設定檔物件移除自訂標頭資訊。</span><span class="sxs-lookup"><span data-stu-id="a9874-103">Removes custom header information from a local Traffic Manager profile object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9874-104">句法</span><span class="sxs-lookup"><span data-stu-id="a9874-104">SYNTAX</span></span>

```
Remove-AzureRmTrafficManagerCustomHeaderFromProfile -Name <String>
 -TrafficManagerProfile <TrafficManagerProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a9874-105">說明</span><span class="sxs-lookup"><span data-stu-id="a9874-105">DESCRIPTION</span></span>
<span data-ttu-id="a9874-106">**AzureRmTrafficManagerCustomHeaderFromProfile** Cmdlet 會從本機 Azure 流量管理器設定檔物件中移除自訂標頭資訊。</span><span class="sxs-lookup"><span data-stu-id="a9874-106">The **Remove-AzureRmTrafficManagerCustomHeaderFromProfile** cmdlet removes custom header information from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="a9874-107">您可以使用 New-AzureRmTrafficManagerProfile 或 Get-AzureRmTrafficManagerProfile Cmdlet 來取得設定檔。</span><span class="sxs-lookup"><span data-stu-id="a9874-107">You can get a profile by using the New-AzureRmTrafficManagerProfile or Get-AzureRmTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="a9874-108">這個 Cmdlet 作用於本機設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="a9874-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="a9874-109">使用 Set-AzureRmTrafficManagerProfile Cmdlet，將您的變更提交至流量管理器的設定檔。</span><span class="sxs-lookup"><span data-stu-id="a9874-109">Commit your changes to the profile for Traffic Manager by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="a9874-110">示例</span><span class="sxs-lookup"><span data-stu-id="a9874-110">EXAMPLES</span></span>

### <span data-ttu-id="a9874-111">範例1：移除設定檔中的自訂頁首資訊</span><span class="sxs-lookup"><span data-stu-id="a9874-111">Example 1: Remove custom header information from a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint -TrafficManagerProfile $TrafficManagerProfile -Name "host"
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="a9874-112">第一個命令會使用 **AzureRmTrafficManagerProfile** Cmdlet 取得 Azure 流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="a9874-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzureRmTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="a9874-113">第二個命令會從儲存在 $TrafficManagerProfile 的設定檔中移除自訂標題資訊。</span><span class="sxs-lookup"><span data-stu-id="a9874-113">The second command removes custom header information from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="a9874-114">最後一個命令會更新流量管理器中的設定檔，以符合 $TrafficManagerProfile 中的本機值。</span><span class="sxs-lookup"><span data-stu-id="a9874-114">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="a9874-115">參數</span><span class="sxs-lookup"><span data-stu-id="a9874-115">PARAMETERS</span></span>

### <span data-ttu-id="a9874-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9874-116">-DefaultProfile</span></span>
<span data-ttu-id="a9874-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a9874-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9874-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="a9874-118">-Name</span></span>
<span data-ttu-id="a9874-119">指定要移除的自訂標頭資訊的名稱。</span><span class="sxs-lookup"><span data-stu-id="a9874-119">Specifies the name of the custom header information to be removed.</span></span>

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

### <span data-ttu-id="a9874-120">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a9874-120">-TrafficManagerProfile</span></span>
<span data-ttu-id="a9874-121">指定本機 **TrafficManagerProfile** 物件。</span><span class="sxs-lookup"><span data-stu-id="a9874-121">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="a9874-122">這個 Cmdlet 會修改這個本機物件。</span><span class="sxs-lookup"><span data-stu-id="a9874-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="a9874-123">若要取得 **TrafficManagerProfile** 物件，請使用 Get-AzureRmTrafficManagerProfile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a9874-123">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="a9874-124">-確認</span><span class="sxs-lookup"><span data-stu-id="a9874-124">-Confirm</span></span>
<span data-ttu-id="a9874-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a9874-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9874-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9874-126">-WhatIf</span></span>
<span data-ttu-id="a9874-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a9874-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a9874-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a9874-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9874-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9874-129">CommonParameters</span></span>
<span data-ttu-id="a9874-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a9874-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9874-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a9874-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9874-132">輸入</span><span class="sxs-lookup"><span data-stu-id="a9874-132">INPUTS</span></span>

### <span data-ttu-id="a9874-133">TrafficManagerProfile （）</span><span class="sxs-lookup"><span data-stu-id="a9874-133">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="a9874-134">這個 Cmdlet 接受 **TrafficManagerProfile** 物件到這個 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a9874-134">This cmdlet accepts a **TrafficManagerProfile** object to this cmdlet.</span></span>

## <span data-ttu-id="a9874-135">輸出</span><span class="sxs-lookup"><span data-stu-id="a9874-135">OUTPUTS</span></span>

### <span data-ttu-id="a9874-136">TrafficManagerProfile （）</span><span class="sxs-lookup"><span data-stu-id="a9874-136">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="a9874-137">這個 Cmdlet 會傳回修改過的 **TrafficManagerProfile** 物件。</span><span class="sxs-lookup"><span data-stu-id="a9874-137">This cmdlet returns a modified **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="a9874-138">筆記</span><span class="sxs-lookup"><span data-stu-id="a9874-138">NOTES</span></span>

## <span data-ttu-id="a9874-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="a9874-139">RELATED LINKS</span></span>

[<span data-ttu-id="a9874-140">附加 AzureRmTrafficManagerCustomHeaderToProfile</span><span class="sxs-lookup"><span data-stu-id="a9874-140">Add-AzureRmTrafficManagerCustomHeaderToProfile</span></span>](./Add-AzureRmTrafficManagerCustomHeaderToProfile.md)

[<span data-ttu-id="a9874-141">AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a9874-141">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="a9874-142">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a9874-142">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)
