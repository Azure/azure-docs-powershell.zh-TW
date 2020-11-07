---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/stop-azsdiskmigrationjob
schema: 2.0.0
ms.openlocfilehash: bb5c78d6c0ae29d415e02d3e78e79f963bc3315c
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/24/2020
ms.locfileid: "93966803"
---
# <span data-ttu-id="dda91-101">Stop-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="dda91-101">Stop-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="dda91-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dda91-102">SYNOPSIS</span></span>
<span data-ttu-id="dda91-103">取消磁片遷移作業。</span><span class="sxs-lookup"><span data-stu-id="dda91-103">Cancel a disk migration job.</span></span>

## <span data-ttu-id="dda91-104">句法</span><span class="sxs-lookup"><span data-stu-id="dda91-104">SYNTAX</span></span>

```
Stop-AzsDiskMigrationJob -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="dda91-105">說明</span><span class="sxs-lookup"><span data-stu-id="dda91-105">DESCRIPTION</span></span>
<span data-ttu-id="dda91-106">取消磁片遷移作業。</span><span class="sxs-lookup"><span data-stu-id="dda91-106">Cancel a disk migration job.</span></span>

## <span data-ttu-id="dda91-107">示例</span><span class="sxs-lookup"><span data-stu-id="dda91-107">EXAMPLES</span></span>

### <span data-ttu-id="dda91-108">範例1：</span><span class="sxs-lookup"><span data-stu-id="dda91-108">Example 1:</span></span>
```powershell
PS C:\> Stop-AzsDiskMigrationJob -Name TestJob

CreationTime : 2/26/2020 11:06:40 AM
EndTime      : 2/26/2020 11:07:24 AM
Id           : /subscriptions/627fecef-520e-4c18-94e0-8f0665ba86a7/providers/Microsoft.Compute.Admin/locations/redmond/diskmigrati
               onjobs/TestJob
Location     : redmond
MigrationId  : TestJob
Name         : redmond/TestJob
StartTime    : 2/26/2020 11:06:40 AM
Status       : Canceled
Subtask      : {47774498-6bc7-4ce2-98ca-738739ded2fc, b09ac623-f71d-480c-98bc-88fa3f603f2c}
TargetShare  : \\SU1FileServer.s31r1801.masd.stbtest.microsoft.com\SU1_ObjStore_4
Type         : Microsoft.Compute.Admin/locations/diskmigrationjobs
```

<span data-ttu-id="dda91-109">取消受管理的磁片遷移作業。</span><span class="sxs-lookup"><span data-stu-id="dda91-109">Cancel a managed disk migration job.</span></span>

## <span data-ttu-id="dda91-110">參數</span><span class="sxs-lookup"><span data-stu-id="dda91-110">PARAMETERS</span></span>

### <span data-ttu-id="dda91-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dda91-111">-DefaultProfile</span></span>
<span data-ttu-id="dda91-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dda91-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="dda91-113">-位置</span><span class="sxs-lookup"><span data-stu-id="dda91-113">-Location</span></span>
<span data-ttu-id="dda91-114">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="dda91-114">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="dda91-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="dda91-115">-Name</span></span>
<span data-ttu-id="dda91-116">[遷移作業 guid] 名稱。</span><span class="sxs-lookup"><span data-stu-id="dda91-116">The migration job guid name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MigrationId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="dda91-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dda91-117">-SubscriptionId</span></span>
<span data-ttu-id="dda91-118">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="dda91-118">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="dda91-119">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="dda91-119">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="dda91-120">-確認</span><span class="sxs-lookup"><span data-stu-id="dda91-120">-Confirm</span></span>
<span data-ttu-id="dda91-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="dda91-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dda91-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dda91-122">-WhatIf</span></span>
<span data-ttu-id="dda91-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="dda91-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dda91-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dda91-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dda91-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dda91-125">CommonParameters</span></span>
<span data-ttu-id="dda91-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dda91-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dda91-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="dda91-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dda91-128">輸入</span><span class="sxs-lookup"><span data-stu-id="dda91-128">INPUTS</span></span>

## <span data-ttu-id="dda91-129">輸出</span><span class="sxs-lookup"><span data-stu-id="dda91-129">OUTPUTS</span></span>

### <span data-ttu-id="dda91-130">IDiskMigrationJob （ComputeAdmin）。 Api20180730Preview。</span><span class="sxs-lookup"><span data-stu-id="dda91-130">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180730Preview.IDiskMigrationJob</span></span>



## <span data-ttu-id="dda91-131">筆記</span><span class="sxs-lookup"><span data-stu-id="dda91-131">NOTES</span></span>

## <span data-ttu-id="dda91-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="dda91-132">RELATED LINKS</span></span>

