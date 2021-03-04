---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: B6E043FF-F4DD-44B7-BEAA-6B17C8F21D58
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/disable-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerProfile.md
ms.openlocfilehash: 4d667b1435a7396082f0626d8f55882f7c37b8ad
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901625"
---
# <span data-ttu-id="27101-101">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="27101-101">Disable-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="27101-102">簡介</span><span class="sxs-lookup"><span data-stu-id="27101-102">SYNOPSIS</span></span>
<span data-ttu-id="27101-103">停用流量管理員設定檔。</span><span class="sxs-lookup"><span data-stu-id="27101-103">Disables a Traffic Manager profile.</span></span>

## <span data-ttu-id="27101-104">語法</span><span class="sxs-lookup"><span data-stu-id="27101-104">SYNTAX</span></span>

### <span data-ttu-id="27101-105">領域</span><span class="sxs-lookup"><span data-stu-id="27101-105">Fields</span></span>
```
Disable-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27101-106">物件</span><span class="sxs-lookup"><span data-stu-id="27101-106">Object</span></span>
```
Disable-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27101-107">描述</span><span class="sxs-lookup"><span data-stu-id="27101-107">DESCRIPTION</span></span>
<span data-ttu-id="27101-108">**Disable-AzTrafficManagerProfile** Cmdlet 會停用 Azure 流量管理員設定檔。</span><span class="sxs-lookup"><span data-stu-id="27101-108">The **Disable-AzTrafficManagerProfile** cmdlet disables an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="27101-109">您可以使用管線或參數值來指定設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="27101-109">You can specify the profile object by using the pipeline or as a parameter value.</span></span>
<span data-ttu-id="27101-110">或者，您可以使用 Name 和 *ResourceGroupName* 參數來指定設定檔。 </span><span class="sxs-lookup"><span data-stu-id="27101-110">Alternatively, you can specify the profile by using the *Name* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="27101-111">例子</span><span class="sxs-lookup"><span data-stu-id="27101-111">EXAMPLES</span></span>

### <span data-ttu-id="27101-112">範例 1：停用由名稱指定的設定檔</span><span class="sxs-lookup"><span data-stu-id="27101-112">Example 1: Disable a profile specified by name</span></span>
```
PS C:\>Disable-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="27101-113">此命令會停用 ResourceGroup11 中名為 ContosoProfile 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="27101-113">This command disables the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="27101-114">命令會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="27101-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="27101-115">範例 2：使用管線停用設定檔</span><span class="sxs-lookup"><span data-stu-id="27101-115">Example 2: Disable a profile by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzTrafficManagerProfile -Force
```

<span data-ttu-id="27101-116">此命令會獲得 ResourceGroup11 中名為 ContosoProfile 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="27101-116">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="27101-117">命令接著使用管線運算子，將設定檔傳遞給 **Disable-AzTrafficManagerProfile** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="27101-117">The command then passes that profile to the **Disable-AzTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="27101-118">該 Cmdlet 會停用該設定檔。</span><span class="sxs-lookup"><span data-stu-id="27101-118">That cmdlet disables that profile.</span></span>
<span data-ttu-id="27101-119">命令會指定 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="27101-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="27101-120">因此，它不會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="27101-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="27101-121">參數</span><span class="sxs-lookup"><span data-stu-id="27101-121">PARAMETERS</span></span>

### <span data-ttu-id="27101-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27101-122">-DefaultProfile</span></span>
<span data-ttu-id="27101-123">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="27101-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27101-124">-強制</span><span class="sxs-lookup"><span data-stu-id="27101-124">-Force</span></span>
<span data-ttu-id="27101-125">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="27101-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="27101-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="27101-126">-Name</span></span>
<span data-ttu-id="27101-127">指定此 Cmdlet 停用的流量管理員設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="27101-127">Specifies the name of the Traffic Manager profile that this cmdlet disables.</span></span>

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

### <span data-ttu-id="27101-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27101-128">-ResourceGroupName</span></span>
<span data-ttu-id="27101-129">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="27101-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="27101-130">此 Cmdlet 會停用此參數指定之群組中的流量管理員設定檔。</span><span class="sxs-lookup"><span data-stu-id="27101-130">This cmdlet disables a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="27101-131">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="27101-131">-TrafficManagerProfile</span></span>
<span data-ttu-id="27101-132">指定 **要停用的 TrafficManagerProfile** 物件。</span><span class="sxs-lookup"><span data-stu-id="27101-132">Specifies a **TrafficManagerProfile** object to disable.</span></span>
<span data-ttu-id="27101-133">若要取得 **TrafficManagerProfile** 物件，請使用 Get-AzTrafficManagerProfile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="27101-133">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="27101-134">-確認</span><span class="sxs-lookup"><span data-stu-id="27101-134">-Confirm</span></span>
<span data-ttu-id="27101-135">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="27101-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27101-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27101-136">-WhatIf</span></span>
<span data-ttu-id="27101-137">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="27101-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27101-138">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="27101-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27101-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27101-139">CommonParameters</span></span>
<span data-ttu-id="27101-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="27101-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27101-141">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="27101-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27101-142">輸入</span><span class="sxs-lookup"><span data-stu-id="27101-142">INPUTS</span></span>

### <span data-ttu-id="27101-143">Microsoft.Azure.Commands.TrafficManager.models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="27101-143">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="27101-144">輸出</span><span class="sxs-lookup"><span data-stu-id="27101-144">OUTPUTS</span></span>

### <span data-ttu-id="27101-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="27101-145">System.Boolean</span></span>

## <span data-ttu-id="27101-146">筆記</span><span class="sxs-lookup"><span data-stu-id="27101-146">NOTES</span></span>

## <span data-ttu-id="27101-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="27101-147">RELATED LINKS</span></span>

[<span data-ttu-id="27101-148">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="27101-148">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="27101-149">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="27101-149">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="27101-150">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="27101-150">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="27101-151">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="27101-151">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="27101-152">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="27101-152">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


