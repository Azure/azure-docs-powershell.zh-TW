---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Enable-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Enable-AzureRmActivityLogAlert.md
ms.openlocfilehash: 92607537fb80132627e1f26f240a10b8f7150fb8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456596"
---
# <span data-ttu-id="f3a08-101">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="f3a08-101">Enable-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="f3a08-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f3a08-102">SYNOPSIS</span></span>
<span data-ttu-id="f3a08-103">啟用活動記錄通知並設定其標記。</span><span class="sxs-lookup"><span data-stu-id="f3a08-103">Enables an activity log alert and sets its Tags.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3a08-104">句法</span><span class="sxs-lookup"><span data-stu-id="f3a08-104">SYNTAX</span></span>

### <span data-ttu-id="f3a08-105">啟用活動記錄通知的預設參數</span><span class="sxs-lookup"><span data-stu-id="f3a08-105">Default parameters for enable an activity log alert</span></span>
```
Enable-AzureRmActivityLogAlert -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3a08-106">讓活動記錄通知從管道取得價值的參數</span><span class="sxs-lookup"><span data-stu-id="f3a08-106">Parameters to enable an activity log alerts taking value from the pipe</span></span>
```
Enable-AzureRmActivityLogAlert -InputObject <PSActivityLogAlertResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3a08-107">[參數] 可讓活動記錄警報從管道取得 ResourceId 的值</span><span class="sxs-lookup"><span data-stu-id="f3a08-107">Parameters to enable an activity log alerts taking the value of ResourceId from the pipe</span></span>
```
Enable-AzureRmActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3a08-108">說明</span><span class="sxs-lookup"><span data-stu-id="f3a08-108">DESCRIPTION</span></span>
<span data-ttu-id="f3a08-109">**Enable-AzureRmActivityLogAlert** Cmdlet 可啟用活動記錄通知並設定其標記。</span><span class="sxs-lookup"><span data-stu-id="f3a08-109">The **Enable-AzureRmActivityLogAlert** cmdlet allows enabling an activity log alert and setting its tags.</span></span>
<span data-ttu-id="f3a08-110">這個 Cmdlet 會實現 ShouldProcess 模式，亦即，在實際修補資源之前，它可能會要求使用者進行確認。</span><span class="sxs-lookup"><span data-stu-id="f3a08-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="f3a08-111">示例</span><span class="sxs-lookup"><span data-stu-id="f3a08-111">EXAMPLES</span></span>

### <span data-ttu-id="f3a08-112">範例1：停用活動記錄通知</span><span class="sxs-lookup"><span data-stu-id="f3a08-112">Example 1: Disable an activity log alert</span></span>
```
PS C:\>Enable-AzureRmActivityLogAlert -Name "alert1" -ResourceGroupName "Default-ActivityLogsAlerts"
```

<span data-ttu-id="f3a08-113">這個命令會在資源群組預設-ActivityLogsAlerts 中啟用稱為 alert1 的活動記錄提醒。</span><span class="sxs-lookup"><span data-stu-id="f3a08-113">This command enables the activity log alert called alert1 in the resource group Default-ActivityLogsAlerts.</span></span>

### <span data-ttu-id="f3a08-114">範例2：使用 PSActivityLogAlertResource 物件做為輸入來啟用活動記錄提醒</span><span class="sxs-lookup"><span data-stu-id="f3a08-114">Example 2: Enable an activity log alert using a PSActivityLogAlertResource object as input</span></span>
```
PS C:\>$obj = Get-AzureRmActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1"
PS C:\>Enable-AzureRmActivityLogAlert -InputObject $obj
```

<span data-ttu-id="f3a08-115">這個命令會啟用稱為 alert1 的活動記錄提醒。</span><span class="sxs-lookup"><span data-stu-id="f3a08-115">This command enables an activity log alert called alert1.</span></span> <span data-ttu-id="f3a08-116">針對這種情況，它會使用 PSActivityLogAlertResource 物件做為輸入引數。</span><span class="sxs-lookup"><span data-stu-id="f3a08-116">For this it uses a PSActivityLogAlertResource object as input argument.</span></span>

### <span data-ttu-id="f3a08-117">範例3：使用 ResourceId 參數啟用 ActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="f3a08-117">Example 3: Enable the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Find-AzureRmResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Enable-AzureRmActivityLogAlert
```

<span data-ttu-id="f3a08-118">這個命令會從管道使用 ResourceId 參數來啟用 ActivityLogAlert。</span><span class="sxs-lookup"><span data-stu-id="f3a08-118">This command enables the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="f3a08-119">參數</span><span class="sxs-lookup"><span data-stu-id="f3a08-119">PARAMETERS</span></span>

### <span data-ttu-id="f3a08-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="f3a08-120">-Name</span></span>
<span data-ttu-id="f3a08-121">活動記錄通知的名稱。</span><span class="sxs-lookup"><span data-stu-id="f3a08-121">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for enable an activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3a08-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3a08-122">-ResourceGroupName</span></span>
<span data-ttu-id="f3a08-123">要在其中存在預警資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f3a08-123">The name of the resource group where the alert resource is going to exist.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for enable an activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3a08-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f3a08-124">-InputObject</span></span>
<span data-ttu-id="f3a08-125">設定通話的 InputObject tags 屬性來解壓縮所需的名稱、資源組名稱，以及選用的標記屬性。</span><span class="sxs-lookup"><span data-stu-id="f3a08-125">Sets the InputObject tags property of the call to extract the required name, resource group name, and the optional tags properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: Parameters to enable an activity log alerts taking value from the pipe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f3a08-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f3a08-126">-ResourceId</span></span>
<span data-ttu-id="f3a08-127">設定呼叫的 ResourceId 標籤屬性來解壓縮所需的名稱、資源組名稱屬性。</span><span class="sxs-lookup"><span data-stu-id="f3a08-127">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters to enable an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3a08-128">-確認</span><span class="sxs-lookup"><span data-stu-id="f3a08-128">-Confirm</span></span>
<span data-ttu-id="f3a08-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f3a08-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3a08-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3a08-130">-DefaultProfile</span></span>
<span data-ttu-id="f3a08-131">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f3a08-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3a08-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3a08-132">-WhatIf</span></span>
<span data-ttu-id="f3a08-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f3a08-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f3a08-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f3a08-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3a08-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3a08-135">CommonParameters</span></span>
<span data-ttu-id="f3a08-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f3a08-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3a08-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f3a08-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3a08-138">輸入</span><span class="sxs-lookup"><span data-stu-id="f3a08-138">INPUTS</span></span>

## <span data-ttu-id="f3a08-139">輸出</span><span class="sxs-lookup"><span data-stu-id="f3a08-139">OUTPUTS</span></span>

### <span data-ttu-id="f3a08-140">PSActivityLogAlertResource 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="f3a08-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="f3a08-141">筆記</span><span class="sxs-lookup"><span data-stu-id="f3a08-141">NOTES</span></span>

## <span data-ttu-id="f3a08-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="f3a08-142">RELATED LINKS</span></span>

[<span data-ttu-id="f3a08-143">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="f3a08-143">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="f3a08-144">AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="f3a08-144">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="f3a08-145">移除-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="f3a08-145">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="f3a08-146">新-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="f3a08-146">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="f3a08-147">新-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="f3a08-147">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)

[<span data-ttu-id="f3a08-148">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="f3a08-148">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)
