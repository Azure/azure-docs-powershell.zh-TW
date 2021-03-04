---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5A4D685F-B904-4C85-8B68-C9936B0627FA
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/remove-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerProfile.md
ms.openlocfilehash: 1b1dab7edc07242dab28daa6028adefb8b7090eb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911241"
---
# <span data-ttu-id="b7e4a-101">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b7e4a-101">Remove-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="b7e4a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b7e4a-102">SYNOPSIS</span></span>
<span data-ttu-id="b7e4a-103">刪除流量管理員設定檔。</span><span class="sxs-lookup"><span data-stu-id="b7e4a-103">Deletes a Traffic Manager profile.</span></span>

## <span data-ttu-id="b7e4a-104">語法</span><span class="sxs-lookup"><span data-stu-id="b7e4a-104">SYNTAX</span></span>

### <span data-ttu-id="b7e4a-105">領域</span><span class="sxs-lookup"><span data-stu-id="b7e4a-105">Fields</span></span>
```
Remove-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7e4a-106">物件</span><span class="sxs-lookup"><span data-stu-id="b7e4a-106">Object</span></span>
```
Remove-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7e4a-107">描述</span><span class="sxs-lookup"><span data-stu-id="b7e4a-107">DESCRIPTION</span></span>
<span data-ttu-id="b7e4a-108">**Remove-AzTrafficManagerProfile** Cmdlet 會刪除 Azure 流量管理員設定檔。</span><span class="sxs-lookup"><span data-stu-id="b7e4a-108">The **Remove-AzTrafficManagerProfile** cmdlet deletes an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="b7e4a-109">使用 Name 和 *ResourceGroupName* 參數指定要刪除的設定檔。 </span><span class="sxs-lookup"><span data-stu-id="b7e4a-109">Specify the profile to delete by using the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="b7e4a-110">或者，您可以使用 **TrafficManagerProfile 參數指定 TrafficManagerProfile** 物件，或者您可以使用管線。 </span><span class="sxs-lookup"><span data-stu-id="b7e4a-110">Alternatively, you can specify a **TrafficManagerProfile** object using the *TrafficManagerProfile* parameter, or you can use the pipeline.</span></span>

## <span data-ttu-id="b7e4a-111">例子</span><span class="sxs-lookup"><span data-stu-id="b7e4a-111">EXAMPLES</span></span>

### <span data-ttu-id="b7e4a-112">範例 1：刪除由名稱指定的設定檔</span><span class="sxs-lookup"><span data-stu-id="b7e4a-112">Example 1: Delete a profile specified by name</span></span>
```
PS C:\>Remove-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="b7e4a-113">此命令會刪除 ResourceGroup11 中名為 ContosoProfile 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="b7e4a-113">This command deletes the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="b7e4a-114">命令會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b7e4a-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="b7e4a-115">範例 2：使用管線刪除設定檔</span><span class="sxs-lookup"><span data-stu-id="b7e4a-115">Example 2: Delete a profile by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Remove-AzTrafficManagerProfile -Force
```

<span data-ttu-id="b7e4a-116">此命令會獲得 ResourceGroup11 中名為 ContosoProfile 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="b7e4a-116">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="b7e4a-117">命令接著使用管線運算子，將設定檔傳遞給 **Remove-AzTrafficManagerProfile** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b7e4a-117">The command then passes that profile to the **Remove-AzTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b7e4a-118">該 Cmdlet 會刪除該設定檔。</span><span class="sxs-lookup"><span data-stu-id="b7e4a-118">That cmdlet deletes that profile.</span></span>
<span data-ttu-id="b7e4a-119">命令會指定 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="b7e4a-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="b7e4a-120">因此，它不會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b7e4a-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="b7e4a-121">參數</span><span class="sxs-lookup"><span data-stu-id="b7e4a-121">PARAMETERS</span></span>

### <span data-ttu-id="b7e4a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7e4a-122">-DefaultProfile</span></span>
<span data-ttu-id="b7e4a-123">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b7e4a-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7e4a-124">-強制</span><span class="sxs-lookup"><span data-stu-id="b7e4a-124">-Force</span></span>
<span data-ttu-id="b7e4a-125">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="b7e4a-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b7e4a-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="b7e4a-126">-Name</span></span>
<span data-ttu-id="b7e4a-127">指定此 Cmdlet 刪除的流量管理員設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="b7e4a-127">Specifies the name of the Traffic Manager profile that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="b7e4a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7e4a-128">-ResourceGroupName</span></span>
<span data-ttu-id="b7e4a-129">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b7e4a-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="b7e4a-130">此 Cmdlet 會刪除此參數指定之群組中的流量管理員設定檔。</span><span class="sxs-lookup"><span data-stu-id="b7e4a-130">This cmdlet deletes a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="b7e4a-131">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b7e4a-131">-TrafficManagerProfile</span></span>
<span data-ttu-id="b7e4a-132">指定 **要刪除的 TrafficManagerProfile** 物件。</span><span class="sxs-lookup"><span data-stu-id="b7e4a-132">Specifies a **TrafficManagerProfile** object to delete.</span></span>
<span data-ttu-id="b7e4a-133">若要取得 **TrafficManagerProfile** 物件，請使用 Get-AzTrafficManagerProfile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b7e4a-133">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="b7e4a-134">-確認</span><span class="sxs-lookup"><span data-stu-id="b7e4a-134">-Confirm</span></span>
<span data-ttu-id="b7e4a-135">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b7e4a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7e4a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7e4a-136">-WhatIf</span></span>
<span data-ttu-id="b7e4a-137">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b7e4a-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7e4a-138">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b7e4a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7e4a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7e4a-139">CommonParameters</span></span>
<span data-ttu-id="b7e4a-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b7e4a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7e4a-141">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="b7e4a-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7e4a-142">輸入</span><span class="sxs-lookup"><span data-stu-id="b7e4a-142">INPUTS</span></span>

### <span data-ttu-id="b7e4a-143">Microsoft.Azure.Commands.TrafficManager.models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b7e4a-143">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="b7e4a-144">輸出</span><span class="sxs-lookup"><span data-stu-id="b7e4a-144">OUTPUTS</span></span>

### <span data-ttu-id="b7e4a-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b7e4a-145">System.Boolean</span></span>

## <span data-ttu-id="b7e4a-146">筆記</span><span class="sxs-lookup"><span data-stu-id="b7e4a-146">NOTES</span></span>

## <span data-ttu-id="b7e4a-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="b7e4a-147">RELATED LINKS</span></span>

[<span data-ttu-id="b7e4a-148">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b7e4a-148">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="b7e4a-149">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b7e4a-149">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="b7e4a-150">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b7e4a-150">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="b7e4a-151">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b7e4a-151">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="b7e4a-152">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b7e4a-152">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


