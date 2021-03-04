---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D344
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/remove-aztrafficmanagerexpectedstatuscoderange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerExpectedStatusCodeRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerExpectedStatusCodeRange.md
ms.openlocfilehash: 8e79fe1a0d0cc1c681c88cb3d5dfdd8d48dfd26b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910841"
---
# <span data-ttu-id="cc8a6-101">Remove-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="cc8a6-101">Remove-AzTrafficManagerExpectedStatusCodeRange</span></span>

## <span data-ttu-id="cc8a6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="cc8a6-102">SYNOPSIS</span></span>
<span data-ttu-id="cc8a6-103">從本地流量管理員設定檔物件移除預期的狀態碼範圍。</span><span class="sxs-lookup"><span data-stu-id="cc8a6-103">Removes an expected status code range from a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="cc8a6-104">語法</span><span class="sxs-lookup"><span data-stu-id="cc8a6-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerExpectedStatusCodeRange -Min <Int32> -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc8a6-105">描述</span><span class="sxs-lookup"><span data-stu-id="cc8a6-105">DESCRIPTION</span></span>
<span data-ttu-id="cc8a6-106">**Remove-AzTrafficManagerExpectedStatusCodeRange** Cmdlet 會從一個本地 Azure Traffic Manager 設定檔物件移除一系列預期的狀態碼。</span><span class="sxs-lookup"><span data-stu-id="cc8a6-106">The **Remove-AzTrafficManagerExpectedStatusCodeRange** cmdlet removes a range of expected status codes from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="cc8a6-107">您可以使用 Cmdlet 或 Cmdlet New-AzTrafficManagerProfile或Get-AzTrafficManagerProfile設定檔。</span><span class="sxs-lookup"><span data-stu-id="cc8a6-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="cc8a6-108">此 Cmdlet 可在本地設定檔物件上操作。</span><span class="sxs-lookup"><span data-stu-id="cc8a6-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="cc8a6-109">使用 Cmdlet 來針對流量管理員的設定檔Set-AzTrafficManagerProfile變更。</span><span class="sxs-lookup"><span data-stu-id="cc8a6-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="cc8a6-110">例子</span><span class="sxs-lookup"><span data-stu-id="cc8a6-110">EXAMPLES</span></span>

### <span data-ttu-id="cc8a6-111">範例 1：從設定檔移除預期狀態碼範圍</span><span class="sxs-lookup"><span data-stu-id="cc8a6-111">Example 1: Remove an expected status code range from a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzTrafficManagerExpectedStatusCodeRange -TrafficManagerProfile $TrafficManagerProfile -Min 200
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="cc8a6-112">第一個命令會使用 **Get-AzTrafficManagerProfile** Cmdlet 取得 Azure 流量管理員設定檔。</span><span class="sxs-lookup"><span data-stu-id="cc8a6-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="cc8a6-113">第二個命令會從儲存在 $TrafficManagerProfile 中的設定檔移除預期狀態碼$TrafficManagerProfile。</span><span class="sxs-lookup"><span data-stu-id="cc8a6-113">The second command removes an expected status code range from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="cc8a6-114">最後一個命令會更新 Traffic Manager 中的設定檔，以符合 $TrafficManagerProfile。</span><span class="sxs-lookup"><span data-stu-id="cc8a6-114">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="cc8a6-115">參數</span><span class="sxs-lookup"><span data-stu-id="cc8a6-115">PARAMETERS</span></span>

### <span data-ttu-id="cc8a6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc8a6-116">-DefaultProfile</span></span>
<span data-ttu-id="cc8a6-117">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="cc8a6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc8a6-118">-Min</span><span class="sxs-lookup"><span data-stu-id="cc8a6-118">-Min</span></span>
<span data-ttu-id="cc8a6-119">指定要移除的狀態碼範圍中的最低值。</span><span class="sxs-lookup"><span data-stu-id="cc8a6-119">Specifies the lowest value in the status code range to be removed.</span></span>

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

### <span data-ttu-id="cc8a6-120">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="cc8a6-120">-TrafficManagerProfile</span></span>
<span data-ttu-id="cc8a6-121">指定一個本地 **TrafficManagerProfile** 物件。</span><span class="sxs-lookup"><span data-stu-id="cc8a6-121">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="cc8a6-122">此 Cmdlet 會修改此本機物件。</span><span class="sxs-lookup"><span data-stu-id="cc8a6-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="cc8a6-123">若要取得 **TrafficManagerProfile** 物件，請使用 Get-AzTrafficManagerProfile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cc8a6-123">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="cc8a6-124">-確認</span><span class="sxs-lookup"><span data-stu-id="cc8a6-124">-Confirm</span></span>
<span data-ttu-id="cc8a6-125">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="cc8a6-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc8a6-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc8a6-126">-WhatIf</span></span>
<span data-ttu-id="cc8a6-127">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cc8a6-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cc8a6-128">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cc8a6-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc8a6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc8a6-129">CommonParameters</span></span>
<span data-ttu-id="cc8a6-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="cc8a6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc8a6-131">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="cc8a6-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc8a6-132">輸入</span><span class="sxs-lookup"><span data-stu-id="cc8a6-132">INPUTS</span></span>

### <span data-ttu-id="cc8a6-133">Microsoft.Azure.Commands.TrafficManager.models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="cc8a6-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="cc8a6-134">輸出</span><span class="sxs-lookup"><span data-stu-id="cc8a6-134">OUTPUTS</span></span>

### <span data-ttu-id="cc8a6-135">Microsoft.Azure.Commands.TrafficManager.models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="cc8a6-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="cc8a6-136">筆記</span><span class="sxs-lookup"><span data-stu-id="cc8a6-136">NOTES</span></span>

## <span data-ttu-id="cc8a6-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="cc8a6-137">RELATED LINKS</span></span>

[<span data-ttu-id="cc8a6-138">Add-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="cc8a6-138">Add-AzTrafficManagerExpectedStatusCodeRange</span></span>](./Add-AzTrafficManagerExpectedStatusCodeRange.md)

[<span data-ttu-id="cc8a6-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="cc8a6-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="cc8a6-140">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="cc8a6-140">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)
