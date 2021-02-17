---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzActivityLogAlert.md
ms.openlocfilehash: 9d1cd1b13a24c2b5a5374d29cfd38273caa92e33
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100403012"
---
# <span data-ttu-id="b4d90-101">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="b4d90-101">Remove-AzActivityLogAlert</span></span>

## <span data-ttu-id="b4d90-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b4d90-102">SYNOPSIS</span></span>
<span data-ttu-id="b4d90-103">移除活動記錄提醒。</span><span class="sxs-lookup"><span data-stu-id="b4d90-103">Removes an activity log alert.</span></span>

## <span data-ttu-id="b4d90-104">語法</span><span class="sxs-lookup"><span data-stu-id="b4d90-104">SYNTAX</span></span>

### <span data-ttu-id="b4d90-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b4d90-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzActivityLogAlert -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4d90-106">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="b4d90-106">RemoveByInputObject</span></span>
```
Remove-AzActivityLogAlert -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4d90-107">RemoveByResourceId</span><span class="sxs-lookup"><span data-stu-id="b4d90-107">RemoveByResourceId</span></span>
```
Remove-AzActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b4d90-108">描述</span><span class="sxs-lookup"><span data-stu-id="b4d90-108">DESCRIPTION</span></span>
<span data-ttu-id="b4d90-109">**Remove-AzActivityLogAlert** Cmdlet 會移除活動記錄提醒。</span><span class="sxs-lookup"><span data-stu-id="b4d90-109">The **Remove-AzActivityLogAlert** cmdlet removes an activity log alert.</span></span>
<span data-ttu-id="b4d90-110">此 Cmdlet 實做 ShouldProcess 模式，即實際修補資源之前，可能會向使用者要求確認。</span><span class="sxs-lookup"><span data-stu-id="b4d90-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>
<span data-ttu-id="b4d90-111">此 Cmdlet 實做 ShouldProcess 模式，即實際建立、修改或移除資源之前，可能會向使用者要求確認。</span><span class="sxs-lookup"><span data-stu-id="b4d90-111">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="b4d90-112">例子</span><span class="sxs-lookup"><span data-stu-id="b4d90-112">EXAMPLES</span></span>

### <span data-ttu-id="b4d90-113">範例 1：移除活動記錄提醒</span><span class="sxs-lookup"><span data-stu-id="b4d90-113">Example 1: Remove an activity log alert</span></span>
```
PS C:\>Remove-AzActivityLogAlert -ResourceGroup "Default-Web-CentralUS" -Name "myalert"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="b4d90-114">使用名稱和資源組名做為輸入來移除活動記錄提醒。</span><span class="sxs-lookup"><span data-stu-id="b4d90-114">Removes an activity log alert using name and resource group name as inputs.</span></span>

### <span data-ttu-id="b4d90-115">範例 2：使用 PSActivityLogAlertResource 做為輸入來移除活動記錄提醒</span><span class="sxs-lookup"><span data-stu-id="b4d90-115">Example 2: Remove an activity log alert using a PSActivityLogAlertResource as input</span></span>
```
PS C:\>Get-AzActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1" | Remove-AzActivityLogAlert 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
5c371547-80b0-4185-9b95-700b129de9d4                                                                                 OK
```

<span data-ttu-id="b4d90-116">使用 PSActivityLogAlertResource 做為輸入來移除活動記錄提醒。</span><span class="sxs-lookup"><span data-stu-id="b4d90-116">Removes an activity log alert using a PSActivityLogAlertResource as input.</span></span>

### <span data-ttu-id="b4d90-117">範例 3：使用 ResourceId 參數移除 ActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="b4d90-117">Example 3: Remove the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Find-AzResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Remove-AzActivityLogAlert
```

<span data-ttu-id="b4d90-118">此命令會使用 ResourceId 參數從管道移除 ActivityLogAlert。</span><span class="sxs-lookup"><span data-stu-id="b4d90-118">This command removes the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="b4d90-119">參數</span><span class="sxs-lookup"><span data-stu-id="b4d90-119">PARAMETERS</span></span>

### <span data-ttu-id="b4d90-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4d90-120">-DefaultProfile</span></span>
<span data-ttu-id="b4d90-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="b4d90-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b4d90-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b4d90-122">-InputObject</span></span>
<span data-ttu-id="b4d90-123">設定呼叫的 InputObject 標記屬性，以解壓縮必要的名稱和資源組名屬性。</span><span class="sxs-lookup"><span data-stu-id="b4d90-123">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b4d90-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="b4d90-124">-Name</span></span>
<span data-ttu-id="b4d90-125">活動記錄提醒的名稱。</span><span class="sxs-lookup"><span data-stu-id="b4d90-125">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4d90-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4d90-126">-ResourceGroupName</span></span>
<span data-ttu-id="b4d90-127">警示資源存在之資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b4d90-127">The name of the resource group where the alert resource exists.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4d90-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4d90-128">-ResourceId</span></span>
<span data-ttu-id="b4d90-129">設定呼叫的 ResourceId 標記屬性，以解壓縮必要的名稱、資源組名屬性。</span><span class="sxs-lookup"><span data-stu-id="b4d90-129">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4d90-130">-確認</span><span class="sxs-lookup"><span data-stu-id="b4d90-130">-Confirm</span></span>
<span data-ttu-id="b4d90-131">執行 Cmdlet 之前，系統會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b4d90-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4d90-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4d90-132">-WhatIf</span></span>
<span data-ttu-id="b4d90-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b4d90-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b4d90-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b4d90-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4d90-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4d90-135">CommonParameters</span></span>
<span data-ttu-id="b4d90-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b4d90-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4d90-137">詳細資訊請參閱 https://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="b4d90-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4d90-138">輸入</span><span class="sxs-lookup"><span data-stu-id="b4d90-138">INPUTS</span></span>

### <span data-ttu-id="b4d90-139">System.String</span><span class="sxs-lookup"><span data-stu-id="b4d90-139">System.String</span></span>

### <span data-ttu-id="b4d90-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="b4d90-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="b4d90-141">輸出</span><span class="sxs-lookup"><span data-stu-id="b4d90-141">OUTPUTS</span></span>

### <span data-ttu-id="b4d90-142">Microsoft.Azure.AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="b4d90-142">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="b4d90-143">筆記</span><span class="sxs-lookup"><span data-stu-id="b4d90-143">NOTES</span></span>

## <span data-ttu-id="b4d90-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="b4d90-144">RELATED LINKS</span></span>

[<span data-ttu-id="b4d90-145">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="b4d90-145">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="b4d90-146">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="b4d90-146">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="b4d90-147">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="b4d90-147">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="b4d90-148">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="b4d90-148">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="b4d90-149">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="b4d90-149">New-AzActionGroup</span></span>](./New-AzActionGroup.md)



