---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azactivitylogalertcondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActivityLogAlertCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActivityLogAlertCondition.md
ms.openlocfilehash: f18479f8cf42c68a7c8a8a5d9f45a4542a758212
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908897"
---
# <span data-ttu-id="e1cff-101">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="e1cff-101">New-AzActivityLogAlertCondition</span></span>

## <span data-ttu-id="e1cff-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e1cff-102">SYNOPSIS</span></span>
<span data-ttu-id="e1cff-103">在記憶體中建立新活動記錄警示條件物件。</span><span class="sxs-lookup"><span data-stu-id="e1cff-103">Creates an new activity log alert condition object in memory.</span></span>

## <span data-ttu-id="e1cff-104">語法</span><span class="sxs-lookup"><span data-stu-id="e1cff-104">SYNTAX</span></span>

```
New-AzActivityLogAlertCondition -Field <String> -Equal <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e1cff-105">描述</span><span class="sxs-lookup"><span data-stu-id="e1cff-105">DESCRIPTION</span></span>
<span data-ttu-id="e1cff-106">**New-AzActivityLogAlertCondition Cmdlet** 會建立記憶體中的新活動記錄警示條件物件。</span><span class="sxs-lookup"><span data-stu-id="e1cff-106">The **New-AzActivityLogAlertCondition** cmdlet creates new activity log alert condition object in memory.</span></span>

## <span data-ttu-id="e1cff-107">例子</span><span class="sxs-lookup"><span data-stu-id="e1cff-107">EXAMPLES</span></span>

### <span data-ttu-id="e1cff-108">範例 1：在記憶體中建立新活動記錄警示條件物件。</span><span class="sxs-lookup"><span data-stu-id="e1cff-108">Example 1: Create a new activity log alert condition object in memory.</span></span>
```
PS C:\>$Condition = New-AzActivityLogAlertCondition -Field "Requests" -Equal "OtherField"
PS C:\>Write-Host "Field property value: $($Condition.Field)"
PS C:\>Write-Host "Equals property value: $($Condition.Equals)"

Field property value: Requests
Equals property value: OtherField
```

<span data-ttu-id="e1cff-109">此命令在記憶體中建立新的活動記錄提醒條件物件。</span><span class="sxs-lookup"><span data-stu-id="e1cff-109">This command creates a new activity log alert condition object in memory.</span></span>
<span data-ttu-id="e1cff-110">**注意**：當此 Cmdlet 與 [Set-AzActivityLogAlert](https://docs.microsoft.com/powershell/module/az.monitor/set-azactivitylogalert) 一起使用時，至少其中一個物件傳遞為參數時，其欄位必須等於 "Category"。</span><span class="sxs-lookup"><span data-stu-id="e1cff-110">**NOTE**: when this cmdlet is used with [Set-AzActivityLogAlert](https://docs.microsoft.com/powershell/module/az.monitor/set-azactivitylogalert) at least one of these objects, passed as parameters, must have its Field equal to "Category".</span></span> <span data-ttu-id="e1cff-111">否則，後端會以 400 (BadRequest.) </span><span class="sxs-lookup"><span data-stu-id="e1cff-111">Otherwise, the backend responds with a 400 (BadRequest.)</span></span>

## <span data-ttu-id="e1cff-112">參數</span><span class="sxs-lookup"><span data-stu-id="e1cff-112">PARAMETERS</span></span>

### <span data-ttu-id="e1cff-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1cff-113">-DefaultProfile</span></span>
<span data-ttu-id="e1cff-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="e1cff-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e1cff-115">-等號</span><span class="sxs-lookup"><span data-stu-id="e1cff-115">-Equal</span></span>
<span data-ttu-id="e1cff-116">指定條件條件之等號屬性。</span><span class="sxs-lookup"><span data-stu-id="e1cff-116">Specifies the equals property for the leaf condition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1cff-117">-功能區</span><span class="sxs-lookup"><span data-stu-id="e1cff-117">-Field</span></span>
<span data-ttu-id="e1cff-118">指定條件欄位。</span><span class="sxs-lookup"><span data-stu-id="e1cff-118">Specifies the field for the condition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1cff-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1cff-119">CommonParameters</span></span>
<span data-ttu-id="e1cff-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e1cff-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1cff-121">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e1cff-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1cff-122">輸入</span><span class="sxs-lookup"><span data-stu-id="e1cff-122">INPUTS</span></span>

### <span data-ttu-id="e1cff-123">System.String</span><span class="sxs-lookup"><span data-stu-id="e1cff-123">System.String</span></span>

## <span data-ttu-id="e1cff-124">輸出</span><span class="sxs-lookup"><span data-stu-id="e1cff-124">OUTPUTS</span></span>

### <span data-ttu-id="e1cff-125">Microsoft.Azure.management.monitor.management.models.ActivityLogAlertLeafCondition</span><span class="sxs-lookup"><span data-stu-id="e1cff-125">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition</span></span>

## <span data-ttu-id="e1cff-126">筆記</span><span class="sxs-lookup"><span data-stu-id="e1cff-126">NOTES</span></span>

## <span data-ttu-id="e1cff-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="e1cff-127">RELATED LINKS</span></span>

[<span data-ttu-id="e1cff-128">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e1cff-128">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="e1cff-129">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e1cff-129">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="e1cff-130">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e1cff-130">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="e1cff-131">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e1cff-131">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="e1cff-132">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e1cff-132">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="e1cff-133">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="e1cff-133">New-AzActionGroup</span></span>](./Get-AzActionGroup.md)
