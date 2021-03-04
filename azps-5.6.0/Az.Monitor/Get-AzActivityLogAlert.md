---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 85492E00-3776-4F20-A444-9C28CC6154B7
online version: https://docs.microsoft.com/powershell/module/az.monitor/get-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLogAlert.md
ms.openlocfilehash: 526b03fb1d73ab88b43929df143e9825f42c7fdf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908974"
---
# <span data-ttu-id="5bd4d-101">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="5bd4d-101">Get-AzActivityLogAlert</span></span>

## <span data-ttu-id="5bd4d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5bd4d-102">SYNOPSIS</span></span>
<span data-ttu-id="5bd4d-103">獲得一或多個活動記錄提醒資源。</span><span class="sxs-lookup"><span data-stu-id="5bd4d-103">Gets one or more activity log alert resources.</span></span>

## <span data-ttu-id="5bd4d-104">語法</span><span class="sxs-lookup"><span data-stu-id="5bd4d-104">SYNTAX</span></span>

### <span data-ttu-id="5bd4d-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5bd4d-105">GetByNameAndResourceGroup</span></span>
```
Get-AzActivityLogAlert [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5bd4d-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5bd4d-106">GetByResourceGroup</span></span>
```
Get-AzActivityLogAlert [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5bd4d-107">描述</span><span class="sxs-lookup"><span data-stu-id="5bd4d-107">DESCRIPTION</span></span>
<span data-ttu-id="5bd4d-108">**Get-AzActivityLogAlert** Cmdlet 會取得一或多個活動記錄提醒資源。</span><span class="sxs-lookup"><span data-stu-id="5bd4d-108">The **Get-AzActivityLogAlert** cmdlet gets one or more activity log alert resources.</span></span>

## <span data-ttu-id="5bd4d-109">例子</span><span class="sxs-lookup"><span data-stu-id="5bd4d-109">EXAMPLES</span></span>

### <span data-ttu-id="5bd4d-110">範例 1：根據訂閱識別碼取得活動記錄提醒</span><span class="sxs-lookup"><span data-stu-id="5bd4d-110">Example 1: Get a activity log alerts by subscription ID</span></span>
```
PS C:\>Get-AzActivityLogAlert
```

<span data-ttu-id="5bd4d-111">此命令會列出目前訂閱的所有活動記錄通知。</span><span class="sxs-lookup"><span data-stu-id="5bd4d-111">This command lists all the activity log alerts for the current subscription.</span></span>

### <span data-ttu-id="5bd4d-112">範例 2：取得給定資源群組的活動記錄提醒</span><span class="sxs-lookup"><span data-stu-id="5bd4d-112">Example 2: Get activity log alerts for the given resource group</span></span>
```
PS C:\>Get-AzActivityLogAlert -ResourceGroupName "Default-activityLogAlerts"
```

<span data-ttu-id="5bd4d-113">此命令會列出給定資源群組的活動記錄通知。</span><span class="sxs-lookup"><span data-stu-id="5bd4d-113">This command lists activity log alerts for the given resource group.</span></span>

### <span data-ttu-id="5bd4d-114">範例 3：取得活動記錄提醒。</span><span class="sxs-lookup"><span data-stu-id="5bd4d-114">Example 3: Get an activity log alert.</span></span>
```
PS C:\>Get-AzActivityLogAlert -ResourceGroupName "Default-activityLogAlerts" -Name "alert1"
```

<span data-ttu-id="5bd4d-115">此命令會列出一 (活動記錄提醒的單一) 清單。</span><span class="sxs-lookup"><span data-stu-id="5bd4d-115">This command lists one (a list with a single element) activity log alert.</span></span>

## <span data-ttu-id="5bd4d-116">參數</span><span class="sxs-lookup"><span data-stu-id="5bd4d-116">PARAMETERS</span></span>

### <span data-ttu-id="5bd4d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bd4d-117">-DefaultProfile</span></span>
<span data-ttu-id="5bd4d-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="5bd4d-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5bd4d-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="5bd4d-119">-Name</span></span>
<span data-ttu-id="5bd4d-120">活動記錄提醒的名稱。</span><span class="sxs-lookup"><span data-stu-id="5bd4d-120">The name of the activity log alert.</span></span>

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

### <span data-ttu-id="5bd4d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bd4d-121">-ResourceGroupName</span></span>
<span data-ttu-id="5bd4d-122">警示資源存在之資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5bd4d-122">The name of the resource group where the alert resource exists.</span></span>
<span data-ttu-id="5bd4d-123">如果 Name 不是 Null 或空值，此參數必須包含非空字串。</span><span class="sxs-lookup"><span data-stu-id="5bd4d-123">If Name is not null or empty, this parameter must contain and non empty string.</span></span>

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

### <span data-ttu-id="5bd4d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bd4d-124">CommonParameters</span></span>
<span data-ttu-id="5bd4d-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5bd4d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bd4d-126">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5bd4d-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bd4d-127">輸入</span><span class="sxs-lookup"><span data-stu-id="5bd4d-127">INPUTS</span></span>

### <span data-ttu-id="5bd4d-128">System.String</span><span class="sxs-lookup"><span data-stu-id="5bd4d-128">System.String</span></span>

## <span data-ttu-id="5bd4d-129">輸出</span><span class="sxs-lookup"><span data-stu-id="5bd4d-129">OUTPUTS</span></span>

### <span data-ttu-id="5bd4d-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="5bd4d-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="5bd4d-131">筆記</span><span class="sxs-lookup"><span data-stu-id="5bd4d-131">NOTES</span></span>

## <span data-ttu-id="5bd4d-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="5bd4d-132">RELATED LINKS</span></span>

[<span data-ttu-id="5bd4d-133">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="5bd4d-133">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="5bd4d-134">Update-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="5bd4d-134">Update-AzActivityLogAlert</span></span>](./Update-AzActivityLogAlert.md)

[<span data-ttu-id="5bd4d-135">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="5bd4d-135">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="5bd4d-136">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="5bd4d-136">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="5bd4d-137">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="5bd4d-137">New-AzActivityLogAlertCondition</span></span>](./New-AzActivityLogAlertCondition.md)
