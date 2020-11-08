---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/update-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Update-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Update-AzHpcCache.md
ms.openlocfilehash: 8f84323df269d8e0fbd0f60525e54595ef89f3e8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94136381"
---
# <span data-ttu-id="21edb-101">Update-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="21edb-101">Update-AzHpcCache</span></span>

## <span data-ttu-id="21edb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="21edb-102">SYNOPSIS</span></span>
<span data-ttu-id="21edb-103">更新 HPC 快取。</span><span class="sxs-lookup"><span data-stu-id="21edb-103">Updates a HPC Cache.</span></span>

## <span data-ttu-id="21edb-104">句法</span><span class="sxs-lookup"><span data-stu-id="21edb-104">SYNTAX</span></span>

### <span data-ttu-id="21edb-105">FlushParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="21edb-105">FlushParameterSet (Default)</span></span>
```
Update-AzHpcCache -ResourceGroupName <String> -Name <String> [-Flush] [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21edb-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="21edb-106">ByResourceIdParameterSet</span></span>
```
Update-AzHpcCache -ResourceGroupName <String> -Name <String> -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21edb-107">UpgradeParameterSet</span><span class="sxs-lookup"><span data-stu-id="21edb-107">UpgradeParameterSet</span></span>
```
Update-AzHpcCache -ResourceGroupName <String> -Name <String> [-Upgrade] [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21edb-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="21edb-108">ByObjectParameterSet</span></span>
```
Update-AzHpcCache -ResourceGroupName <String> -Name <String> -InputObject <PSHPCCache> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21edb-109">說明</span><span class="sxs-lookup"><span data-stu-id="21edb-109">DESCRIPTION</span></span>
<span data-ttu-id="21edb-110">**AzHpcCache** Cmdlet 會更新 Azure HPC 緩存。</span><span class="sxs-lookup"><span data-stu-id="21edb-110">The **Update-AzHpcCache** cmdlet updates a Azure HPC Cache.</span></span>

## <span data-ttu-id="21edb-111">示例</span><span class="sxs-lookup"><span data-stu-id="21edb-111">EXAMPLES</span></span>

### <span data-ttu-id="21edb-112">範例1</span><span class="sxs-lookup"><span data-stu-id="21edb-112">Example 1</span></span>
```powershell
PS C:\> Update-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="21edb-113">參數</span><span class="sxs-lookup"><span data-stu-id="21edb-113">PARAMETERS</span></span>

### <span data-ttu-id="21edb-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="21edb-114">-AsJob</span></span>
<span data-ttu-id="21edb-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="21edb-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="21edb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21edb-116">-DefaultProfile</span></span>
<span data-ttu-id="21edb-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="21edb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21edb-118">-Flush</span><span class="sxs-lookup"><span data-stu-id="21edb-118">-Flush</span></span>
<span data-ttu-id="21edb-119">刷新 HPC 快取。</span><span class="sxs-lookup"><span data-stu-id="21edb-119">Flushes HPC Cache.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FlushParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21edb-120">-Force</span><span class="sxs-lookup"><span data-stu-id="21edb-120">-Force</span></span>
<span data-ttu-id="21edb-121">表示 Cmdlet 不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="21edb-121">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="21edb-122">根據預設，這個 Cmdlet 會提示您確認是否要更新快取。</span><span class="sxs-lookup"><span data-stu-id="21edb-122">By default, this cmdlet prompts you to confirm that you want to update the cache.</span></span>

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

### <span data-ttu-id="21edb-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="21edb-123">-InputObject</span></span>
<span data-ttu-id="21edb-124">要更新的快取物件。</span><span class="sxs-lookup"><span data-stu-id="21edb-124">The cache object to update.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="21edb-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="21edb-125">-Name</span></span>
<span data-ttu-id="21edb-126">快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="21edb-126">Name of cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CacheName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21edb-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="21edb-127">-PassThru</span></span>
<span data-ttu-id="21edb-128">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="21edb-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="21edb-129">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="21edb-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="21edb-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21edb-130">-ResourceGroupName</span></span>
<span data-ttu-id="21edb-131">您要在其上更新快取的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="21edb-131">Name of resource group under which you want to update cache.</span></span>

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

### <span data-ttu-id="21edb-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="21edb-132">-ResourceId</span></span>
<span data-ttu-id="21edb-133">快取的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="21edb-133">The resource id of the Cache</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21edb-134">-升級</span><span class="sxs-lookup"><span data-stu-id="21edb-134">-Upgrade</span></span>
<span data-ttu-id="21edb-135">升級 HpcCache。</span><span class="sxs-lookup"><span data-stu-id="21edb-135">Upgrade HpcCache.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpgradeParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21edb-136">-確認</span><span class="sxs-lookup"><span data-stu-id="21edb-136">-Confirm</span></span>
<span data-ttu-id="21edb-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="21edb-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21edb-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21edb-138">-WhatIf</span></span>
<span data-ttu-id="21edb-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="21edb-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="21edb-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="21edb-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21edb-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21edb-141">CommonParameters</span></span>
<span data-ttu-id="21edb-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="21edb-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21edb-143">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="21edb-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21edb-144">輸入</span><span class="sxs-lookup"><span data-stu-id="21edb-144">INPUTS</span></span>

### <span data-ttu-id="21edb-145">System.object</span><span class="sxs-lookup"><span data-stu-id="21edb-145">System.String</span></span>

## <span data-ttu-id="21edb-146">輸出</span><span class="sxs-lookup"><span data-stu-id="21edb-146">OUTPUTS</span></span>

## <span data-ttu-id="21edb-147">筆記</span><span class="sxs-lookup"><span data-stu-id="21edb-147">NOTES</span></span>

## <span data-ttu-id="21edb-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="21edb-148">RELATED LINKS</span></span>
