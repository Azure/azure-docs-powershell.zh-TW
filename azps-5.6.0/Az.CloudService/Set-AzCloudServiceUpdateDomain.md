---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/set-azcloudserviceupdatedomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Set-AzCloudServiceUpdateDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Set-AzCloudServiceUpdateDomain.md
ms.openlocfilehash: 4b47992eb290c0a34ac2b368017d443051a6bb92
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911181"
---
# <span data-ttu-id="4d4c1-101">Set-AzCloudServiceUpdateDomain</span><span class="sxs-lookup"><span data-stu-id="4d4c1-101">Set-AzCloudServiceUpdateDomain</span></span>

## <span data-ttu-id="4d4c1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4d4c1-102">SYNOPSIS</span></span>
<span data-ttu-id="4d4c1-103">更新指定更新網域中的角色實例。</span><span class="sxs-lookup"><span data-stu-id="4d4c1-103">Updates the role instances in the specified update domain.</span></span>

## <span data-ttu-id="4d4c1-104">語法</span><span class="sxs-lookup"><span data-stu-id="4d4c1-104">SYNTAX</span></span>

```
Set-AzCloudServiceUpdateDomain -CloudServiceName <String> -ResourceGroupName <String> -UpdateDomain <Int32>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="4d4c1-105">描述</span><span class="sxs-lookup"><span data-stu-id="4d4c1-105">DESCRIPTION</span></span>
<span data-ttu-id="4d4c1-106">更新指定更新網域中的角色實例。</span><span class="sxs-lookup"><span data-stu-id="4d4c1-106">Updates the role instances in the specified update domain.</span></span>

## <span data-ttu-id="4d4c1-107">例子</span><span class="sxs-lookup"><span data-stu-id="4d4c1-107">EXAMPLES</span></span>

### <span data-ttu-id="4d4c1-108">範例 1：更新網域中的更新角色實例</span><span class="sxs-lookup"><span data-stu-id="4d4c1-108">Example 1: Update role instance in update domain</span></span>
```powershell
PS C:\> Set-AzCloudServiceUpdateDomain -CloudServiceName "ContosoCS" -ResourceGroupName "ContosOrg" -UpdateDomain 0
```

<span data-ttu-id="4d4c1-109">此命令會更新名為 ContosoCS 之雲端服務更新網域 0 中屬於 ContosOrg 資源群組的角色實例。</span><span class="sxs-lookup"><span data-stu-id="4d4c1-109">This command updates role instances in update domain 0 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="4d4c1-110">參數</span><span class="sxs-lookup"><span data-stu-id="4d4c1-110">PARAMETERS</span></span>

### <span data-ttu-id="4d4c1-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4d4c1-111">-AsJob</span></span>
<span data-ttu-id="4d4c1-112">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="4d4c1-112">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d4c1-113">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="4d4c1-113">-CloudServiceName</span></span>
<span data-ttu-id="4d4c1-114">雲端服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="4d4c1-114">Name of the cloud service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d4c1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d4c1-115">-DefaultProfile</span></span>
<span data-ttu-id="4d4c1-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4d4c1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d4c1-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="4d4c1-117">-NoWait</span></span>
<span data-ttu-id="4d4c1-118">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="4d4c1-118">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d4c1-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4d4c1-119">-PassThru</span></span>
<span data-ttu-id="4d4c1-120">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="4d4c1-120">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d4c1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d4c1-121">-ResourceGroupName</span></span>
<span data-ttu-id="4d4c1-122">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4d4c1-122">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d4c1-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4d4c1-123">-SubscriptionId</span></span>
<span data-ttu-id="4d4c1-124">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="4d4c1-124">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="4d4c1-125">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="4d4c1-125">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="4d4c1-126">-UpdateDomain</span><span class="sxs-lookup"><span data-stu-id="4d4c1-126">-UpdateDomain</span></span>
<span data-ttu-id="4d4c1-127">指定可識別更新網域的整數值。</span><span class="sxs-lookup"><span data-stu-id="4d4c1-127">Specifies an integer value that identifies the update domain.</span></span>
<span data-ttu-id="4d4c1-128">更新網域會以零型索引識別：第一個更新網域的識別碼為 0，第二個更新網域的識別碼為 1，以此類比。</span><span class="sxs-lookup"><span data-stu-id="4d4c1-128">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d4c1-129">-確認</span><span class="sxs-lookup"><span data-stu-id="4d4c1-129">-Confirm</span></span>
<span data-ttu-id="4d4c1-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="4d4c1-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d4c1-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d4c1-131">-WhatIf</span></span>
<span data-ttu-id="4d4c1-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4d4c1-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d4c1-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4d4c1-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d4c1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d4c1-134">CommonParameters</span></span>
<span data-ttu-id="4d4c1-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4d4c1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d4c1-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4d4c1-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d4c1-137">輸入</span><span class="sxs-lookup"><span data-stu-id="4d4c1-137">INPUTS</span></span>

## <span data-ttu-id="4d4c1-138">輸出</span><span class="sxs-lookup"><span data-stu-id="4d4c1-138">OUTPUTS</span></span>

### <span data-ttu-id="4d4c1-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4d4c1-139">System.Boolean</span></span>

## <span data-ttu-id="4d4c1-140">筆記</span><span class="sxs-lookup"><span data-stu-id="4d4c1-140">NOTES</span></span>

<span data-ttu-id="4d4c1-141">別名</span><span class="sxs-lookup"><span data-stu-id="4d4c1-141">ALIASES</span></span>

## <span data-ttu-id="4d4c1-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="4d4c1-142">RELATED LINKS</span></span>

