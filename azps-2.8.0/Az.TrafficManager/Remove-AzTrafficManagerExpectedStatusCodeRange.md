---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D344
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerexpectedstatuscoderange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerExpectedStatusCodeRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerExpectedStatusCodeRange.md
ms.openlocfilehash: 8f26030f726d472024dd788abb02e55f8eac4c6e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93793250"
---
# <span data-ttu-id="ef03f-101">Remove-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="ef03f-101">Remove-AzTrafficManagerExpectedStatusCodeRange</span></span>

## <span data-ttu-id="ef03f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ef03f-102">SYNOPSIS</span></span>
<span data-ttu-id="ef03f-103">從本機流量管理器設定檔物件移除預期的狀態碼範圍。</span><span class="sxs-lookup"><span data-stu-id="ef03f-103">Removes an expected status code range from a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="ef03f-104">句法</span><span class="sxs-lookup"><span data-stu-id="ef03f-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerExpectedStatusCodeRange -Min <Int32> -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef03f-105">說明</span><span class="sxs-lookup"><span data-stu-id="ef03f-105">DESCRIPTION</span></span>
<span data-ttu-id="ef03f-106">**AzTrafficManagerExpectedStatusCodeRange** Cmdlet 會從本機 Azure 流量管理器設定檔物件移除一系列預期的狀態碼。</span><span class="sxs-lookup"><span data-stu-id="ef03f-106">The **Remove-AzTrafficManagerExpectedStatusCodeRange** cmdlet removes a range of expected status codes from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="ef03f-107">您可以使用 New-AzTrafficManagerProfile 或 Get-AzTrafficManagerProfile Cmdlet 來取得設定檔。</span><span class="sxs-lookup"><span data-stu-id="ef03f-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="ef03f-108">這個 Cmdlet 作用於本機設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="ef03f-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="ef03f-109">使用 Set-AzTrafficManagerProfile Cmdlet，將您的變更提交至流量管理器的設定檔。</span><span class="sxs-lookup"><span data-stu-id="ef03f-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="ef03f-110">示例</span><span class="sxs-lookup"><span data-stu-id="ef03f-110">EXAMPLES</span></span>

### <span data-ttu-id="ef03f-111">範例1：從設定檔移除預期的狀態碼範圍</span><span class="sxs-lookup"><span data-stu-id="ef03f-111">Example 1: Remove an expected status code range from a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzTrafficManagerExpectedStatusCodeRange -TrafficManagerProfile $TrafficManagerProfile -Min 200
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="ef03f-112">第一個命令會使用 **AzTrafficManagerProfile** Cmdlet 取得 Azure 流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="ef03f-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="ef03f-113">第二個命令會將所儲存設定檔的預期狀態碼範圍從 $TrafficManagerProfile 中移除。</span><span class="sxs-lookup"><span data-stu-id="ef03f-113">The second command removes an expected status code range from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="ef03f-114">最後一個命令會更新流量管理器中的設定檔，以符合 $TrafficManagerProfile 中的本機值。</span><span class="sxs-lookup"><span data-stu-id="ef03f-114">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="ef03f-115">參數</span><span class="sxs-lookup"><span data-stu-id="ef03f-115">PARAMETERS</span></span>

### <span data-ttu-id="ef03f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef03f-116">-DefaultProfile</span></span>
<span data-ttu-id="ef03f-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ef03f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef03f-118">-Min</span><span class="sxs-lookup"><span data-stu-id="ef03f-118">-Min</span></span>
<span data-ttu-id="ef03f-119">指定要移除的狀態碼範圍中的最小值。</span><span class="sxs-lookup"><span data-stu-id="ef03f-119">Specifies the lowest value in the status code range to be removed.</span></span>

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

### <span data-ttu-id="ef03f-120">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ef03f-120">-TrafficManagerProfile</span></span>
<span data-ttu-id="ef03f-121">指定本機 **TrafficManagerProfile** 物件。</span><span class="sxs-lookup"><span data-stu-id="ef03f-121">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="ef03f-122">這個 Cmdlet 會修改這個本機物件。</span><span class="sxs-lookup"><span data-stu-id="ef03f-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="ef03f-123">若要取得 **TrafficManagerProfile** 物件，請使用 Get-AzTrafficManagerProfile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ef03f-123">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="ef03f-124">-確認</span><span class="sxs-lookup"><span data-stu-id="ef03f-124">-Confirm</span></span>
<span data-ttu-id="ef03f-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ef03f-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef03f-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef03f-126">-WhatIf</span></span>
<span data-ttu-id="ef03f-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ef03f-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ef03f-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ef03f-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef03f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef03f-129">CommonParameters</span></span>
<span data-ttu-id="ef03f-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ef03f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef03f-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ef03f-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef03f-132">輸入</span><span class="sxs-lookup"><span data-stu-id="ef03f-132">INPUTS</span></span>

### <span data-ttu-id="ef03f-133">TrafficManagerProfile 中的 TrafficManager。</span><span class="sxs-lookup"><span data-stu-id="ef03f-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="ef03f-134">輸出</span><span class="sxs-lookup"><span data-stu-id="ef03f-134">OUTPUTS</span></span>

### <span data-ttu-id="ef03f-135">TrafficManagerProfile 中的 TrafficManager。</span><span class="sxs-lookup"><span data-stu-id="ef03f-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="ef03f-136">筆記</span><span class="sxs-lookup"><span data-stu-id="ef03f-136">NOTES</span></span>

## <span data-ttu-id="ef03f-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="ef03f-137">RELATED LINKS</span></span>

[<span data-ttu-id="ef03f-138">附加 AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="ef03f-138">Add-AzTrafficManagerExpectedStatusCodeRange</span></span>](./Add-AzTrafficManagerExpectedStatusCodeRange.md)

[<span data-ttu-id="ef03f-139">AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ef03f-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="ef03f-140">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ef03f-140">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)
