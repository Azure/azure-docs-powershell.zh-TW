---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/set-azcloudserviceupdatedomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Set-AzCloudServiceUpdateDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Set-AzCloudServiceUpdateDomain.md
ms.openlocfilehash: 4ffb65d4eca9511e179d33c53cb8f515c28aab58
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100141390"
---
# <span data-ttu-id="dbdde-101">Set-AzCloudServiceUpdateDomain</span><span class="sxs-lookup"><span data-stu-id="dbdde-101">Set-AzCloudServiceUpdateDomain</span></span>

## <span data-ttu-id="dbdde-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dbdde-102">SYNOPSIS</span></span>
<span data-ttu-id="dbdde-103">更新指定更新網域中的角色實例。</span><span class="sxs-lookup"><span data-stu-id="dbdde-103">Updates the role instances in the specified update domain.</span></span>

## <span data-ttu-id="dbdde-104">句法</span><span class="sxs-lookup"><span data-stu-id="dbdde-104">SYNTAX</span></span>

```
Set-AzCloudServiceUpdateDomain -CloudServiceName <String> -ResourceGroupName <String> -UpdateDomain <Int32>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="dbdde-105">說明</span><span class="sxs-lookup"><span data-stu-id="dbdde-105">DESCRIPTION</span></span>
<span data-ttu-id="dbdde-106">更新指定更新網域中的角色實例。</span><span class="sxs-lookup"><span data-stu-id="dbdde-106">Updates the role instances in the specified update domain.</span></span>

## <span data-ttu-id="dbdde-107">示例</span><span class="sxs-lookup"><span data-stu-id="dbdde-107">EXAMPLES</span></span>

### <span data-ttu-id="dbdde-108">範例1： update 網域中的更新角色實例</span><span class="sxs-lookup"><span data-stu-id="dbdde-108">Example 1: Update role instance in update domain</span></span>
```powershell
PS C:\> Set-AzCloudServiceUpdateDomain -CloudServiceName "ContosoCS" -ResourceGroupName "ContosOrg" -UpdateDomain 0
```

<span data-ttu-id="dbdde-109">這個命令會更新屬於名為 ContosOrg 之資源群組且名為 ContosoCS 的雲端服務更新網域0中的角色實例。</span><span class="sxs-lookup"><span data-stu-id="dbdde-109">This command updates role instances in update domain 0 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="dbdde-110">參數</span><span class="sxs-lookup"><span data-stu-id="dbdde-110">PARAMETERS</span></span>

### <span data-ttu-id="dbdde-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dbdde-111">-AsJob</span></span>
<span data-ttu-id="dbdde-112">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="dbdde-112">Run the command as a job</span></span>

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

### <span data-ttu-id="dbdde-113">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="dbdde-113">-CloudServiceName</span></span>
<span data-ttu-id="dbdde-114">雲端服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="dbdde-114">Name of the cloud service.</span></span>

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

### <span data-ttu-id="dbdde-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbdde-115">-DefaultProfile</span></span>
<span data-ttu-id="dbdde-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dbdde-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dbdde-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="dbdde-117">-NoWait</span></span>
<span data-ttu-id="dbdde-118">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="dbdde-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="dbdde-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dbdde-119">-PassThru</span></span>
<span data-ttu-id="dbdde-120">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="dbdde-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="dbdde-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbdde-121">-ResourceGroupName</span></span>
<span data-ttu-id="dbdde-122">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="dbdde-122">Name of the resource group.</span></span>

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

### <span data-ttu-id="dbdde-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dbdde-123">-SubscriptionId</span></span>
<span data-ttu-id="dbdde-124">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="dbdde-124">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="dbdde-125">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="dbdde-125">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="dbdde-126">-UpdateDomain</span><span class="sxs-lookup"><span data-stu-id="dbdde-126">-UpdateDomain</span></span>
<span data-ttu-id="dbdde-127">指定識別更新網域的整數值。</span><span class="sxs-lookup"><span data-stu-id="dbdde-127">Specifies an integer value that identifies the update domain.</span></span>
<span data-ttu-id="dbdde-128">更新網域是以零為基礎的索引來標識：第一個更新網域的識別碼為0，第二個是 ID 為1，依此類推。</span><span class="sxs-lookup"><span data-stu-id="dbdde-128">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

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

### <span data-ttu-id="dbdde-129">-確認</span><span class="sxs-lookup"><span data-stu-id="dbdde-129">-Confirm</span></span>
<span data-ttu-id="dbdde-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="dbdde-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbdde-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbdde-131">-WhatIf</span></span>
<span data-ttu-id="dbdde-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="dbdde-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dbdde-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dbdde-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbdde-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbdde-134">CommonParameters</span></span>
<span data-ttu-id="dbdde-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dbdde-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbdde-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="dbdde-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbdde-137">輸入</span><span class="sxs-lookup"><span data-stu-id="dbdde-137">INPUTS</span></span>

## <span data-ttu-id="dbdde-138">輸出</span><span class="sxs-lookup"><span data-stu-id="dbdde-138">OUTPUTS</span></span>

### <span data-ttu-id="dbdde-139">System.object</span><span class="sxs-lookup"><span data-stu-id="dbdde-139">System.Boolean</span></span>

## <span data-ttu-id="dbdde-140">筆記</span><span class="sxs-lookup"><span data-stu-id="dbdde-140">NOTES</span></span>

<span data-ttu-id="dbdde-141">別名</span><span class="sxs-lookup"><span data-stu-id="dbdde-141">ALIASES</span></span>

## <span data-ttu-id="dbdde-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="dbdde-142">RELATED LINKS</span></span>

