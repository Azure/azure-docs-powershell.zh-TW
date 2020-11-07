---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5A4D685F-B904-4C85-8B68-C9936B0627FA
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerProfile.md
ms.openlocfilehash: 640aed5ccfb38a2dca6989048e3185774ceda15a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958987"
---
# <span data-ttu-id="d37a3-101">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d37a3-101">Remove-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="d37a3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d37a3-102">SYNOPSIS</span></span>
<span data-ttu-id="d37a3-103">刪除流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="d37a3-103">Deletes a Traffic Manager profile.</span></span>

## <span data-ttu-id="d37a3-104">句法</span><span class="sxs-lookup"><span data-stu-id="d37a3-104">SYNTAX</span></span>

### <span data-ttu-id="d37a3-105">區域</span><span class="sxs-lookup"><span data-stu-id="d37a3-105">Fields</span></span>
```
Remove-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d37a3-106">面向</span><span class="sxs-lookup"><span data-stu-id="d37a3-106">Object</span></span>
```
Remove-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d37a3-107">說明</span><span class="sxs-lookup"><span data-stu-id="d37a3-107">DESCRIPTION</span></span>
<span data-ttu-id="d37a3-108">**AzTrafficManagerProfile** Cmdlet 會刪除 Azure 流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="d37a3-108">The **Remove-AzTrafficManagerProfile** cmdlet deletes an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="d37a3-109">使用 *Name* 及 *ResourceGroupName* 參數指定要刪除的設定檔。</span><span class="sxs-lookup"><span data-stu-id="d37a3-109">Specify the profile to delete by using the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="d37a3-110">或者，您也可以使用 *TrafficManagerProfile* 參數指定 **TrafficManagerProfile** 物件，或者您可以使用管線。</span><span class="sxs-lookup"><span data-stu-id="d37a3-110">Alternatively, you can specify a **TrafficManagerProfile** object using the *TrafficManagerProfile* parameter, or you can use the pipeline.</span></span>

## <span data-ttu-id="d37a3-111">示例</span><span class="sxs-lookup"><span data-stu-id="d37a3-111">EXAMPLES</span></span>

### <span data-ttu-id="d37a3-112">範例1：刪除名稱指定的設定檔</span><span class="sxs-lookup"><span data-stu-id="d37a3-112">Example 1: Delete a profile specified by name</span></span>
```
PS C:\>Remove-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="d37a3-113">這個命令會在 ResourceGroup11 中刪除名為 ContosoProfile 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="d37a3-113">This command deletes the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="d37a3-114">命令會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d37a3-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="d37a3-115">範例2：使用管線刪除設定檔</span><span class="sxs-lookup"><span data-stu-id="d37a3-115">Example 2: Delete a profile by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Remove-AzTrafficManagerProfile -Force
```

<span data-ttu-id="d37a3-116">這個命令會在 ResourceGroup11 中取得名為 ContosoProfile 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="d37a3-116">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="d37a3-117">然後，命令會使用管線運算子將該設定檔傳遞到 **AzTrafficManagerProfile** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d37a3-117">The command then passes that profile to the **Remove-AzTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d37a3-118">該 Cmdlet 會刪除該設定檔。</span><span class="sxs-lookup"><span data-stu-id="d37a3-118">That cmdlet deletes that profile.</span></span>
<span data-ttu-id="d37a3-119">命令會指定 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="d37a3-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="d37a3-120">因此，它不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d37a3-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="d37a3-121">參數</span><span class="sxs-lookup"><span data-stu-id="d37a3-121">PARAMETERS</span></span>

### <span data-ttu-id="d37a3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d37a3-122">-DefaultProfile</span></span>
<span data-ttu-id="d37a3-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d37a3-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d37a3-124">-Force</span><span class="sxs-lookup"><span data-stu-id="d37a3-124">-Force</span></span>
<span data-ttu-id="d37a3-125">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="d37a3-125">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d37a3-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="d37a3-126">-Name</span></span>
<span data-ttu-id="d37a3-127">指定此 Cmdlet 刪除的流量管理器設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="d37a3-127">Specifies the name of the Traffic Manager profile that this cmdlet deletes.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d37a3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d37a3-128">-ResourceGroupName</span></span>
<span data-ttu-id="d37a3-129">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d37a3-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="d37a3-130">這個 Cmdlet 會刪除此參數指定之群組中的流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="d37a3-130">This cmdlet deletes a Traffic Manager profile in the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d37a3-131">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d37a3-131">-TrafficManagerProfile</span></span>
<span data-ttu-id="d37a3-132">指定要刪除的 **TrafficManagerProfile** 物件。</span><span class="sxs-lookup"><span data-stu-id="d37a3-132">Specifies a **TrafficManagerProfile** object to delete.</span></span>
<span data-ttu-id="d37a3-133">若要取得 **TrafficManagerProfile** 物件，請使用 Get-AzTrafficManagerProfile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d37a3-133">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d37a3-134">-確認</span><span class="sxs-lookup"><span data-stu-id="d37a3-134">-Confirm</span></span>
<span data-ttu-id="d37a3-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d37a3-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d37a3-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d37a3-136">-WhatIf</span></span>
<span data-ttu-id="d37a3-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d37a3-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d37a3-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d37a3-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d37a3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d37a3-139">CommonParameters</span></span>
<span data-ttu-id="d37a3-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d37a3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d37a3-141">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d37a3-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d37a3-142">輸入</span><span class="sxs-lookup"><span data-stu-id="d37a3-142">INPUTS</span></span>

### <span data-ttu-id="d37a3-143">TrafficManagerProfile 中的 TrafficManager。</span><span class="sxs-lookup"><span data-stu-id="d37a3-143">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="d37a3-144">輸出</span><span class="sxs-lookup"><span data-stu-id="d37a3-144">OUTPUTS</span></span>

### <span data-ttu-id="d37a3-145">System.object</span><span class="sxs-lookup"><span data-stu-id="d37a3-145">System.Boolean</span></span>

## <span data-ttu-id="d37a3-146">筆記</span><span class="sxs-lookup"><span data-stu-id="d37a3-146">NOTES</span></span>

## <span data-ttu-id="d37a3-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="d37a3-147">RELATED LINKS</span></span>

[<span data-ttu-id="d37a3-148">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d37a3-148">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="d37a3-149">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d37a3-149">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="d37a3-150">AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d37a3-150">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="d37a3-151">新-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d37a3-151">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="d37a3-152">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d37a3-152">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


