---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 5A4D685F-B904-4C85-8B68-C9936B0627FA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/remove-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: 8e43fd59184d8d07688c5ac3d4a8a8cc872745f9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445336"
---
# <span data-ttu-id="9c898-101">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9c898-101">Remove-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="9c898-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9c898-102">SYNOPSIS</span></span>
<span data-ttu-id="9c898-103">刪除流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="9c898-103">Deletes a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c898-104">句法</span><span class="sxs-lookup"><span data-stu-id="9c898-104">SYNTAX</span></span>

### <span data-ttu-id="9c898-105">區域</span><span class="sxs-lookup"><span data-stu-id="9c898-105">Fields</span></span>
```
Remove-AzureRmTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c898-106">面向</span><span class="sxs-lookup"><span data-stu-id="9c898-106">Object</span></span>
```
Remove-AzureRmTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c898-107">說明</span><span class="sxs-lookup"><span data-stu-id="9c898-107">DESCRIPTION</span></span>
<span data-ttu-id="9c898-108">**AzureRmTrafficManagerProfile** Cmdlet 會刪除 Azure 流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="9c898-108">The **Remove-AzureRmTrafficManagerProfile** cmdlet deletes an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="9c898-109">使用 *Name* 及 *ResourceGroupName* 參數指定要刪除的設定檔。</span><span class="sxs-lookup"><span data-stu-id="9c898-109">Specify the profile to delete by using the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="9c898-110">或者，您也可以使用 *TrafficManagerProfile* 參數指定 **TrafficManagerProfile** 物件，或者您可以使用管線。</span><span class="sxs-lookup"><span data-stu-id="9c898-110">Alternatively, you can specify a **TrafficManagerProfile** object using the *TrafficManagerProfile* parameter, or you can use the pipeline.</span></span>

## <span data-ttu-id="9c898-111">示例</span><span class="sxs-lookup"><span data-stu-id="9c898-111">EXAMPLES</span></span>

### <span data-ttu-id="9c898-112">範例1：刪除名稱指定的設定檔</span><span class="sxs-lookup"><span data-stu-id="9c898-112">Example 1: Delete a profile specified by name</span></span>
```
PS C:\>Remove-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="9c898-113">這個命令會在 ResourceGroup11 中刪除名為 ContosoProfile 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="9c898-113">This command deletes the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="9c898-114">命令會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9c898-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="9c898-115">範例2：使用管線刪除設定檔</span><span class="sxs-lookup"><span data-stu-id="9c898-115">Example 2: Delete a profile by using the pipeline</span></span>
```
PS C:\>Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Remove-AzureRmTrafficManagerProfile -Force
```

<span data-ttu-id="9c898-116">這個命令會在 ResourceGroup11 中取得名為 ContosoProfile 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="9c898-116">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="9c898-117">然後，命令會使用管線運算子將該設定檔傳遞到 **AzureRmTrafficManagerProfile** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9c898-117">The command then passes that profile to the **Remove-AzureRmTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="9c898-118">該 Cmdlet 會刪除該設定檔。</span><span class="sxs-lookup"><span data-stu-id="9c898-118">That cmdlet deletes that profile.</span></span>
<span data-ttu-id="9c898-119">命令會指定 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="9c898-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="9c898-120">因此，它不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9c898-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="9c898-121">參數</span><span class="sxs-lookup"><span data-stu-id="9c898-121">PARAMETERS</span></span>

### <span data-ttu-id="9c898-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c898-122">-DefaultProfile</span></span>
<span data-ttu-id="9c898-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9c898-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c898-124">-Force</span><span class="sxs-lookup"><span data-stu-id="9c898-124">-Force</span></span>
<span data-ttu-id="9c898-125">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="9c898-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9c898-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="9c898-126">-Name</span></span>
<span data-ttu-id="9c898-127">指定此 Cmdlet 刪除的流量管理器設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="9c898-127">Specifies the name of the Traffic Manager profile that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="9c898-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c898-128">-ResourceGroupName</span></span>
<span data-ttu-id="9c898-129">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9c898-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="9c898-130">這個 Cmdlet 會刪除此參數指定之群組中的流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="9c898-130">This cmdlet deletes a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="9c898-131">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9c898-131">-TrafficManagerProfile</span></span>
<span data-ttu-id="9c898-132">指定要刪除的 **TrafficManagerProfile** 物件。</span><span class="sxs-lookup"><span data-stu-id="9c898-132">Specifies a **TrafficManagerProfile** object to delete.</span></span>
<span data-ttu-id="9c898-133">若要取得 **TrafficManagerProfile** 物件，請使用 Get-AzureRmTrafficManagerProfile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9c898-133">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="9c898-134">-確認</span><span class="sxs-lookup"><span data-stu-id="9c898-134">-Confirm</span></span>
<span data-ttu-id="9c898-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9c898-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c898-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c898-136">-WhatIf</span></span>
<span data-ttu-id="9c898-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9c898-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c898-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9c898-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c898-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c898-139">CommonParameters</span></span>
<span data-ttu-id="9c898-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9c898-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c898-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9c898-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c898-142">輸入</span><span class="sxs-lookup"><span data-stu-id="9c898-142">INPUTS</span></span>

### <span data-ttu-id="9c898-143">TrafficManagerProfile （）</span><span class="sxs-lookup"><span data-stu-id="9c898-143">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="9c898-144">這個 Cmdlet 接受 **TrafficManagerProfile** 物件。</span><span class="sxs-lookup"><span data-stu-id="9c898-144">This cmdlet accepts a **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="9c898-145">輸出</span><span class="sxs-lookup"><span data-stu-id="9c898-145">OUTPUTS</span></span>

### <span data-ttu-id="9c898-146">布林值</span><span class="sxs-lookup"><span data-stu-id="9c898-146">Boolean</span></span>
<span data-ttu-id="9c898-147">這個 Cmdlet 會傳回 $True 的值（如果它成功的話），或者如果刪除失敗，則會傳回 $False 值。</span><span class="sxs-lookup"><span data-stu-id="9c898-147">This cmdlet returns a value of $True, if it succeeds or, if the deletion fails, a value of $False.</span></span>

## <span data-ttu-id="9c898-148">筆記</span><span class="sxs-lookup"><span data-stu-id="9c898-148">NOTES</span></span>

## <span data-ttu-id="9c898-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="9c898-149">RELATED LINKS</span></span>

[<span data-ttu-id="9c898-150">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9c898-150">Disable-AzureRmTrafficManagerProfile</span></span>](./Disable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="9c898-151">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9c898-151">Enable-AzureRmTrafficManagerProfile</span></span>](./Enable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="9c898-152">AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9c898-152">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="9c898-153">新-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9c898-153">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="9c898-154">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9c898-154">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


