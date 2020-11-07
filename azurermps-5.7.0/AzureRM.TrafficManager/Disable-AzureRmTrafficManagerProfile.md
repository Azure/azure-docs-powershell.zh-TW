---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: B6E043FF-F4DD-44B7-BEAA-6B17C8F21D58
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/disable-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Disable-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Disable-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: 99bff202a67dcc0db6109f3622188e10d250c573
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624648"
---
# <span data-ttu-id="0622f-101">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0622f-101">Disable-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="0622f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0622f-102">SYNOPSIS</span></span>
<span data-ttu-id="0622f-103">停用流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="0622f-103">Disables a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0622f-104">句法</span><span class="sxs-lookup"><span data-stu-id="0622f-104">SYNTAX</span></span>

### <span data-ttu-id="0622f-105">區域</span><span class="sxs-lookup"><span data-stu-id="0622f-105">Fields</span></span>
```
Disable-AzureRmTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0622f-106">面向</span><span class="sxs-lookup"><span data-stu-id="0622f-106">Object</span></span>
```
Disable-AzureRmTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0622f-107">說明</span><span class="sxs-lookup"><span data-stu-id="0622f-107">DESCRIPTION</span></span>
<span data-ttu-id="0622f-108">**Disable AzureRmTrafficManagerProfile** Cmdlet 會停用 Azure 流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="0622f-108">The **Disable-AzureRmTrafficManagerProfile** cmdlet disables an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="0622f-109">您可以使用管線或參數值來指定設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="0622f-109">You can specify the profile object by using the pipeline or as a parameter value.</span></span>
<span data-ttu-id="0622f-110">或者，您也可以使用 *Name* 和 *ResourceGroupName* 參數來指定設定檔。</span><span class="sxs-lookup"><span data-stu-id="0622f-110">Alternatively, you can specify the profile by using the *Name* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="0622f-111">示例</span><span class="sxs-lookup"><span data-stu-id="0622f-111">EXAMPLES</span></span>

### <span data-ttu-id="0622f-112">範例1：停用名稱指定的設定檔</span><span class="sxs-lookup"><span data-stu-id="0622f-112">Example 1: Disable a profile specified by name</span></span>
```
PS C:\>Disable-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="0622f-113">這個命令會在 ResourceGroup11 中停用名為 ContosoProfile 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="0622f-113">This command disables the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="0622f-114">命令會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0622f-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="0622f-115">範例2：使用管線停用設定檔</span><span class="sxs-lookup"><span data-stu-id="0622f-115">Example 2: Disable a profile by using the pipeline</span></span>
```
PS C:\>Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzureRmTrafficManagerProfile -Force
```

<span data-ttu-id="0622f-116">這個命令會在 ResourceGroup11 中取得名為 ContosoProfile 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="0622f-116">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="0622f-117">然後，命令會使用管線運算子將該設定檔傳遞到 **Disable AzureRmTrafficManagerProfile** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0622f-117">The command then passes that profile to the **Disable-AzureRmTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="0622f-118">該 Cmdlet 會停用該設定檔。</span><span class="sxs-lookup"><span data-stu-id="0622f-118">That cmdlet disables that profile.</span></span>
<span data-ttu-id="0622f-119">命令會指定 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="0622f-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="0622f-120">因此，它不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0622f-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="0622f-121">參數</span><span class="sxs-lookup"><span data-stu-id="0622f-121">PARAMETERS</span></span>

### <span data-ttu-id="0622f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0622f-122">-DefaultProfile</span></span>
<span data-ttu-id="0622f-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0622f-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0622f-124">-Force</span><span class="sxs-lookup"><span data-stu-id="0622f-124">-Force</span></span>
<span data-ttu-id="0622f-125">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="0622f-125">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0622f-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="0622f-126">-Name</span></span>
<span data-ttu-id="0622f-127">指定此 Cmdlet 停用之流量管理器設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="0622f-127">Specifies the name of the Traffic Manager profile that this cmdlet disables.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0622f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0622f-128">-ResourceGroupName</span></span>
<span data-ttu-id="0622f-129">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0622f-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="0622f-130">這個 Cmdlet 會停用此參數指定之群組中的流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="0622f-130">This cmdlet disables a Traffic Manager profile in the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0622f-131">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0622f-131">-TrafficManagerProfile</span></span>
<span data-ttu-id="0622f-132">指定要停用的 **TrafficManagerProfile** 物件。</span><span class="sxs-lookup"><span data-stu-id="0622f-132">Specifies a **TrafficManagerProfile** object to disable.</span></span>
<span data-ttu-id="0622f-133">若要取得 **TrafficManagerProfile** 物件，請使用 Get-AzureRmTrafficManagerProfile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0622f-133">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: TrafficManagerProfile
Parameter Sets: Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0622f-134">-確認</span><span class="sxs-lookup"><span data-stu-id="0622f-134">-Confirm</span></span>
<span data-ttu-id="0622f-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0622f-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0622f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0622f-136">-WhatIf</span></span>
<span data-ttu-id="0622f-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0622f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0622f-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0622f-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0622f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0622f-139">CommonParameters</span></span>
<span data-ttu-id="0622f-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0622f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0622f-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0622f-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0622f-142">輸入</span><span class="sxs-lookup"><span data-stu-id="0622f-142">INPUTS</span></span>

### <span data-ttu-id="0622f-143">TrafficManagerProfile （）</span><span class="sxs-lookup"><span data-stu-id="0622f-143">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="0622f-144">這個 Cmdlet 接受 **TrafficManagerProfile** 物件。</span><span class="sxs-lookup"><span data-stu-id="0622f-144">This cmdlet accepts a **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="0622f-145">輸出</span><span class="sxs-lookup"><span data-stu-id="0622f-145">OUTPUTS</span></span>

### <span data-ttu-id="0622f-146">System.object</span><span class="sxs-lookup"><span data-stu-id="0622f-146">System.Boolean</span></span>

## <span data-ttu-id="0622f-147">筆記</span><span class="sxs-lookup"><span data-stu-id="0622f-147">NOTES</span></span>

## <span data-ttu-id="0622f-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="0622f-148">RELATED LINKS</span></span>

[<span data-ttu-id="0622f-149">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0622f-149">Enable-AzureRmTrafficManagerProfile</span></span>](./Enable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="0622f-150">AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0622f-150">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="0622f-151">新-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0622f-151">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="0622f-152">移除-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0622f-152">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="0622f-153">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0622f-153">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


