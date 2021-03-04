---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskAccess.md
ms.openlocfilehash: 4b67364f0d079c7cd5fbbdd89b1a84b4dc6fee0e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911158"
---
# <span data-ttu-id="b882c-101">Remove-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="b882c-101">Remove-AzDiskAccess</span></span>

## <span data-ttu-id="b882c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b882c-102">SYNOPSIS</span></span>
<span data-ttu-id="b882c-103">移除磁片存取資源。</span><span class="sxs-lookup"><span data-stu-id="b882c-103">Removes a disk access resource.</span></span>

## <span data-ttu-id="b882c-104">語法</span><span class="sxs-lookup"><span data-stu-id="b882c-104">SYNTAX</span></span>

### <span data-ttu-id="b882c-105">DefaultParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b882c-105">DefaultParameterSet (Default)</span></span>
```
Remove-AzDiskAccess [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b882c-106">ResourceIDParameterSet</span><span class="sxs-lookup"><span data-stu-id="b882c-106">ResourceIDParameterSet</span></span>
```
Remove-AzDiskAccess [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b882c-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b882c-107">InputObjectParameterSet</span></span>
```
Remove-AzDiskAccess [-InputObject] <PSDiskAccess> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b882c-108">描述</span><span class="sxs-lookup"><span data-stu-id="b882c-108">DESCRIPTION</span></span>
<span data-ttu-id="b882c-109">**Remove-Az與Access** Cmdlet 會移除磁片存取資源。</span><span class="sxs-lookup"><span data-stu-id="b882c-109">The **Remove-AzDiskAccess** cmdlet removes a disk access resource.</span></span>

## <span data-ttu-id="b882c-110">例子</span><span class="sxs-lookup"><span data-stu-id="b882c-110">EXAMPLES</span></span>

### <span data-ttu-id="b882c-111">範例 1：使用預設參數集移除磁片存取</span><span class="sxs-lookup"><span data-stu-id="b882c-111">Example 1: Remove Disk Access using Default Parameter Set</span></span>
```
PS C:\> Remove-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01"
```

<span data-ttu-id="b882c-112">此命令會移除資源群組 "ResourceGroup01" 中名為 "DiskAccess01" 的磁片存取權</span><span class="sxs-lookup"><span data-stu-id="b882c-112">This command removes the disk access named "DiskAccess01" in resource group "ResourceGroup01"</span></span>

### <span data-ttu-id="b882c-113">範例 2：使用資源識別碼移除磁片存取</span><span class="sxs-lookup"><span data-stu-id="b882c-113">Example 2: Remove Disk Access using Resource ID</span></span>
```
PS C:\> $myDiskAccess = Get-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01"
PS C:\> Remove-AzDiskAccess -ResourceId $myDiskAccess.id
```

<span data-ttu-id="b882c-114">此命令會移除根據資源識別碼的磁片存取權</span><span class="sxs-lookup"><span data-stu-id="b882c-114">This command removes the disk access by Resource ID</span></span>

### <span data-ttu-id="b882c-115">範例 3：使用輸入物件移除磁片存取</span><span class="sxs-lookup"><span data-stu-id="b882c-115">Example 3: Remove Disk Access using Input Object</span></span>
```
PS C:\> $myDiskAccess = Get-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01"
PS C:\> Remove-AzDiskAccess -InputObject $myDiskAccess
```

<span data-ttu-id="b882c-116">此命令會移除 InputObject 的磁片存取權</span><span class="sxs-lookup"><span data-stu-id="b882c-116">This command removes the disk access by InputObject</span></span>

### <span data-ttu-id="b882c-117">範例 4：使用管道輸入物件移除磁片存取</span><span class="sxs-lookup"><span data-stu-id="b882c-117">Example 4: Remove Disk Access by piping Input Object</span></span>
```
PS C:\> Get-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01" | Remove-AzDiskAccess 
```

<span data-ttu-id="b882c-118">此命令會使用 InputObject 管道移除磁片存取</span><span class="sxs-lookup"><span data-stu-id="b882c-118">This command removes the disk access by piping the InputObject</span></span>

## <span data-ttu-id="b882c-119">參數</span><span class="sxs-lookup"><span data-stu-id="b882c-119">PARAMETERS</span></span>

### <span data-ttu-id="b882c-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b882c-120">-AsJob</span></span>
<span data-ttu-id="b882c-121">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b882c-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b882c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b882c-122">-DefaultProfile</span></span>
<span data-ttu-id="b882c-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b882c-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b882c-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b882c-124">-InputObject</span></span>
<span data-ttu-id="b882c-125">PowerShell 磁片存取物件</span><span class="sxs-lookup"><span data-stu-id="b882c-125">PowerShell Disk Access Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess
Parameter Sets: InputObjectParameterSet
Aliases: DiskAccess

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b882c-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="b882c-126">-Name</span></span>
<span data-ttu-id="b882c-127">指定磁片存取的名稱。</span><span class="sxs-lookup"><span data-stu-id="b882c-127">Specifies the name of a disk access.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases: DiskAccessName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b882c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b882c-128">-ResourceGroupName</span></span>
<span data-ttu-id="b882c-129">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b882c-129">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b882c-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b882c-130">-ResourceId</span></span>
<span data-ttu-id="b882c-131">您磁片存取的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="b882c-131">Resource ID for your disk access.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIDParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b882c-132">-確認</span><span class="sxs-lookup"><span data-stu-id="b882c-132">-Confirm</span></span>
<span data-ttu-id="b882c-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b882c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b882c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b882c-134">-WhatIf</span></span>
<span data-ttu-id="b882c-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b882c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b882c-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b882c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b882c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b882c-137">CommonParameters</span></span>
<span data-ttu-id="b882c-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b882c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b882c-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b882c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b882c-140">輸入</span><span class="sxs-lookup"><span data-stu-id="b882c-140">INPUTS</span></span>

### <span data-ttu-id="b882c-141">System.String</span><span class="sxs-lookup"><span data-stu-id="b882c-141">System.String</span></span>

### <span data-ttu-id="b882c-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span><span class="sxs-lookup"><span data-stu-id="b882c-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span></span>

## <span data-ttu-id="b882c-143">輸出</span><span class="sxs-lookup"><span data-stu-id="b882c-143">OUTPUTS</span></span>

### <span data-ttu-id="b882c-144">Microsoft.Azure.Commands.Compute.Automation.models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="b882c-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="b882c-145">筆記</span><span class="sxs-lookup"><span data-stu-id="b882c-145">NOTES</span></span>

## <span data-ttu-id="b882c-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="b882c-146">RELATED LINKS</span></span>
