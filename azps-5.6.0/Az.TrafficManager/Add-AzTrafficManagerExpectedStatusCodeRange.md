---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D340
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/add-aztrafficmanagerexpectedstatuscoderange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerExpectedStatusCodeRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerExpectedStatusCodeRange.md
ms.openlocfilehash: 88755e6830342dc7636bdb0b338269c47bc23398
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910874"
---
# <span data-ttu-id="151a2-101">Add-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="151a2-101">Add-AzTrafficManagerExpectedStatusCodeRange</span></span>

## <span data-ttu-id="151a2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="151a2-102">SYNOPSIS</span></span>
<span data-ttu-id="151a2-103">將預期的狀態碼範圍新增到本地流量管理員設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="151a2-103">Adds an expected status code range to a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="151a2-104">語法</span><span class="sxs-lookup"><span data-stu-id="151a2-104">SYNTAX</span></span>

```
Add-AzTrafficManagerExpectedStatusCodeRange -Min <Int32> -Max <Int32>
 -TrafficManagerProfile <TrafficManagerProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="151a2-105">描述</span><span class="sxs-lookup"><span data-stu-id="151a2-105">DESCRIPTION</span></span>
<span data-ttu-id="151a2-106">**Add-AzTrafficManagerExpectedStatusCodeRange** Cmdlet 會將一系列預期的狀態碼新增到本地 Azure Traffic Manager 設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="151a2-106">The **Add-AzTrafficManagerExpectedStatusCodeRange** cmdlet adds a range of expected status codes to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="151a2-107">您可以使用 Cmdlet 或 Cmdlet New-AzTrafficManagerProfile或Get-AzTrafficManagerProfile設定檔。</span><span class="sxs-lookup"><span data-stu-id="151a2-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="151a2-108">此 Cmdlet 可在本地設定檔物件上操作。</span><span class="sxs-lookup"><span data-stu-id="151a2-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="151a2-109">使用 Cmdlet 來針對流量管理員的設定檔Set-AzTrafficManagerProfile變更。</span><span class="sxs-lookup"><span data-stu-id="151a2-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="151a2-110">例子</span><span class="sxs-lookup"><span data-stu-id="151a2-110">EXAMPLES</span></span>

### <span data-ttu-id="151a2-111">範例 1：新增預期狀態碼範圍至設定檔</span><span class="sxs-lookup"><span data-stu-id="151a2-111">Example 1: Add an expected status code range to a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzTrafficManagerExpectedStatusCodeRange -TrafficManagerProfile $TrafficManagerProfile -Min 200 -Max 499
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="151a2-112">第一個命令會使用 **Get-AzTrafficManagerProfile** Cmdlet 取得 Azure 流量管理員設定檔。</span><span class="sxs-lookup"><span data-stu-id="151a2-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="151a2-113">該命令將本地設定檔儲存在 $TrafficManagerProfile 變數中。</span><span class="sxs-lookup"><span data-stu-id="151a2-113">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>
<span data-ttu-id="151a2-114">第二個命令會將預期的狀態碼範圍新增到儲存在 $TrafficManagerProfile 中的設定檔。</span><span class="sxs-lookup"><span data-stu-id="151a2-114">The second command adds an expected status code range to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="151a2-115">最後一個命令會更新 Traffic Manager 中的設定檔，以符合 $TrafficManagerProfile。</span><span class="sxs-lookup"><span data-stu-id="151a2-115">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="151a2-116">參數</span><span class="sxs-lookup"><span data-stu-id="151a2-116">PARAMETERS</span></span>

### <span data-ttu-id="151a2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="151a2-117">-DefaultProfile</span></span>
<span data-ttu-id="151a2-118">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="151a2-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="151a2-119">-最大值</span><span class="sxs-lookup"><span data-stu-id="151a2-119">-Max</span></span>
<span data-ttu-id="151a2-120">指定要新增的狀態碼範圍中的最高值。</span><span class="sxs-lookup"><span data-stu-id="151a2-120">Specifies the highest value in the status code range to be added.</span></span>

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

### <span data-ttu-id="151a2-121">-Min</span><span class="sxs-lookup"><span data-stu-id="151a2-121">-Min</span></span>
<span data-ttu-id="151a2-122">指定要新增的狀態碼範圍中的最低值。</span><span class="sxs-lookup"><span data-stu-id="151a2-122">Specifies the lowest value in the status code range to be added.</span></span>

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

### <span data-ttu-id="151a2-123">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="151a2-123">-TrafficManagerProfile</span></span>
<span data-ttu-id="151a2-124">指定一個本地 **TrafficManagerProfile** 物件。</span><span class="sxs-lookup"><span data-stu-id="151a2-124">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="151a2-125">此 Cmdlet 會修改此本機物件。</span><span class="sxs-lookup"><span data-stu-id="151a2-125">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="151a2-126">若要取得 **TrafficManagerProfile** 物件，請使用 Get-AzTrafficManagerProfile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="151a2-126">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="151a2-127">-確認</span><span class="sxs-lookup"><span data-stu-id="151a2-127">-Confirm</span></span>
<span data-ttu-id="151a2-128">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="151a2-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="151a2-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="151a2-129">-WhatIf</span></span>
<span data-ttu-id="151a2-130">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="151a2-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="151a2-131">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="151a2-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="151a2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="151a2-132">CommonParameters</span></span>
<span data-ttu-id="151a2-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="151a2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="151a2-134">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="151a2-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="151a2-135">輸入</span><span class="sxs-lookup"><span data-stu-id="151a2-135">INPUTS</span></span>

### <span data-ttu-id="151a2-136">Microsoft.Azure.Commands.TrafficManager.models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="151a2-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="151a2-137">輸出</span><span class="sxs-lookup"><span data-stu-id="151a2-137">OUTPUTS</span></span>

### <span data-ttu-id="151a2-138">Microsoft.Azure.Commands.TrafficManager.models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="151a2-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="151a2-139">筆記</span><span class="sxs-lookup"><span data-stu-id="151a2-139">NOTES</span></span>

## <span data-ttu-id="151a2-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="151a2-140">RELATED LINKS</span></span>

[<span data-ttu-id="151a2-141">Remove-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="151a2-141">Remove-AzTrafficManagerExpectedStatusCodeRange</span></span>](./Remove-AzTrafficManagerExpectedStatusCodeRange.md)

[<span data-ttu-id="151a2-142">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="151a2-142">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="151a2-143">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="151a2-143">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)
