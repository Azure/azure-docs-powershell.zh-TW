---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D340
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/add-azurertmtrafficmanagerexpectedstatuscoderange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerExpectedStatusCodeRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerExpectedStatusCodeRange.md
ms.openlocfilehash: 32a00a6dce3d6a370f7b7f79f05794a312277a09
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93443639"
---
# <span data-ttu-id="47ebc-101">Add-AzureRmTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="47ebc-101">Add-AzureRmTrafficManagerExpectedStatusCodeRange</span></span>

## <span data-ttu-id="47ebc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="47ebc-102">SYNOPSIS</span></span>
<span data-ttu-id="47ebc-103">將預期狀態碼範圍新增至本機流量管理器設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="47ebc-103">Adds an expected status code range to a local Traffic Manager profile object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47ebc-104">句法</span><span class="sxs-lookup"><span data-stu-id="47ebc-104">SYNTAX</span></span>

```
Add-AzureRmTrafficManagerExpectedStatusCodeRange -Min <Int32> -Max <Int32>
 -TrafficManagerProfile <TrafficManagerProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="47ebc-105">說明</span><span class="sxs-lookup"><span data-stu-id="47ebc-105">DESCRIPTION</span></span>
<span data-ttu-id="47ebc-106">**AzureRmTrafficManagerExpectedStatusCodeRange** Cmdlet 會將一系列預期的狀態碼新增到本機 Azure 流量管理器設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="47ebc-106">The **Add-AzureRmTrafficManagerExpectedStatusCodeRange** cmdlet adds a range of expected status codes to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="47ebc-107">您可以使用 New-AzureRmTrafficManagerProfile 或 Get-AzureRmTrafficManagerProfile Cmdlet 來取得設定檔。</span><span class="sxs-lookup"><span data-stu-id="47ebc-107">You can get a profile by using the New-AzureRmTrafficManagerProfile or Get-AzureRmTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="47ebc-108">這個 Cmdlet 作用於本機設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="47ebc-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="47ebc-109">使用 Set-AzureRmTrafficManagerProfile Cmdlet，將您的變更提交至流量管理器的設定檔。</span><span class="sxs-lookup"><span data-stu-id="47ebc-109">Commit your changes to the profile for Traffic Manager by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="47ebc-110">示例</span><span class="sxs-lookup"><span data-stu-id="47ebc-110">EXAMPLES</span></span>

### <span data-ttu-id="47ebc-111">範例1：在設定檔中新增預期的狀態碼範圍</span><span class="sxs-lookup"><span data-stu-id="47ebc-111">Example 1: Add an expected status code range to a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzureRmTrafficManagerExpectedStatusCodeRange -TrafficManagerProfile $TrafficManagerProfile -Min 200 -Max 499
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="47ebc-112">第一個命令會使用 **AzureRmTrafficManagerProfile** Cmdlet 取得 Azure 流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="47ebc-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzureRmTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="47ebc-113">該命令會將本機設定檔儲存在 $TrafficManagerProfile 變數中。</span><span class="sxs-lookup"><span data-stu-id="47ebc-113">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>
<span data-ttu-id="47ebc-114">第二個命令會將預期的狀態碼範圍新增至儲存在 $TrafficManagerProfile 中的設定檔。</span><span class="sxs-lookup"><span data-stu-id="47ebc-114">The second command adds an expected status code range to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="47ebc-115">最後一個命令會更新流量管理器中的設定檔，以符合 $TrafficManagerProfile 中的本機值。</span><span class="sxs-lookup"><span data-stu-id="47ebc-115">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="47ebc-116">參數</span><span class="sxs-lookup"><span data-stu-id="47ebc-116">PARAMETERS</span></span>

### <span data-ttu-id="47ebc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47ebc-117">-DefaultProfile</span></span>
<span data-ttu-id="47ebc-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="47ebc-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47ebc-119">-Max</span><span class="sxs-lookup"><span data-stu-id="47ebc-119">-Max</span></span>
<span data-ttu-id="47ebc-120">指定要新增之狀態碼範圍中的最大值。</span><span class="sxs-lookup"><span data-stu-id="47ebc-120">Specifies the highest value in the status code range to be added.</span></span>

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

### <span data-ttu-id="47ebc-121">-Min</span><span class="sxs-lookup"><span data-stu-id="47ebc-121">-Min</span></span>
<span data-ttu-id="47ebc-122">指定要新增之狀態碼範圍中的最小值。</span><span class="sxs-lookup"><span data-stu-id="47ebc-122">Specifies the lowest value in the status code range to be added.</span></span>

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

### <span data-ttu-id="47ebc-123">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="47ebc-123">-TrafficManagerProfile</span></span>
<span data-ttu-id="47ebc-124">指定本機 **TrafficManagerProfile** 物件。</span><span class="sxs-lookup"><span data-stu-id="47ebc-124">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="47ebc-125">這個 Cmdlet 會修改這個本機物件。</span><span class="sxs-lookup"><span data-stu-id="47ebc-125">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="47ebc-126">若要取得 **TrafficManagerProfile** 物件，請使用 Get-AzureRmTrafficManagerProfile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="47ebc-126">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="47ebc-127">-確認</span><span class="sxs-lookup"><span data-stu-id="47ebc-127">-Confirm</span></span>
<span data-ttu-id="47ebc-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="47ebc-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47ebc-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47ebc-129">-WhatIf</span></span>
<span data-ttu-id="47ebc-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="47ebc-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="47ebc-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="47ebc-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47ebc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47ebc-132">CommonParameters</span></span>
<span data-ttu-id="47ebc-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="47ebc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47ebc-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="47ebc-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47ebc-135">輸入</span><span class="sxs-lookup"><span data-stu-id="47ebc-135">INPUTS</span></span>

### <span data-ttu-id="47ebc-136">TrafficManagerProfile （）</span><span class="sxs-lookup"><span data-stu-id="47ebc-136">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="47ebc-137">這個 Cmdlet 接受 **TrafficManagerProfile** 物件到這個 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="47ebc-137">This cmdlet accepts a **TrafficManagerProfile** object to this cmdlet.</span></span>

## <span data-ttu-id="47ebc-138">輸出</span><span class="sxs-lookup"><span data-stu-id="47ebc-138">OUTPUTS</span></span>

### <span data-ttu-id="47ebc-139">TrafficManagerProfile （）</span><span class="sxs-lookup"><span data-stu-id="47ebc-139">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="47ebc-140">這個 Cmdlet 會傳回修改過的 **TrafficManagerProfile** 物件。</span><span class="sxs-lookup"><span data-stu-id="47ebc-140">This cmdlet returns a modified **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="47ebc-141">筆記</span><span class="sxs-lookup"><span data-stu-id="47ebc-141">NOTES</span></span>

## <span data-ttu-id="47ebc-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="47ebc-142">RELATED LINKS</span></span>

[<span data-ttu-id="47ebc-143">移除-AzureRmTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="47ebc-143">Remove-AzureRmTrafficManagerExpectedStatusCodeRange</span></span>](./Remove-AzureRmTrafficManagerExpectedStatusCodeRange.md)

[<span data-ttu-id="47ebc-144">AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="47ebc-144">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="47ebc-145">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="47ebc-145">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)
