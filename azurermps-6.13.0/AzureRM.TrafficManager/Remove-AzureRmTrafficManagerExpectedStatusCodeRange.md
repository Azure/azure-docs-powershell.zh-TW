---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D344
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/remove-azurermtrafficmanagerexpectedstatuscoderange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerExpectedStatusCodeRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerExpectedStatusCodeRange.md
ms.openlocfilehash: 0971a4b8d485c1590794de6f1b6c2d4d9d21da4a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445340"
---
# <span data-ttu-id="3a50d-101">Remove-AzureRmTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="3a50d-101">Remove-AzureRmTrafficManagerExpectedStatusCodeRange</span></span>

## <span data-ttu-id="3a50d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3a50d-102">SYNOPSIS</span></span>
<span data-ttu-id="3a50d-103">從本機流量管理器設定檔物件移除預期的狀態碼範圍。</span><span class="sxs-lookup"><span data-stu-id="3a50d-103">Removes an expected status code range from a local Traffic Manager profile object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a50d-104">句法</span><span class="sxs-lookup"><span data-stu-id="3a50d-104">SYNTAX</span></span>

```
Remove-AzureRmTrafficManagerExpectedStatusCodeRange -Min <Int32> -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a50d-105">說明</span><span class="sxs-lookup"><span data-stu-id="3a50d-105">DESCRIPTION</span></span>
<span data-ttu-id="3a50d-106">**AzureRmTrafficManagerExpectedStatusCodeRange** Cmdlet 會從本機 Azure 流量管理器設定檔物件移除一系列預期的狀態碼。</span><span class="sxs-lookup"><span data-stu-id="3a50d-106">The **Remove-AzureRmTrafficManagerExpectedStatusCodeRange** cmdlet removes a range of expected status codes from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="3a50d-107">您可以使用 New-AzureRmTrafficManagerProfile 或 Get-AzureRmTrafficManagerProfile Cmdlet 來取得設定檔。</span><span class="sxs-lookup"><span data-stu-id="3a50d-107">You can get a profile by using the New-AzureRmTrafficManagerProfile or Get-AzureRmTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="3a50d-108">這個 Cmdlet 作用於本機設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="3a50d-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="3a50d-109">使用 Set-AzureRmTrafficManagerProfile Cmdlet，將您的變更提交至流量管理器的設定檔。</span><span class="sxs-lookup"><span data-stu-id="3a50d-109">Commit your changes to the profile for Traffic Manager by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="3a50d-110">示例</span><span class="sxs-lookup"><span data-stu-id="3a50d-110">EXAMPLES</span></span>

### <span data-ttu-id="3a50d-111">範例1：從設定檔移除預期的狀態碼範圍</span><span class="sxs-lookup"><span data-stu-id="3a50d-111">Example 1: Remove an expected status code range from a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzureRmTrafficManagerExpectedStatusCodeRange -TrafficManagerProfile $TrafficManagerProfile -Min 200
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="3a50d-112">第一個命令會使用 **AzureRmTrafficManagerProfile** Cmdlet 取得 Azure 流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="3a50d-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzureRmTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="3a50d-113">第二個命令會將所儲存設定檔的預期狀態碼範圍從 $TrafficManagerProfile 中移除。</span><span class="sxs-lookup"><span data-stu-id="3a50d-113">The second command removes an expected status code range from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="3a50d-114">最後一個命令會更新流量管理器中的設定檔，以符合 $TrafficManagerProfile 中的本機值。</span><span class="sxs-lookup"><span data-stu-id="3a50d-114">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="3a50d-115">參數</span><span class="sxs-lookup"><span data-stu-id="3a50d-115">PARAMETERS</span></span>

### <span data-ttu-id="3a50d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a50d-116">-DefaultProfile</span></span>
<span data-ttu-id="3a50d-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3a50d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a50d-118">-Min</span><span class="sxs-lookup"><span data-stu-id="3a50d-118">-Min</span></span>
<span data-ttu-id="3a50d-119">指定要移除的狀態碼範圍中的最小值。</span><span class="sxs-lookup"><span data-stu-id="3a50d-119">Specifies the lowest value in the status code range to be removed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a50d-120">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3a50d-120">-TrafficManagerProfile</span></span>
<span data-ttu-id="3a50d-121">指定本機 **TrafficManagerProfile** 物件。</span><span class="sxs-lookup"><span data-stu-id="3a50d-121">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="3a50d-122">這個 Cmdlet 會修改這個本機物件。</span><span class="sxs-lookup"><span data-stu-id="3a50d-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="3a50d-123">若要取得 **TrafficManagerProfile** 物件，請使用 Get-AzureRmTrafficManagerProfile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3a50d-123">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="3a50d-124">-確認</span><span class="sxs-lookup"><span data-stu-id="3a50d-124">-Confirm</span></span>
<span data-ttu-id="3a50d-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3a50d-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a50d-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a50d-126">-WhatIf</span></span>
<span data-ttu-id="3a50d-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3a50d-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3a50d-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3a50d-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a50d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a50d-129">CommonParameters</span></span>
<span data-ttu-id="3a50d-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3a50d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a50d-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3a50d-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a50d-132">輸入</span><span class="sxs-lookup"><span data-stu-id="3a50d-132">INPUTS</span></span>

### <span data-ttu-id="3a50d-133">TrafficManagerProfile （）</span><span class="sxs-lookup"><span data-stu-id="3a50d-133">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="3a50d-134">這個 Cmdlet 接受 **TrafficManagerProfile** 物件到這個 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3a50d-134">This cmdlet accepts a **TrafficManagerProfile** object to this cmdlet.</span></span>

## <span data-ttu-id="3a50d-135">輸出</span><span class="sxs-lookup"><span data-stu-id="3a50d-135">OUTPUTS</span></span>

### <span data-ttu-id="3a50d-136">TrafficManagerProfile （）</span><span class="sxs-lookup"><span data-stu-id="3a50d-136">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="3a50d-137">這個 Cmdlet 會傳回修改過的 **TrafficManagerProfile** 物件。</span><span class="sxs-lookup"><span data-stu-id="3a50d-137">This cmdlet returns a modified **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="3a50d-138">筆記</span><span class="sxs-lookup"><span data-stu-id="3a50d-138">NOTES</span></span>

## <span data-ttu-id="3a50d-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="3a50d-139">RELATED LINKS</span></span>

[<span data-ttu-id="3a50d-140">附加 AzureRmTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="3a50d-140">Add-AzureRmTrafficManagerExpectedStatusCodeRange</span></span>](./Add-AzureRmTrafficManagerExpectedStatusCodeRange.md)

[<span data-ttu-id="3a50d-141">AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3a50d-141">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="3a50d-142">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3a50d-142">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)
