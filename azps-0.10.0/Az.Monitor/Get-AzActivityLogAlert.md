---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 85492E00-3776-4F20-A444-9C28CC6154B7
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Get-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Get-AzActivityLogAlert.md
ms.openlocfilehash: 31e36048587ba6faeee42ab1c2bf15afe1ae1e71
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398745"
---
# <span data-ttu-id="6a7ce-101">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="6a7ce-101">Get-AzActivityLogAlert</span></span>

## <span data-ttu-id="6a7ce-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6a7ce-102">SYNOPSIS</span></span>
<span data-ttu-id="6a7ce-103">獲得一或多個活動記錄提醒資源。</span><span class="sxs-lookup"><span data-stu-id="6a7ce-103">Gets one or more activity log alert resources.</span></span>

## <span data-ttu-id="6a7ce-104">語法</span><span class="sxs-lookup"><span data-stu-id="6a7ce-104">SYNTAX</span></span>

### <span data-ttu-id="6a7ce-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6a7ce-105">GetByNameAndResourceGroup</span></span>
```
Get-AzActivityLogAlert [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a7ce-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6a7ce-106">GetByResourceGroup</span></span>
```
Get-AzActivityLogAlert [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6a7ce-107">描述</span><span class="sxs-lookup"><span data-stu-id="6a7ce-107">DESCRIPTION</span></span>
<span data-ttu-id="6a7ce-108">**Get-AzActivityLogAlert** Cmdlet 會取得一或多個活動記錄提醒資源。</span><span class="sxs-lookup"><span data-stu-id="6a7ce-108">The **Get-AzActivityLogAlert** cmdlet gets one or more activity log alert resources.</span></span>

## <span data-ttu-id="6a7ce-109">例子</span><span class="sxs-lookup"><span data-stu-id="6a7ce-109">EXAMPLES</span></span>

### <span data-ttu-id="6a7ce-110">範例 1：根據訂閱識別碼取得活動記錄提醒</span><span class="sxs-lookup"><span data-stu-id="6a7ce-110">Example 1: Get a activity log alerts by subscription ID</span></span>
```
PS C:\>Get-AzActivityLogAlert
```

<span data-ttu-id="6a7ce-111">此命令會列出目前訂閱的所有活動記錄通知。</span><span class="sxs-lookup"><span data-stu-id="6a7ce-111">This command lists all the activity log alerts for the current subscription.</span></span>

### <span data-ttu-id="6a7ce-112">範例 2：取得給定資源群組的活動記錄提醒</span><span class="sxs-lookup"><span data-stu-id="6a7ce-112">Example 2: Get activity log alerts for the given resource group</span></span>
```
PS C:\>Get-AzActivityLogAlert -ResourceGroupName "Default-activityLogAlerts"
```

<span data-ttu-id="6a7ce-113">此命令會列出給定資源群組的活動記錄通知。</span><span class="sxs-lookup"><span data-stu-id="6a7ce-113">This command lists activity log alerts for the given resource group.</span></span>

### <span data-ttu-id="6a7ce-114">範例 3：取得活動記錄提醒。</span><span class="sxs-lookup"><span data-stu-id="6a7ce-114">Example 3: Get an activity log alert.</span></span>
```
PS C:\>Get-AzActivityLogAlert -ResourceGroupName "Default-activityLogAlerts" -Name "alert1"
```

<span data-ttu-id="6a7ce-115">此命令會列出一 (活動記錄提醒的單一) 清單。</span><span class="sxs-lookup"><span data-stu-id="6a7ce-115">This command lists one (a list with a single element) activity log alert.</span></span>

## <span data-ttu-id="6a7ce-116">參數</span><span class="sxs-lookup"><span data-stu-id="6a7ce-116">PARAMETERS</span></span>

### <span data-ttu-id="6a7ce-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a7ce-117">-DefaultProfile</span></span>
<span data-ttu-id="6a7ce-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="6a7ce-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6a7ce-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="6a7ce-119">-Name</span></span>
<span data-ttu-id="6a7ce-120">活動記錄提醒的名稱。</span><span class="sxs-lookup"><span data-stu-id="6a7ce-120">The name of the activity log alert.</span></span>

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

### <span data-ttu-id="6a7ce-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a7ce-121">-ResourceGroupName</span></span>
<span data-ttu-id="6a7ce-122">警示資源存在之資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6a7ce-122">The name of the resource group where the alert resource exists.</span></span>
<span data-ttu-id="6a7ce-123">如果 Name 不是 Null 或空值，此參數必須包含非空字串。</span><span class="sxs-lookup"><span data-stu-id="6a7ce-123">If Name is not null or empty, this parameter must contain and non empty string.</span></span>

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

### <span data-ttu-id="6a7ce-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a7ce-124">CommonParameters</span></span>
<span data-ttu-id="6a7ce-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6a7ce-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a7ce-126">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6a7ce-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a7ce-127">輸入</span><span class="sxs-lookup"><span data-stu-id="6a7ce-127">INPUTS</span></span>

### <span data-ttu-id="6a7ce-128">System.String</span><span class="sxs-lookup"><span data-stu-id="6a7ce-128">System.String</span></span>

## <span data-ttu-id="6a7ce-129">輸出</span><span class="sxs-lookup"><span data-stu-id="6a7ce-129">OUTPUTS</span></span>

### <span data-ttu-id="6a7ce-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="6a7ce-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="6a7ce-131">筆記</span><span class="sxs-lookup"><span data-stu-id="6a7ce-131">NOTES</span></span>

## <span data-ttu-id="6a7ce-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="6a7ce-132">RELATED LINKS</span></span>

[<span data-ttu-id="6a7ce-133">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="6a7ce-133">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="6a7ce-134">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="6a7ce-134">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="6a7ce-135">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="6a7ce-135">New-AzActionGroup</span></span>](./New-AzActionGroup.md)
