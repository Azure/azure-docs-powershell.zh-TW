---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 85492E00-3776-4F20-A444-9C28CC6154B7
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLogAlert.md
ms.openlocfilehash: 26a1fbcc2016de2e6eca4cff2ee2442ef0111919
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93786753"
---
# <span data-ttu-id="2bdc4-101">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="2bdc4-101">Get-AzActivityLogAlert</span></span>

## <span data-ttu-id="2bdc4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2bdc4-102">SYNOPSIS</span></span>
<span data-ttu-id="2bdc4-103">取得一或多個活動記錄通知資源。</span><span class="sxs-lookup"><span data-stu-id="2bdc4-103">Gets one or more activity log alert resources.</span></span>

## <span data-ttu-id="2bdc4-104">句法</span><span class="sxs-lookup"><span data-stu-id="2bdc4-104">SYNTAX</span></span>

### <span data-ttu-id="2bdc4-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2bdc4-105">GetByNameAndResourceGroup</span></span>
```
Get-AzActivityLogAlert [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2bdc4-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2bdc4-106">GetByResourceGroup</span></span>
```
Get-AzActivityLogAlert [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2bdc4-107">說明</span><span class="sxs-lookup"><span data-stu-id="2bdc4-107">DESCRIPTION</span></span>
<span data-ttu-id="2bdc4-108">**AzActivityLogAlert** Cmdlet 會取得一或多個活動記錄通知資源。</span><span class="sxs-lookup"><span data-stu-id="2bdc4-108">The **Get-AzActivityLogAlert** cmdlet gets one or more activity log alert resources.</span></span>

## <span data-ttu-id="2bdc4-109">示例</span><span class="sxs-lookup"><span data-stu-id="2bdc4-109">EXAMPLES</span></span>

### <span data-ttu-id="2bdc4-110">範例1：依訂閱識別碼取得活動記錄通知</span><span class="sxs-lookup"><span data-stu-id="2bdc4-110">Example 1: Get a activity log alerts by subscription ID</span></span>
```
PS C:\>Get-AzActivityLogAlert
```

<span data-ttu-id="2bdc4-111">這個命令會列出目前訂閱的所有活動記錄通知。</span><span class="sxs-lookup"><span data-stu-id="2bdc4-111">This command lists all the activity log alerts for the current subscription.</span></span>

### <span data-ttu-id="2bdc4-112">範例2：取得特定資源群組的活動記錄警報</span><span class="sxs-lookup"><span data-stu-id="2bdc4-112">Example 2: Get activity log alerts for the given resource group</span></span>
```
PS C:\>Get-AzActivityLogAlert -ResourceGroupName "Default-activityLogAlerts"
```

<span data-ttu-id="2bdc4-113">這個命令會列出特定資源群組的活動記錄通知。</span><span class="sxs-lookup"><span data-stu-id="2bdc4-113">This command lists activity log alerts for the given resource group.</span></span>

### <span data-ttu-id="2bdc4-114">範例3：取得活動記錄警示。</span><span class="sxs-lookup"><span data-stu-id="2bdc4-114">Example 3: Get an activity log alert.</span></span>
```
PS C:\>Get-AzActivityLogAlert -ResourceGroupName "Default-activityLogAlerts" -Name "alert1"
```

<span data-ttu-id="2bdc4-115">這個命令會列出一個 (清單，其中只有一個元素) 活動記錄通知。</span><span class="sxs-lookup"><span data-stu-id="2bdc4-115">This command lists one (a list with a single element) activity log alert.</span></span>

## <span data-ttu-id="2bdc4-116">參數</span><span class="sxs-lookup"><span data-stu-id="2bdc4-116">PARAMETERS</span></span>

### <span data-ttu-id="2bdc4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bdc4-117">-DefaultProfile</span></span>
<span data-ttu-id="2bdc4-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="2bdc4-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2bdc4-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="2bdc4-119">-Name</span></span>
<span data-ttu-id="2bdc4-120">活動記錄通知的名稱。</span><span class="sxs-lookup"><span data-stu-id="2bdc4-120">The name of the activity log alert.</span></span>

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

### <span data-ttu-id="2bdc4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bdc4-121">-ResourceGroupName</span></span>
<span data-ttu-id="2bdc4-122">警示資源所在之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2bdc4-122">The name of the resource group where the alert resource exists.</span></span>
<span data-ttu-id="2bdc4-123">如果 Name 不是 null 或空，此參數必須包含且非空字串。</span><span class="sxs-lookup"><span data-stu-id="2bdc4-123">If Name is not null or empty, this parameter must contain and non empty string.</span></span>

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

### <span data-ttu-id="2bdc4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bdc4-124">CommonParameters</span></span>
<span data-ttu-id="2bdc4-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2bdc4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bdc4-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2bdc4-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bdc4-127">輸入</span><span class="sxs-lookup"><span data-stu-id="2bdc4-127">INPUTS</span></span>

### <span data-ttu-id="2bdc4-128">System.object</span><span class="sxs-lookup"><span data-stu-id="2bdc4-128">System.String</span></span>

## <span data-ttu-id="2bdc4-129">輸出</span><span class="sxs-lookup"><span data-stu-id="2bdc4-129">OUTPUTS</span></span>

### <span data-ttu-id="2bdc4-130">PSActivityLogAlertResource 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="2bdc4-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="2bdc4-131">筆記</span><span class="sxs-lookup"><span data-stu-id="2bdc4-131">NOTES</span></span>

## <span data-ttu-id="2bdc4-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="2bdc4-132">RELATED LINKS</span></span>

[<span data-ttu-id="2bdc4-133">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="2bdc4-133">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="2bdc4-134">更新-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="2bdc4-134">Update-AzActivityLogAlert</span></span>](./Update-AzActivityLogAlert.md)

[<span data-ttu-id="2bdc4-135">移除-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="2bdc4-135">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="2bdc4-136">新-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="2bdc4-136">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="2bdc4-137">新-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="2bdc4-137">New-AzActivityLogAlertCondition</span></span>](./Get-AzActivityLogAlertCondition.md)
