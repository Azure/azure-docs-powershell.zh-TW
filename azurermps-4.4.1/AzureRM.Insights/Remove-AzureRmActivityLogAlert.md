---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmActivityLogAlert.md
ms.openlocfilehash: adff43beed709db91b2f22bd1072728d3e7a0425
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626620"
---
# <span data-ttu-id="50729-101">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="50729-101">Remove-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="50729-102">摘要</span><span class="sxs-lookup"><span data-stu-id="50729-102">SYNOPSIS</span></span>
<span data-ttu-id="50729-103">移除活動記錄通知。</span><span class="sxs-lookup"><span data-stu-id="50729-103">Removes an activity log alert.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50729-104">句法</span><span class="sxs-lookup"><span data-stu-id="50729-104">SYNTAX</span></span>

### <span data-ttu-id="50729-105">移除活動記錄通知的預設參數</span><span class="sxs-lookup"><span data-stu-id="50729-105">Default parameters for remove an activity log alert</span></span>
```
Remove-AzureRmActivityLogAlert -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50729-106">用來移除活動記錄通知的參數從管道取得值</span><span class="sxs-lookup"><span data-stu-id="50729-106">Parameters to remove an activity log alerts taking value from the pipe</span></span>
```
Remove-AzureRmActivityLogAlert -InputObject <PSActivityLogAlertResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50729-107">用來移除活動記錄通知的參數從管道取得 ResourceId 的值</span><span class="sxs-lookup"><span data-stu-id="50729-107">Parameters to remove an activity log alerts taking the value of ResourceId from the pipe</span></span>
```
Remove-AzureRmActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50729-108">說明</span><span class="sxs-lookup"><span data-stu-id="50729-108">DESCRIPTION</span></span>
<span data-ttu-id="50729-109">**AzureRmActivityLogAlert** Cmdlet 會移除活動記錄通知。</span><span class="sxs-lookup"><span data-stu-id="50729-109">The **Remove-AzureRmActivityLogAlert** cmdlet removes an activity log alert.</span></span>
<span data-ttu-id="50729-110">這個 Cmdlet 會實現 ShouldProcess 模式，亦即，在實際修補資源之前，它可能會要求使用者進行確認。</span><span class="sxs-lookup"><span data-stu-id="50729-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="50729-111">示例</span><span class="sxs-lookup"><span data-stu-id="50729-111">EXAMPLES</span></span>

### <span data-ttu-id="50729-112">範例1：移除活動記錄通知</span><span class="sxs-lookup"><span data-stu-id="50729-112">Example 1: Remove an activity log alert</span></span>
```
PS C:\>Remove-AzureRmActivityLogAlert -ResourceGroup "Default-Web-CentralUS" -Name "myalert"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="50729-113">使用名稱和資源群組名稱作為輸入，移除活動記錄提醒。</span><span class="sxs-lookup"><span data-stu-id="50729-113">Removes an activity log alert using name and resource group name as inputs.</span></span>

### <span data-ttu-id="50729-114">範例2：使用 PSActivityLogAlertResource 做為輸入來移除活動記錄提醒</span><span class="sxs-lookup"><span data-stu-id="50729-114">Example 2: Remove an activity log alert using a PSActivityLogAlertResource as input</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1" | Remove-AzureRmActivityLogAlert 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
5c371547-80b0-4185-9b95-700b129de9d4                                                                                 OK
```

<span data-ttu-id="50729-115">使用 PSActivityLogAlertResource 作為輸入來移除活動記錄提醒。</span><span class="sxs-lookup"><span data-stu-id="50729-115">Removes an activity log alert using a PSActivityLogAlertResource as input.</span></span>

### <span data-ttu-id="50729-116">範例3：使用 ResourceId 參數移除 ActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="50729-116">Example 3: Remove the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Find-AzureRmResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Remove-AzureRmActivityLogAlert
```

<span data-ttu-id="50729-117">這個命令會從管道使用 ResourceId 參數移除 ActivityLogAlert。</span><span class="sxs-lookup"><span data-stu-id="50729-117">This command removes the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="50729-118">參數</span><span class="sxs-lookup"><span data-stu-id="50729-118">PARAMETERS</span></span>

### <span data-ttu-id="50729-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="50729-119">-Name</span></span>
<span data-ttu-id="50729-120">活動記錄通知的名稱。</span><span class="sxs-lookup"><span data-stu-id="50729-120">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for remove an activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50729-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50729-121">-ResourceGroupName</span></span>
<span data-ttu-id="50729-122">警示資源所在之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="50729-122">The name of the resource group where the alert resource exists.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for remove an activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50729-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="50729-123">-InputObject</span></span>
<span data-ttu-id="50729-124">設定呼叫的 InputObject tags 屬性來解壓縮所需的名稱，以及資源組名屬性。</span><span class="sxs-lookup"><span data-stu-id="50729-124">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: Parameters to remove an activity log alerts taking value from the pipe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50729-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="50729-125">-ResourceId</span></span>
<span data-ttu-id="50729-126">設定呼叫的 ResourceId 標籤屬性來解壓縮所需的名稱、資源組名稱屬性。</span><span class="sxs-lookup"><span data-stu-id="50729-126">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters to remove an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50729-127">-確認</span><span class="sxs-lookup"><span data-stu-id="50729-127">-Confirm</span></span>
<span data-ttu-id="50729-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="50729-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50729-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50729-129">-DefaultProfile</span></span>
<span data-ttu-id="50729-130">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="50729-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50729-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50729-131">-WhatIf</span></span>
<span data-ttu-id="50729-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="50729-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="50729-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="50729-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50729-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50729-134">CommonParameters</span></span>
<span data-ttu-id="50729-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="50729-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50729-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="50729-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50729-137">輸入</span><span class="sxs-lookup"><span data-stu-id="50729-137">INPUTS</span></span>

## <span data-ttu-id="50729-138">輸出</span><span class="sxs-lookup"><span data-stu-id="50729-138">OUTPUTS</span></span>

### <span data-ttu-id="50729-139">AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="50729-139">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="50729-140">筆記</span><span class="sxs-lookup"><span data-stu-id="50729-140">NOTES</span></span>

## <span data-ttu-id="50729-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="50729-141">RELATED LINKS</span></span>

[<span data-ttu-id="50729-142">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="50729-142">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="50729-143">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="50729-143">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="50729-144">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="50729-144">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="50729-145">AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="50729-145">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="50729-146">新-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="50729-146">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="50729-147">新-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="50729-147">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)

