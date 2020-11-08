---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/set-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Set-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Set-AzHpcCache.md
ms.openlocfilehash: 909f3be2e4a08ff1d1b0538b451ffa93f368d211
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94136384"
---
# <span data-ttu-id="c63cf-101">Set-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="c63cf-101">Set-AzHpcCache</span></span>

## <span data-ttu-id="c63cf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c63cf-102">SYNOPSIS</span></span>
<span data-ttu-id="c63cf-103">更新 HPC 緩存上的標記。</span><span class="sxs-lookup"><span data-stu-id="c63cf-103">Updates tags on a HPC Cache.</span></span>

## <span data-ttu-id="c63cf-104">句法</span><span class="sxs-lookup"><span data-stu-id="c63cf-104">SYNTAX</span></span>

### <span data-ttu-id="c63cf-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c63cf-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzHpcCache -ResourceGroupName <String> -Name <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c63cf-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c63cf-106">ByObjectParameterSet</span></span>
```
Set-AzHpcCache -InputObject <PSHPCCache> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c63cf-107">說明</span><span class="sxs-lookup"><span data-stu-id="c63cf-107">DESCRIPTION</span></span>
<span data-ttu-id="c63cf-108">**AzHpcCache** Cmdlet 會更新 Azure HPC 緩存標籤。</span><span class="sxs-lookup"><span data-stu-id="c63cf-108">The **Set-AzHpcCache** cmdlet updates an Azure HPC Cache tags.</span></span>

## <span data-ttu-id="c63cf-109">示例</span><span class="sxs-lookup"><span data-stu-id="c63cf-109">EXAMPLES</span></span>

### <span data-ttu-id="c63cf-110">範例1</span><span class="sxs-lookup"><span data-stu-id="c63cf-110">Example 1</span></span>
```powershell
PS C:\> Set-AzHpcCache -ResourceGroupName testRG -CacheName testCache -Tag @{"tag3" = "value1"; "tag4" = "value2"}
```

## <span data-ttu-id="c63cf-111">參數</span><span class="sxs-lookup"><span data-stu-id="c63cf-111">PARAMETERS</span></span>

### <span data-ttu-id="c63cf-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c63cf-112">-AsJob</span></span>
<span data-ttu-id="c63cf-113">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c63cf-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c63cf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c63cf-114">-DefaultProfile</span></span>
<span data-ttu-id="c63cf-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c63cf-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c63cf-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c63cf-116">-InputObject</span></span>
<span data-ttu-id="c63cf-117">要更新的快取物件。</span><span class="sxs-lookup"><span data-stu-id="c63cf-117">The cache object to update.</span></span>

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

### <span data-ttu-id="c63cf-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="c63cf-118">-Name</span></span>
<span data-ttu-id="c63cf-119">快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="c63cf-119">Name of cache.</span></span>

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

### <span data-ttu-id="c63cf-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c63cf-120">-ResourceGroupName</span></span>
<span data-ttu-id="c63cf-121">您要在其上更新快取的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c63cf-121">Name of resource group under which you want to update cache.</span></span>

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

### <span data-ttu-id="c63cf-122">-Tag</span><span class="sxs-lookup"><span data-stu-id="c63cf-122">-Tag</span></span>
<span data-ttu-id="c63cf-123">要與 HPC 緩存關聯的標籤。</span><span class="sxs-lookup"><span data-stu-id="c63cf-123">The tags to associate with HPC Cache.</span></span> 

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c63cf-124">-確認</span><span class="sxs-lookup"><span data-stu-id="c63cf-124">-Confirm</span></span>
<span data-ttu-id="c63cf-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c63cf-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c63cf-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c63cf-126">-WhatIf</span></span>
<span data-ttu-id="c63cf-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c63cf-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c63cf-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c63cf-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c63cf-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c63cf-129">CommonParameters</span></span>
<span data-ttu-id="c63cf-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c63cf-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c63cf-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c63cf-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c63cf-132">輸入</span><span class="sxs-lookup"><span data-stu-id="c63cf-132">INPUTS</span></span>

### <span data-ttu-id="c63cf-133">System.object</span><span class="sxs-lookup"><span data-stu-id="c63cf-133">System.String</span></span>

### <span data-ttu-id="c63cf-134">System.object</span><span class="sxs-lookup"><span data-stu-id="c63cf-134">System.Int32</span></span>

## <span data-ttu-id="c63cf-135">輸出</span><span class="sxs-lookup"><span data-stu-id="c63cf-135">OUTPUTS</span></span>

### <span data-ttu-id="c63cf-136">PSHPCCache （HPCCache）的</span><span class="sxs-lookup"><span data-stu-id="c63cf-136">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span></span>

## <span data-ttu-id="c63cf-137">筆記</span><span class="sxs-lookup"><span data-stu-id="c63cf-137">NOTES</span></span>

## <span data-ttu-id="c63cf-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="c63cf-138">RELATED LINKS</span></span>