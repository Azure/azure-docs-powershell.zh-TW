---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/enable-azurermactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Enable-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Enable-AzureRmActivityLogAlert.md
ms.openlocfilehash: 67d1b91c58793560f619c4d69e2e957d30f37758
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452248"
---
# <span data-ttu-id="a33db-101">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="a33db-101">Enable-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="a33db-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a33db-102">SYNOPSIS</span></span>
<span data-ttu-id="a33db-103">啟用活動記錄通知並設定其標記。</span><span class="sxs-lookup"><span data-stu-id="a33db-103">Enables an activity log alert and sets its Tags.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a33db-104">句法</span><span class="sxs-lookup"><span data-stu-id="a33db-104">SYNTAX</span></span>

### <span data-ttu-id="a33db-105">EnableByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a33db-105">EnableByNameAndResourceGroup</span></span>
```
Enable-AzureRmActivityLogAlert -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a33db-106">EnableByInputObject</span><span class="sxs-lookup"><span data-stu-id="a33db-106">EnableByInputObject</span></span>
```
Enable-AzureRmActivityLogAlert -InputObject <PSActivityLogAlertResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a33db-107">EnableByResourceId</span><span class="sxs-lookup"><span data-stu-id="a33db-107">EnableByResourceId</span></span>
```
Enable-AzureRmActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a33db-108">說明</span><span class="sxs-lookup"><span data-stu-id="a33db-108">DESCRIPTION</span></span>
<span data-ttu-id="a33db-109">**Enable-AzureRmActivityLogAlert** Cmdlet 可啟用活動記錄通知並設定其標記。</span><span class="sxs-lookup"><span data-stu-id="a33db-109">The **Enable-AzureRmActivityLogAlert** cmdlet allows enabling an activity log alert and setting its tags.</span></span>
<span data-ttu-id="a33db-110">這個 Cmdlet 會實現 ShouldProcess 模式，亦即，在實際修補資源之前，它可能會要求使用者進行確認。</span><span class="sxs-lookup"><span data-stu-id="a33db-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="a33db-111">示例</span><span class="sxs-lookup"><span data-stu-id="a33db-111">EXAMPLES</span></span>

### <span data-ttu-id="a33db-112">範例1：停用活動記錄通知</span><span class="sxs-lookup"><span data-stu-id="a33db-112">Example 1: Disable an activity log alert</span></span>
```
PS C:\>Enable-AzureRmActivityLogAlert -Name "alert1" -ResourceGroupName "Default-ActivityLogsAlerts"
```

<span data-ttu-id="a33db-113">這個命令會在資源群組預設-ActivityLogsAlerts 中啟用稱為 alert1 的活動記錄提醒。</span><span class="sxs-lookup"><span data-stu-id="a33db-113">This command enables the activity log alert called alert1 in the resource group Default-ActivityLogsAlerts.</span></span>

### <span data-ttu-id="a33db-114">範例2：使用 PSActivityLogAlertResource 物件做為輸入來啟用活動記錄提醒</span><span class="sxs-lookup"><span data-stu-id="a33db-114">Example 2: Enable an activity log alert using a PSActivityLogAlertResource object as input</span></span>
```
PS C:\>$obj = Get-AzureRmActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1"
PS C:\>Enable-AzureRmActivityLogAlert -InputObject $obj
```

<span data-ttu-id="a33db-115">這個命令會啟用稱為 alert1 的活動記錄提醒。</span><span class="sxs-lookup"><span data-stu-id="a33db-115">This command enables an activity log alert called alert1.</span></span> <span data-ttu-id="a33db-116">針對這種情況，它會使用 PSActivityLogAlertResource 物件做為輸入引數。</span><span class="sxs-lookup"><span data-stu-id="a33db-116">For this it uses a PSActivityLogAlertResource object as input argument.</span></span>

### <span data-ttu-id="a33db-117">範例3：使用 ResourceId 參數啟用 ActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="a33db-117">Example 3: Enable the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Find-AzureRmResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Enable-AzureRmActivityLogAlert
```

<span data-ttu-id="a33db-118">這個命令會從管道使用 ResourceId 參數來啟用 ActivityLogAlert。</span><span class="sxs-lookup"><span data-stu-id="a33db-118">This command enables the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="a33db-119">參數</span><span class="sxs-lookup"><span data-stu-id="a33db-119">PARAMETERS</span></span>

### <span data-ttu-id="a33db-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a33db-120">-DefaultProfile</span></span>
<span data-ttu-id="a33db-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="a33db-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a33db-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a33db-122">-InputObject</span></span>
<span data-ttu-id="a33db-123">設定通話的 InputObject tags 屬性來解壓縮所需的名稱、資源組名稱，以及選用的標記屬性。</span><span class="sxs-lookup"><span data-stu-id="a33db-123">Sets the InputObject tags property of the call to extract the required name, resource group name, and the optional tags properties.</span></span>

```yaml
Type: PSActivityLogAlertResource
Parameter Sets: EnableByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a33db-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="a33db-124">-Name</span></span>
<span data-ttu-id="a33db-125">活動記錄通知的名稱。</span><span class="sxs-lookup"><span data-stu-id="a33db-125">The name of the activity log alert.</span></span>

```yaml
Type: String
Parameter Sets: EnableByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a33db-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a33db-126">-ResourceGroupName</span></span>
<span data-ttu-id="a33db-127">要在其中存在預警資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a33db-127">The name of the resource group where the alert resource is going to exist.</span></span>

```yaml
Type: String
Parameter Sets: EnableByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a33db-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a33db-128">-ResourceId</span></span>
<span data-ttu-id="a33db-129">設定呼叫的 ResourceId 標籤屬性來解壓縮所需的名稱、資源組名稱屬性。</span><span class="sxs-lookup"><span data-stu-id="a33db-129">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: String
Parameter Sets: EnableByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a33db-130">-確認</span><span class="sxs-lookup"><span data-stu-id="a33db-130">-Confirm</span></span>
<span data-ttu-id="a33db-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a33db-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a33db-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a33db-132">-WhatIf</span></span>
<span data-ttu-id="a33db-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a33db-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a33db-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a33db-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a33db-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a33db-135">CommonParameters</span></span>
<span data-ttu-id="a33db-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a33db-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a33db-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a33db-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a33db-138">輸入</span><span class="sxs-lookup"><span data-stu-id="a33db-138">INPUTS</span></span>

### <span data-ttu-id="a33db-139">所有</span><span class="sxs-lookup"><span data-stu-id="a33db-139">None</span></span>
<span data-ttu-id="a33db-140">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="a33db-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a33db-141">輸出</span><span class="sxs-lookup"><span data-stu-id="a33db-141">OUTPUTS</span></span>

### <span data-ttu-id="a33db-142">PSActivityLogAlertResource 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="a33db-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="a33db-143">筆記</span><span class="sxs-lookup"><span data-stu-id="a33db-143">NOTES</span></span>

## <span data-ttu-id="a33db-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="a33db-144">RELATED LINKS</span></span>

[<span data-ttu-id="a33db-145">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="a33db-145">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="a33db-146">AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="a33db-146">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="a33db-147">移除-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="a33db-147">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="a33db-148">新-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="a33db-148">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="a33db-149">新-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="a33db-149">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)

[<span data-ttu-id="a33db-150">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="a33db-150">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)
