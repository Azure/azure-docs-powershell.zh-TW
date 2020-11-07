---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 85492E00-3776-4F20-A444-9C28CC6154B7
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLogAlert.md
ms.openlocfilehash: a40116e0c244b6017d21678a8c09182fa4e2376e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93966453"
---
# <span data-ttu-id="466d1-101">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="466d1-101">Get-AzActivityLogAlert</span></span>

## <span data-ttu-id="466d1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="466d1-102">SYNOPSIS</span></span>
<span data-ttu-id="466d1-103">取得一或多個活動記錄通知資源。</span><span class="sxs-lookup"><span data-stu-id="466d1-103">Gets one or more activity log alert resources.</span></span>

## <span data-ttu-id="466d1-104">句法</span><span class="sxs-lookup"><span data-stu-id="466d1-104">SYNTAX</span></span>

### <span data-ttu-id="466d1-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="466d1-105">GetByNameAndResourceGroup</span></span>
```
Get-AzActivityLogAlert [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="466d1-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="466d1-106">GetByResourceGroup</span></span>
```
Get-AzActivityLogAlert [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="466d1-107">說明</span><span class="sxs-lookup"><span data-stu-id="466d1-107">DESCRIPTION</span></span>
<span data-ttu-id="466d1-108">**AzActivityLogAlert** Cmdlet 會取得一或多個活動記錄通知資源。</span><span class="sxs-lookup"><span data-stu-id="466d1-108">The **Get-AzActivityLogAlert** cmdlet gets one or more activity log alert resources.</span></span>

## <span data-ttu-id="466d1-109">示例</span><span class="sxs-lookup"><span data-stu-id="466d1-109">EXAMPLES</span></span>

### <span data-ttu-id="466d1-110">範例1：依訂閱識別碼取得活動記錄通知</span><span class="sxs-lookup"><span data-stu-id="466d1-110">Example 1: Get a activity log alerts by subscription ID</span></span>
```
PS C:\>Get-AzActivityLogAlert
```

<span data-ttu-id="466d1-111">這個命令會列出目前訂閱的所有活動記錄通知。</span><span class="sxs-lookup"><span data-stu-id="466d1-111">This command lists all the activity log alerts for the current subscription.</span></span>

### <span data-ttu-id="466d1-112">範例2：取得特定資源群組的活動記錄警報</span><span class="sxs-lookup"><span data-stu-id="466d1-112">Example 2: Get activity log alerts for the given resource group</span></span>
```
PS C:\>Get-AzActivityLogAlert -ResourceGroupName "Default-activityLogAlerts"
```

<span data-ttu-id="466d1-113">這個命令會列出特定資源群組的活動記錄通知。</span><span class="sxs-lookup"><span data-stu-id="466d1-113">This command lists activity log alerts for the given resource group.</span></span>

### <span data-ttu-id="466d1-114">範例3：取得活動記錄警示。</span><span class="sxs-lookup"><span data-stu-id="466d1-114">Example 3: Get an activity log alert.</span></span>
```
PS C:\>Get-AzActivityLogAlert -ResourceGroupName "Default-activityLogAlerts" -Name "alert1"
```

<span data-ttu-id="466d1-115">這個命令會列出一個 (清單，其中只有一個元素) 活動記錄通知。</span><span class="sxs-lookup"><span data-stu-id="466d1-115">This command lists one (a list with a single element) activity log alert.</span></span>

## <span data-ttu-id="466d1-116">參數</span><span class="sxs-lookup"><span data-stu-id="466d1-116">PARAMETERS</span></span>

### <span data-ttu-id="466d1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="466d1-117">-DefaultProfile</span></span>
<span data-ttu-id="466d1-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="466d1-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="466d1-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="466d1-119">-Name</span></span>
<span data-ttu-id="466d1-120">活動記錄通知的名稱。</span><span class="sxs-lookup"><span data-stu-id="466d1-120">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="466d1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="466d1-121">-ResourceGroupName</span></span>
<span data-ttu-id="466d1-122">警示資源所在之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="466d1-122">The name of the resource group where the alert resource exists.</span></span>
<span data-ttu-id="466d1-123">如果 Name 不是 null 或空，此參數必須包含且非空字串。</span><span class="sxs-lookup"><span data-stu-id="466d1-123">If Name is not null or empty, this parameter must contain and non empty string.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="466d1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="466d1-124">CommonParameters</span></span>
<span data-ttu-id="466d1-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="466d1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="466d1-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="466d1-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="466d1-127">輸入</span><span class="sxs-lookup"><span data-stu-id="466d1-127">INPUTS</span></span>

### <span data-ttu-id="466d1-128">System.object</span><span class="sxs-lookup"><span data-stu-id="466d1-128">System.String</span></span>

## <span data-ttu-id="466d1-129">輸出</span><span class="sxs-lookup"><span data-stu-id="466d1-129">OUTPUTS</span></span>

### <span data-ttu-id="466d1-130">PSActivityLogAlertResource 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="466d1-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="466d1-131">筆記</span><span class="sxs-lookup"><span data-stu-id="466d1-131">NOTES</span></span>

## <span data-ttu-id="466d1-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="466d1-132">RELATED LINKS</span></span>

[<span data-ttu-id="466d1-133">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="466d1-133">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="466d1-134">更新-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="466d1-134">Update-AzActivityLogAlert</span></span>](./Update-AzActivityLogAlert.md)

[<span data-ttu-id="466d1-135">移除-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="466d1-135">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="466d1-136">新-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="466d1-136">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="466d1-137">新-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="466d1-137">New-AzActivityLogAlertCondition</span></span>](./Get-AzActivityLogAlertCondition.md)
