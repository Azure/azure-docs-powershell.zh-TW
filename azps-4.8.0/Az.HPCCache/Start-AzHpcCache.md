---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/start-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Start-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Start-AzHpcCache.md
ms.openlocfilehash: 7465a74db4da777d60e097fe959ef69bed11918c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94136385"
---
# <span data-ttu-id="90014-101">Start-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="90014-101">Start-AzHpcCache</span></span>

## <span data-ttu-id="90014-102">摘要</span><span class="sxs-lookup"><span data-stu-id="90014-102">SYNOPSIS</span></span>
<span data-ttu-id="90014-103">啟動 HPC 快取。</span><span class="sxs-lookup"><span data-stu-id="90014-103">Starts HPC cache.</span></span>

## <span data-ttu-id="90014-104">句法</span><span class="sxs-lookup"><span data-stu-id="90014-104">SYNTAX</span></span>

### <span data-ttu-id="90014-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="90014-105">ByFieldsParameterSet (Default)</span></span>
```
Start-AzHpcCache -ResourceGroupName <String> -Name <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90014-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="90014-106">ByResourceIdParameterSet</span></span>
```
Start-AzHpcCache -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90014-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="90014-107">ByObjectParameterSet</span></span>
```
Start-AzHpcCache -InputObject <PSHPCCache> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90014-108">說明</span><span class="sxs-lookup"><span data-stu-id="90014-108">DESCRIPTION</span></span>
<span data-ttu-id="90014-109">**AzHpcCache** Cmdlet 會啟動 Azure HPC 緩存。</span><span class="sxs-lookup"><span data-stu-id="90014-109">The **Start-AzHpcCache** cmdlet starts a Azure HPC Cache.</span></span>

## <span data-ttu-id="90014-110">示例</span><span class="sxs-lookup"><span data-stu-id="90014-110">EXAMPLES</span></span>

### <span data-ttu-id="90014-111">範例1</span><span class="sxs-lookup"><span data-stu-id="90014-111">Example 1</span></span>
```powershell
PS C:\> Start-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="90014-112">參數</span><span class="sxs-lookup"><span data-stu-id="90014-112">PARAMETERS</span></span>

### <span data-ttu-id="90014-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="90014-113">-AsJob</span></span>
<span data-ttu-id="90014-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="90014-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="90014-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90014-115">-DefaultProfile</span></span>
<span data-ttu-id="90014-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="90014-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90014-117">-Force</span><span class="sxs-lookup"><span data-stu-id="90014-117">-Force</span></span>
<span data-ttu-id="90014-118">表示 Cmdlet 不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="90014-118">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="90014-119">根據預設，這個 Cmdlet 會提示您確認是否要啟動快取。</span><span class="sxs-lookup"><span data-stu-id="90014-119">By default, this cmdlet prompts you to confirm that you want to start the cache.</span></span>

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

### <span data-ttu-id="90014-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="90014-120">-InputObject</span></span>
<span data-ttu-id="90014-121">要開始的快取物件。</span><span class="sxs-lookup"><span data-stu-id="90014-121">The cache object to start.</span></span>

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

### <span data-ttu-id="90014-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="90014-122">-Name</span></span>
<span data-ttu-id="90014-123">快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="90014-123">Name of cache.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: CacheName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90014-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="90014-124">-PassThru</span></span>
<span data-ttu-id="90014-125">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="90014-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="90014-126">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="90014-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="90014-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90014-127">-ResourceGroupName</span></span>
<span data-ttu-id="90014-128">您想要啟動快取的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="90014-128">Name of resource group under which you want to start cache.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90014-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="90014-129">-ResourceId</span></span>
<span data-ttu-id="90014-130">快取的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="90014-130">The resource id of the Cache</span></span>

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

### <span data-ttu-id="90014-131">-確認</span><span class="sxs-lookup"><span data-stu-id="90014-131">-Confirm</span></span>
<span data-ttu-id="90014-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="90014-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90014-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90014-133">-WhatIf</span></span>
<span data-ttu-id="90014-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="90014-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="90014-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="90014-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90014-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90014-136">CommonParameters</span></span>
<span data-ttu-id="90014-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="90014-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90014-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="90014-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90014-139">輸入</span><span class="sxs-lookup"><span data-stu-id="90014-139">INPUTS</span></span>

### <span data-ttu-id="90014-140">System.object</span><span class="sxs-lookup"><span data-stu-id="90014-140">System.String</span></span>

## <span data-ttu-id="90014-141">輸出</span><span class="sxs-lookup"><span data-stu-id="90014-141">OUTPUTS</span></span>

## <span data-ttu-id="90014-142">筆記</span><span class="sxs-lookup"><span data-stu-id="90014-142">NOTES</span></span>

## <span data-ttu-id="90014-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="90014-143">RELATED LINKS</span></span>
