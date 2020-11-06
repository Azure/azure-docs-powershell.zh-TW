---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/add-azurertmtrafficmanagercustomheadertoprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerCustomHeaderToProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerCustomHeaderToProfile.md
ms.openlocfilehash: c14854da187101f3b15db178c656005942c1bff0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455888"
---
# <span data-ttu-id="2b037-101">Add-AzureRmTrafficManagerCustomHeaderToProfile</span><span class="sxs-lookup"><span data-stu-id="2b037-101">Add-AzureRmTrafficManagerCustomHeaderToProfile</span></span>

## <span data-ttu-id="2b037-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2b037-102">SYNOPSIS</span></span>
<span data-ttu-id="2b037-103">將自訂標頭資訊新增到本機流量管理器設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="2b037-103">Adds custom header information to a local Traffic Manager profile object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b037-104">句法</span><span class="sxs-lookup"><span data-stu-id="2b037-104">SYNTAX</span></span>

```
Add-AzureRmTrafficManagerCustomHeaderToProfile -Name <String> -Value <String>
 -TrafficManagerProfile <TrafficManagerProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2b037-105">說明</span><span class="sxs-lookup"><span data-stu-id="2b037-105">DESCRIPTION</span></span>
<span data-ttu-id="2b037-106">**載入 AzureRmTrafficManagerCustomHeaderToProfile** Cmdlet 會將自訂標頭資訊新增到本機 Azure 流量管理器設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="2b037-106">The **Add-AzureRmTrafficManagerCustomHeaderToProfile** cmdlet adds custom header information to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="2b037-107">您可以使用 New-AzureRmTrafficManagerProfile 或 Get-AzureRmTrafficManagerProfile Cmdlet 來取得設定檔。</span><span class="sxs-lookup"><span data-stu-id="2b037-107">You can get a profile by using the New-AzureRmTrafficManagerProfile or Get-AzureRmTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="2b037-108">這個 Cmdlet 作用於本機設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="2b037-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="2b037-109">使用 Set-AzureRmTrafficManagerProfile Cmdlet，將您的變更提交至流量管理器的設定檔。</span><span class="sxs-lookup"><span data-stu-id="2b037-109">Commit your changes to the profile for Traffic Manager by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="2b037-110">示例</span><span class="sxs-lookup"><span data-stu-id="2b037-110">EXAMPLES</span></span>

### <span data-ttu-id="2b037-111">範例1：在設定檔中新增自訂標頭資訊</span><span class="sxs-lookup"><span data-stu-id="2b037-111">Example 1: Add custom header information to a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzureRmTrafficManagerCustomHeaderToProfile -TrafficManagerProfile $TrafficManagerProfile -Name "host" -Value "www.contoso.com"
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="2b037-112">第一個命令會使用 **AzureRmTrafficManagerProfile** Cmdlet 取得 Azure 流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="2b037-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzureRmTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="2b037-113">該命令會將本機設定檔儲存在 $TrafficManagerProfile 變數中。</span><span class="sxs-lookup"><span data-stu-id="2b037-113">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>
<span data-ttu-id="2b037-114">第二個命令會將自訂標頭資訊新增至儲存在 $TrafficManagerProfile 中的設定檔。</span><span class="sxs-lookup"><span data-stu-id="2b037-114">The second command adds custom header information to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="2b037-115">最後一個命令會更新流量管理器中的設定檔，以符合 $TrafficManagerProfile 中的本機值。</span><span class="sxs-lookup"><span data-stu-id="2b037-115">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="2b037-116">參數</span><span class="sxs-lookup"><span data-stu-id="2b037-116">PARAMETERS</span></span>

### <span data-ttu-id="2b037-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b037-117">-DefaultProfile</span></span>
<span data-ttu-id="2b037-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2b037-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b037-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="2b037-119">-Name</span></span>
<span data-ttu-id="2b037-120">指定要新增之自訂標頭資訊的名稱。</span><span class="sxs-lookup"><span data-stu-id="2b037-120">Specifies the name of the custom header information to be added.</span></span>

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

### <span data-ttu-id="2b037-121">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2b037-121">-TrafficManagerProfile</span></span>
<span data-ttu-id="2b037-122">指定本機 **TrafficManagerProfile** 物件。</span><span class="sxs-lookup"><span data-stu-id="2b037-122">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="2b037-123">這個 Cmdlet 會修改這個本機物件。</span><span class="sxs-lookup"><span data-stu-id="2b037-123">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="2b037-124">若要取得 **TrafficManagerProfile** 物件，請使用 Get-AzureRmTrafficManagerProfile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2b037-124">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="2b037-125">-值</span><span class="sxs-lookup"><span data-stu-id="2b037-125">-Value</span></span>
<span data-ttu-id="2b037-126">指定要新增之自訂標頭資訊的值。</span><span class="sxs-lookup"><span data-stu-id="2b037-126">Specifies the value of the custom header information to be added.</span></span>

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

### <span data-ttu-id="2b037-127">-確認</span><span class="sxs-lookup"><span data-stu-id="2b037-127">-Confirm</span></span>
<span data-ttu-id="2b037-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2b037-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b037-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b037-129">-WhatIf</span></span>
<span data-ttu-id="2b037-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2b037-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2b037-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2b037-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b037-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b037-132">CommonParameters</span></span>
<span data-ttu-id="2b037-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2b037-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b037-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2b037-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b037-135">輸入</span><span class="sxs-lookup"><span data-stu-id="2b037-135">INPUTS</span></span>

### <span data-ttu-id="2b037-136">TrafficManagerProfile （）</span><span class="sxs-lookup"><span data-stu-id="2b037-136">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="2b037-137">這個 Cmdlet 接受 **TrafficManagerProfile** 物件到這個 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2b037-137">This cmdlet accepts a **TrafficManagerProfile** object to this cmdlet.</span></span>

## <span data-ttu-id="2b037-138">輸出</span><span class="sxs-lookup"><span data-stu-id="2b037-138">OUTPUTS</span></span>

### <span data-ttu-id="2b037-139">TrafficManagerProfile （）</span><span class="sxs-lookup"><span data-stu-id="2b037-139">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="2b037-140">這個 Cmdlet 會傳回修改過的 **TrafficManagerProfile** 物件。</span><span class="sxs-lookup"><span data-stu-id="2b037-140">This cmdlet returns a modified **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="2b037-141">筆記</span><span class="sxs-lookup"><span data-stu-id="2b037-141">NOTES</span></span>

## <span data-ttu-id="2b037-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="2b037-142">RELATED LINKS</span></span>

[<span data-ttu-id="2b037-143">移除-AzureRmTrafficManagerCustomHeaderFromProfile</span><span class="sxs-lookup"><span data-stu-id="2b037-143">Remove-AzureRmTrafficManagerCustomHeaderFromProfile</span></span>](./Remove-AzureRmTrafficManagerCustomHeaderFromProfile.md)

[<span data-ttu-id="2b037-144">AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2b037-144">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="2b037-145">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2b037-145">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)
