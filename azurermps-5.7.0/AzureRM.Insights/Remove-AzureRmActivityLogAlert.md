---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmActivityLogAlert.md
ms.openlocfilehash: b712363b2b4e1d610f00f1111c48145debe084a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452239"
---
# <span data-ttu-id="24f11-101">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="24f11-101">Remove-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="24f11-102">摘要</span><span class="sxs-lookup"><span data-stu-id="24f11-102">SYNOPSIS</span></span>
<span data-ttu-id="24f11-103">移除活動記錄通知。</span><span class="sxs-lookup"><span data-stu-id="24f11-103">Removes an activity log alert.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24f11-104">句法</span><span class="sxs-lookup"><span data-stu-id="24f11-104">SYNTAX</span></span>

### <span data-ttu-id="24f11-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="24f11-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzureRmActivityLogAlert -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24f11-106">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="24f11-106">RemoveByInputObject</span></span>
```
Remove-AzureRmActivityLogAlert -InputObject <PSActivityLogAlertResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24f11-107">RemoveByResourceId</span><span class="sxs-lookup"><span data-stu-id="24f11-107">RemoveByResourceId</span></span>
```
Remove-AzureRmActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24f11-108">說明</span><span class="sxs-lookup"><span data-stu-id="24f11-108">DESCRIPTION</span></span>
<span data-ttu-id="24f11-109">**AzureRmActivityLogAlert** Cmdlet 會移除活動記錄通知。</span><span class="sxs-lookup"><span data-stu-id="24f11-109">The **Remove-AzureRmActivityLogAlert** cmdlet removes an activity log alert.</span></span>
<span data-ttu-id="24f11-110">這個 Cmdlet 會實現 ShouldProcess 模式，亦即，在實際修補資源之前，它可能會要求使用者進行確認。</span><span class="sxs-lookup"><span data-stu-id="24f11-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

<span data-ttu-id="24f11-111">這個 Cmdlet 會實現 ShouldProcess 模式，亦即，在實際建立、修改或移除資源之前，它可能會要求使用者進行確認。</span><span class="sxs-lookup"><span data-stu-id="24f11-111">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="24f11-112">示例</span><span class="sxs-lookup"><span data-stu-id="24f11-112">EXAMPLES</span></span>

### <span data-ttu-id="24f11-113">範例1：移除活動記錄通知</span><span class="sxs-lookup"><span data-stu-id="24f11-113">Example 1: Remove an activity log alert</span></span>
```
PS C:\>Remove-AzureRmActivityLogAlert -ResourceGroup "Default-Web-CentralUS" -Name "myalert"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="24f11-114">使用名稱和資源群組名稱作為輸入，移除活動記錄提醒。</span><span class="sxs-lookup"><span data-stu-id="24f11-114">Removes an activity log alert using name and resource group name as inputs.</span></span>

### <span data-ttu-id="24f11-115">範例2：使用 PSActivityLogAlertResource 做為輸入來移除活動記錄提醒</span><span class="sxs-lookup"><span data-stu-id="24f11-115">Example 2: Remove an activity log alert using a PSActivityLogAlertResource as input</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1" | Remove-AzureRmActivityLogAlert 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
5c371547-80b0-4185-9b95-700b129de9d4                                                                                 OK
```

<span data-ttu-id="24f11-116">使用 PSActivityLogAlertResource 作為輸入來移除活動記錄提醒。</span><span class="sxs-lookup"><span data-stu-id="24f11-116">Removes an activity log alert using a PSActivityLogAlertResource as input.</span></span>

### <span data-ttu-id="24f11-117">範例3：使用 ResourceId 參數移除 ActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="24f11-117">Example 3: Remove the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Find-AzureRmResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Remove-AzureRmActivityLogAlert
```

<span data-ttu-id="24f11-118">這個命令會從管道使用 ResourceId 參數移除 ActivityLogAlert。</span><span class="sxs-lookup"><span data-stu-id="24f11-118">This command removes the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="24f11-119">參數</span><span class="sxs-lookup"><span data-stu-id="24f11-119">PARAMETERS</span></span>

### <span data-ttu-id="24f11-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24f11-120">-DefaultProfile</span></span>
<span data-ttu-id="24f11-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="24f11-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="24f11-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="24f11-122">-InputObject</span></span>
<span data-ttu-id="24f11-123">設定呼叫的 InputObject tags 屬性來解壓縮所需的名稱，以及資源組名屬性。</span><span class="sxs-lookup"><span data-stu-id="24f11-123">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

```yaml
Type: PSActivityLogAlertResource
Parameter Sets: RemoveByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="24f11-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="24f11-124">-Name</span></span>
<span data-ttu-id="24f11-125">活動記錄通知的名稱。</span><span class="sxs-lookup"><span data-stu-id="24f11-125">The name of the activity log alert.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24f11-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24f11-126">-ResourceGroupName</span></span>
<span data-ttu-id="24f11-127">警示資源所在之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="24f11-127">The name of the resource group where the alert resource exists.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24f11-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="24f11-128">-ResourceId</span></span>
<span data-ttu-id="24f11-129">設定呼叫的 ResourceId 標籤屬性來解壓縮所需的名稱、資源組名稱屬性。</span><span class="sxs-lookup"><span data-stu-id="24f11-129">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24f11-130">-確認</span><span class="sxs-lookup"><span data-stu-id="24f11-130">-Confirm</span></span>
<span data-ttu-id="24f11-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="24f11-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24f11-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24f11-132">-WhatIf</span></span>
<span data-ttu-id="24f11-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="24f11-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="24f11-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="24f11-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24f11-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24f11-135">CommonParameters</span></span>
<span data-ttu-id="24f11-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="24f11-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24f11-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="24f11-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24f11-138">輸入</span><span class="sxs-lookup"><span data-stu-id="24f11-138">INPUTS</span></span>

### <span data-ttu-id="24f11-139">所有</span><span class="sxs-lookup"><span data-stu-id="24f11-139">None</span></span>
<span data-ttu-id="24f11-140">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="24f11-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="24f11-141">輸出</span><span class="sxs-lookup"><span data-stu-id="24f11-141">OUTPUTS</span></span>

### <span data-ttu-id="24f11-142">AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="24f11-142">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="24f11-143">筆記</span><span class="sxs-lookup"><span data-stu-id="24f11-143">NOTES</span></span>

## <span data-ttu-id="24f11-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="24f11-144">RELATED LINKS</span></span>

[<span data-ttu-id="24f11-145">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="24f11-145">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="24f11-146">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="24f11-146">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="24f11-147">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="24f11-147">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="24f11-148">AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="24f11-148">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="24f11-149">新-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="24f11-149">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="24f11-150">新-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="24f11-150">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)

