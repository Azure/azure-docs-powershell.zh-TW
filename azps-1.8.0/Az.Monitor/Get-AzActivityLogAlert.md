---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 85492E00-3776-4F20-A444-9C28CC6154B7
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLogAlert.md
ms.openlocfilehash: 93112c8e7518ac23b23e5b1bb6c18109481495dc
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100403148"
---
# <span data-ttu-id="ed4f2-101">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="ed4f2-101">Get-AzActivityLogAlert</span></span>

## <span data-ttu-id="ed4f2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ed4f2-102">SYNOPSIS</span></span>
<span data-ttu-id="ed4f2-103">獲得一或多個活動記錄提醒資源。</span><span class="sxs-lookup"><span data-stu-id="ed4f2-103">Gets one or more activity log alert resources.</span></span>

## <span data-ttu-id="ed4f2-104">語法</span><span class="sxs-lookup"><span data-stu-id="ed4f2-104">SYNTAX</span></span>

### <span data-ttu-id="ed4f2-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ed4f2-105">GetByNameAndResourceGroup</span></span>
```
Get-AzActivityLogAlert [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed4f2-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ed4f2-106">GetByResourceGroup</span></span>
```
Get-AzActivityLogAlert [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ed4f2-107">描述</span><span class="sxs-lookup"><span data-stu-id="ed4f2-107">DESCRIPTION</span></span>
<span data-ttu-id="ed4f2-108">**Get-AzActivityLogAlert** Cmdlet 會取得一或多個活動記錄提醒資源。</span><span class="sxs-lookup"><span data-stu-id="ed4f2-108">The **Get-AzActivityLogAlert** cmdlet gets one or more activity log alert resources.</span></span>

## <span data-ttu-id="ed4f2-109">例子</span><span class="sxs-lookup"><span data-stu-id="ed4f2-109">EXAMPLES</span></span>

### <span data-ttu-id="ed4f2-110">範例 1：根據訂閱識別碼取得活動記錄提醒</span><span class="sxs-lookup"><span data-stu-id="ed4f2-110">Example 1: Get a activity log alerts by subscription ID</span></span>
```
PS C:\>Get-AzActivityLogAlert
```

<span data-ttu-id="ed4f2-111">此命令會列出目前訂閱的所有活動記錄通知。</span><span class="sxs-lookup"><span data-stu-id="ed4f2-111">This command lists all the activity log alerts for the current subscription.</span></span>

### <span data-ttu-id="ed4f2-112">範例 2：取得給定資源群組的活動記錄提醒</span><span class="sxs-lookup"><span data-stu-id="ed4f2-112">Example 2: Get activity log alerts for the given resource group</span></span>
```
PS C:\>Get-AzActivityLogAlert -ResourceGroupName "Default-activityLogAlerts"
```

<span data-ttu-id="ed4f2-113">此命令會列出給定資源群組的活動記錄通知。</span><span class="sxs-lookup"><span data-stu-id="ed4f2-113">This command lists activity log alerts for the given resource group.</span></span>

### <span data-ttu-id="ed4f2-114">範例 3：取得活動記錄提醒。</span><span class="sxs-lookup"><span data-stu-id="ed4f2-114">Example 3: Get an activity log alert.</span></span>
```
PS C:\>Get-AzActivityLogAlert -ResourceGroupName "Default-activityLogAlerts" -Name "alert1"
```

<span data-ttu-id="ed4f2-115">此命令會列出一 (活動記錄提醒的單一) 清單。</span><span class="sxs-lookup"><span data-stu-id="ed4f2-115">This command lists one (a list with a single element) activity log alert.</span></span>

## <span data-ttu-id="ed4f2-116">參數</span><span class="sxs-lookup"><span data-stu-id="ed4f2-116">PARAMETERS</span></span>

### <span data-ttu-id="ed4f2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed4f2-117">-DefaultProfile</span></span>
<span data-ttu-id="ed4f2-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="ed4f2-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ed4f2-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="ed4f2-119">-Name</span></span>
<span data-ttu-id="ed4f2-120">活動記錄提醒的名稱。</span><span class="sxs-lookup"><span data-stu-id="ed4f2-120">The name of the activity log alert.</span></span>

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

### <span data-ttu-id="ed4f2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed4f2-121">-ResourceGroupName</span></span>
<span data-ttu-id="ed4f2-122">警示資源存在之資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ed4f2-122">The name of the resource group where the alert resource exists.</span></span>
<span data-ttu-id="ed4f2-123">如果 Name 不是 Null 或空值，此參數必須包含非空字串。</span><span class="sxs-lookup"><span data-stu-id="ed4f2-123">If Name is not null or empty, this parameter must contain and non empty string.</span></span>

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

### <span data-ttu-id="ed4f2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed4f2-124">CommonParameters</span></span>
<span data-ttu-id="ed4f2-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ed4f2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed4f2-126">詳細資訊請參閱 https://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="ed4f2-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed4f2-127">輸入</span><span class="sxs-lookup"><span data-stu-id="ed4f2-127">INPUTS</span></span>

### <span data-ttu-id="ed4f2-128">System.String</span><span class="sxs-lookup"><span data-stu-id="ed4f2-128">System.String</span></span>

## <span data-ttu-id="ed4f2-129">輸出</span><span class="sxs-lookup"><span data-stu-id="ed4f2-129">OUTPUTS</span></span>

### <span data-ttu-id="ed4f2-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="ed4f2-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="ed4f2-131">筆記</span><span class="sxs-lookup"><span data-stu-id="ed4f2-131">NOTES</span></span>

## <span data-ttu-id="ed4f2-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="ed4f2-132">RELATED LINKS</span></span>

[<span data-ttu-id="ed4f2-133">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="ed4f2-133">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="ed4f2-134">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="ed4f2-134">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="ed4f2-135">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="ed4f2-135">New-AzActionGroup</span></span>](./New-AzActionGroup.md)
