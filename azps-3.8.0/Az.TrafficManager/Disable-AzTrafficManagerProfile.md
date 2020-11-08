---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: B6E043FF-F4DD-44B7-BEAA-6B17C8F21D58
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/disable-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerProfile.md
ms.openlocfilehash: fc1370da73b9217c5f5f8b24705047f154b50f31
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957587"
---
# <span data-ttu-id="7e4c5-101">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7e4c5-101">Disable-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="7e4c5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7e4c5-102">SYNOPSIS</span></span>
<span data-ttu-id="7e4c5-103">停用流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="7e4c5-103">Disables a Traffic Manager profile.</span></span>

## <span data-ttu-id="7e4c5-104">句法</span><span class="sxs-lookup"><span data-stu-id="7e4c5-104">SYNTAX</span></span>

### <span data-ttu-id="7e4c5-105">區域</span><span class="sxs-lookup"><span data-stu-id="7e4c5-105">Fields</span></span>
```
Disable-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e4c5-106">面向</span><span class="sxs-lookup"><span data-stu-id="7e4c5-106">Object</span></span>
```
Disable-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e4c5-107">說明</span><span class="sxs-lookup"><span data-stu-id="7e4c5-107">DESCRIPTION</span></span>
<span data-ttu-id="7e4c5-108">**Disable AzTrafficManagerProfile** Cmdlet 會停用 Azure 流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="7e4c5-108">The **Disable-AzTrafficManagerProfile** cmdlet disables an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="7e4c5-109">您可以使用管線或參數值來指定設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="7e4c5-109">You can specify the profile object by using the pipeline or as a parameter value.</span></span>
<span data-ttu-id="7e4c5-110">或者，您也可以使用 *Name* 和 *ResourceGroupName* 參數來指定設定檔。</span><span class="sxs-lookup"><span data-stu-id="7e4c5-110">Alternatively, you can specify the profile by using the *Name* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="7e4c5-111">示例</span><span class="sxs-lookup"><span data-stu-id="7e4c5-111">EXAMPLES</span></span>

### <span data-ttu-id="7e4c5-112">範例1：停用名稱指定的設定檔</span><span class="sxs-lookup"><span data-stu-id="7e4c5-112">Example 1: Disable a profile specified by name</span></span>
```
PS C:\>Disable-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="7e4c5-113">這個命令會在 ResourceGroup11 中停用名為 ContosoProfile 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="7e4c5-113">This command disables the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="7e4c5-114">命令會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7e4c5-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="7e4c5-115">範例2：使用管線停用設定檔</span><span class="sxs-lookup"><span data-stu-id="7e4c5-115">Example 2: Disable a profile by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzTrafficManagerProfile -Force
```

<span data-ttu-id="7e4c5-116">這個命令會在 ResourceGroup11 中取得名為 ContosoProfile 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="7e4c5-116">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="7e4c5-117">然後，命令會使用管線運算子將該設定檔傳遞到 **Disable AzTrafficManagerProfile** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7e4c5-117">The command then passes that profile to the **Disable-AzTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7e4c5-118">該 Cmdlet 會停用該設定檔。</span><span class="sxs-lookup"><span data-stu-id="7e4c5-118">That cmdlet disables that profile.</span></span>
<span data-ttu-id="7e4c5-119">命令會指定 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="7e4c5-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="7e4c5-120">因此，它不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7e4c5-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="7e4c5-121">參數</span><span class="sxs-lookup"><span data-stu-id="7e4c5-121">PARAMETERS</span></span>

### <span data-ttu-id="7e4c5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e4c5-122">-DefaultProfile</span></span>
<span data-ttu-id="7e4c5-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7e4c5-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e4c5-124">-Force</span><span class="sxs-lookup"><span data-stu-id="7e4c5-124">-Force</span></span>
<span data-ttu-id="7e4c5-125">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="7e4c5-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7e4c5-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="7e4c5-126">-Name</span></span>
<span data-ttu-id="7e4c5-127">指定此 Cmdlet 停用之流量管理器設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="7e4c5-127">Specifies the name of the Traffic Manager profile that this cmdlet disables.</span></span>

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

### <span data-ttu-id="7e4c5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e4c5-128">-ResourceGroupName</span></span>
<span data-ttu-id="7e4c5-129">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7e4c5-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="7e4c5-130">這個 Cmdlet 會停用此參數指定之群組中的流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="7e4c5-130">This cmdlet disables a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="7e4c5-131">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7e4c5-131">-TrafficManagerProfile</span></span>
<span data-ttu-id="7e4c5-132">指定要停用的 **TrafficManagerProfile** 物件。</span><span class="sxs-lookup"><span data-stu-id="7e4c5-132">Specifies a **TrafficManagerProfile** object to disable.</span></span>
<span data-ttu-id="7e4c5-133">若要取得 **TrafficManagerProfile** 物件，請使用 Get-AzTrafficManagerProfile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7e4c5-133">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="7e4c5-134">-確認</span><span class="sxs-lookup"><span data-stu-id="7e4c5-134">-Confirm</span></span>
<span data-ttu-id="7e4c5-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7e4c5-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e4c5-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e4c5-136">-WhatIf</span></span>
<span data-ttu-id="7e4c5-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7e4c5-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e4c5-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7e4c5-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e4c5-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e4c5-139">CommonParameters</span></span>
<span data-ttu-id="7e4c5-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7e4c5-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e4c5-141">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7e4c5-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e4c5-142">輸入</span><span class="sxs-lookup"><span data-stu-id="7e4c5-142">INPUTS</span></span>

### <span data-ttu-id="7e4c5-143">TrafficManagerProfile 中的 TrafficManager。</span><span class="sxs-lookup"><span data-stu-id="7e4c5-143">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="7e4c5-144">輸出</span><span class="sxs-lookup"><span data-stu-id="7e4c5-144">OUTPUTS</span></span>

### <span data-ttu-id="7e4c5-145">System.object</span><span class="sxs-lookup"><span data-stu-id="7e4c5-145">System.Boolean</span></span>

## <span data-ttu-id="7e4c5-146">筆記</span><span class="sxs-lookup"><span data-stu-id="7e4c5-146">NOTES</span></span>

## <span data-ttu-id="7e4c5-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="7e4c5-147">RELATED LINKS</span></span>

[<span data-ttu-id="7e4c5-148">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7e4c5-148">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="7e4c5-149">AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7e4c5-149">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="7e4c5-150">新-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7e4c5-150">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="7e4c5-151">移除-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7e4c5-151">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="7e4c5-152">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7e4c5-152">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)

